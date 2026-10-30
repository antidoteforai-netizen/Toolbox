# Installer n8n en local avec Docker

Une seule commande suffit pour faire tourner n8n chez toi, sans config à la main ni conflit de versions, et on fait ça ensemble, étape par étape.

```bash
$ docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
Editor is now accessible via: http://localhost:5678
```

## Sommaire

- [En local, avant de te lancer](#en-local-avant-de-te-lancer)
- [Pourquoi Docker](#pourquoi-docker-et-pas-une-install-classique)
- [01 · Installer Docker Desktop](#01--installer-docker-desktop)
- [02 · Créer le volume de données](#02--créer-le-volume-de-données)
- [03 · Lancer n8n](#03--lancer-n8n)
- [Le quotidien](#le-quotidien)
- [Mettre à jour n8n](#mettre-à-jour-n8n)
- [Les erreurs classiques](#les-erreurs-classiques)
- [Check final](#check-final)
- [Bonnes pratiques](#bonnes-pratiques)
- [Travailler à plusieurs en local](#travailler-à-plusieurs-en-local)
- [Questions de pros](#questions-de-pros)

## En local, avant de te lancer

Ce tuto installe n8n sur ta machine et non sur un serveur, ce qui est le bon move pour apprendre, prototyper et tester des workflows sans rien payer, mais pas pour tout. Mets ça au clair avant de commencer :

| Avantages | Limites |
|---|---|
| Zéro coût, zéro serveur à gérer | N'existe que quand ton ordi et ton terminal tournent |
| Tu vois tes logs en direct, tu comprends ce qui se passe | Pas de webhooks fiables, ton instance n'est pas joignable depuis internet |
| Tes credentials et données restent chez toi, point | SQLite par défaut : très bien seul, ça coince à plusieurs utilisateurs simultanés |
| Idéal pour apprendre n8n et tester des idées vite | Pas de vraie collab multi-utilisateurs sans licence payante |
| Aucune limite d'exécutions (contrairement au Cloud) | Rien ne tourne si tu fermes ton laptop |

> Besoin que ça tourne 24/7, que ça reçoive des webhooks externes, ou que plusieurs personnes y touchent en même temps ? C'est le signal qu'il te faut un serveur (VPS), pas ce setup. On garde ça pour un autre tuto.

### À la fin de ce tuto, tu sais

- Ce qu'est Docker, et pourquoi c'est la méthode reco pour n8n
- Installer Docker Desktop, puis créer le volume qui t'évite de perdre tes workflows
- Lancer n8n d'une seule commande et l'ouvrir dans ton navigateur
- Le démarrer et l'arrêter au quotidien, sans y réfléchir
- Le mettre à jour sans casser tes données

## Pourquoi Docker, et pas une install classique

n8n s'installe de plusieurs façons, et Docker est celle que l'équipe recommande officiellement. Et honnêtement, c'est aussi la plus simple à comprendre une fois que t'as capté le principe.

Docker fait tourner n8n dans une boîte isolée qui contient tout ce dont il a besoin. Zéro dépendance à installer toi-même, zéro conflit de versions, zéro "ça marche chez moi mais pas chez toi" : la même commande tourne sur Windows, Mac et Linux sans rien changer.

| Terme | Ce que c'est |
|---|---|
| **Conteneur** | Une boîte isolée qui contient l'appli et tout ce qu'il lui faut pour tourner. Tu la supprimes, ton ordi reste intact. Rien n'a touché le reste du système. |
| **Image Docker** | Le modèle qui décrit ce que le conteneur doit contenir. n8n publie la sienne officiellement sur Docker Hub. |
| **Volume** | Un conteneur, par défaut, est éphémère : tu l'arrêtes, tout disparaît. Le volume, c'est l'espace de stockage qui vit en dehors du conteneur. Tes workflows, credentials et paramètres survivent, même si tu recrées le conteneur. |

> **L'image**, c'est la recette. **Le conteneur**, c'est le gâteau.

## 01 · Installer Docker Desktop

Docker Desktop, c'est l'appli qui fait tourner Docker chez toi, et elle s'installe comme n'importe quel logiciel.

### Windows

Va sur [docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop/), télécharge la version Windows, lance le fichier. Pendant l'install, laisse coché **WSL 2**, c'est la config recommandée. Redémarre si on te le demande, puis lance Docker Desktop depuis le menu Démarrer. Une baleine apparaît dans la barre des tâches : attends qu'elle soit stable.

> WSL 2 = Windows Subsystem for Linux. Un noyau Linux qui tourne dans Windows, et dont Docker se sert en arrière-plan. Tu n'as rien à gérer directement.

### Mac

Même page, télécharge la bonne version : Apple Silicon (M1/M2/M3) ou Intel. Pour vérifier ta puce → Pomme > À propos de ce Mac. Ouvre le `.dmg`, glisse Docker dans Applications, lance-le. La baleine apparaît en haut à droite : attends qu'elle soit stable.

### Linux (Ubuntu / Debian)

Ça se passe dans le terminal :

```bash
sudo apt update
sudo apt install -y ca-certificates curl gnupg

sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo $VERSION_CODENAME) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin

sudo usermod -aG docker $USER
newgrp docker
```

Vérifie l'install, tous systèmes confondus :

```bash
$ docker --version
Docker version 24.0.5
```

> Sur Windows et Mac, Docker Desktop doit tourner en arrière-plan pour que les commandes fonctionnent. Fermé = les commandes échouent.

## 02 · Créer le volume de données

Avant de lancer n8n, tu crées, une fois pour toutes, le volume qui va stocker tes données.

```bash
$ docker volume create n8n_data
n8n_data
```

Docker te renvoie `n8n_data` : c'est la confirmation. Ce volume survit à toutes les mises à jour et à tous les redémarrages de conteneur, alors tes workflows y restent, point.

## 03 · Lancer n8n

C'est parti, tout tient en une commande :

```bash
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```

| Morceau | Ce qu'il fait |
|---|---|
| `docker run` | lance un nouveau conteneur |
| `-it` | mode interactif, tu vois les logs défiler |
| `--rm` | supprime le conteneur à l'arrêt (les données, elles, restent dans le volume) |
| `--name n8n` | donne un nom au conteneur |
| `-p 5678:5678` | connecte le port de ta machine à celui du conteneur |
| `-v n8n_data:...` | attache le volume au bon dossier n8n |
| `docker.n8n.io/n8nio/n8n` | l'image officielle |

Au premier lancement, Docker télécharge l'image, ce qui prend quelques minutes selon ta connexion, et les fois suivantes ce sera instantané. Tu sais que c'est bon quand tu vois :

```text
Editor is now accessible via: http://localhost:5678
```

Ouvre <http://localhost:5678> dans ton navigateur. Au premier lancement, n8n te demande de créer un compte local, stocké uniquement chez toi, dans le volume.

> `localhost` = ton propre ordinateur. `5678` = le port, il identifie n8n parmi tout ce qui tourne sur ta machine. Toujours la même adresse en local.

Tant que n8n tourne, laisse le terminal ouvert. Pour arrêter : `Ctrl + C`.

## Le quotidien

**Démarrer :**

1. Ouvre Docker Desktop, attends que la baleine soit stable (Windows / Mac)
2. Ouvre un terminal
3. Lance la commande `docker run`
4. Attends le message `Editor is now accessible`
5. Ouvre <http://localhost:5678>

**Arrêter :** retourne dans le terminal, `Ctrl + C`. Le conteneur s'arrête, tes workflows restent dans le volume.

**Se simplifier la vie :** la commande est longue à retaper à chaque fois. Sur Mac / Linux, crée un alias :

```bash
echo "alias n8n='docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n'" >> ~/.zshrc
source ~/.zshrc
```

> Ton terminal tourne sous bash plutôt que zsh ? Remplace `~/.zshrc` par `~/.bashrc`.

Ensuite, taper `n8n` suffit, et tu n'as plus rien à copier-coller.

Sur Windows : crée un fichier `lancer-n8n.bat` sur ton bureau, avec ce contenu, et double-clique dessus :

```bat
@echo off
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```

## Mettre à jour n8n

Arrête n8n s'il tourne, télécharge la nouvelle image et relance : tes données ne bougent pas.

```bash
docker pull docker.n8n.io/n8nio/n8n
```

Relance ensuite avec ta commande habituelle. Docker prend la nouvelle image automatiquement.

## Les erreurs classiques

| Erreur | Cause et solution |
|---|---|
| `port is already allocated` | Un autre programme squatte le port 5678, ou n8n tourne déjà ailleurs. Check tes terminaux ouverts. Sinon, remplace `-p 5678:5678` par `-p 5679:5678` et va sur <http://localhost:5679>. |
| `Cannot connect to the Docker daemon` | Docker Desktop n'est pas lancé. Ouvre-le, attends la baleine stable, retente. |
| `container name already in use` | Un conteneur nommé n8n existe déjà, même arrêté. Supprime-le : `docker rm n8n`, puis relance. |
| La page ne s'affiche pas | Vérifie que le terminal a bien affiché `Editor is now accessible`. Si oui mais rien à l'écran, attends quelques secondes, rafraîchis. Essaie aussi <http://127.0.0.1:5678>, même adresse que localhost. |

## Check final

Avant de passer à la suite, vérifie que tout tient debout :

- [ ] Lance n8n, va sur <http://localhost:5678>
- [ ] Crée un workflow, donne-lui un nom, sauvegarde
- [ ] Arrête avec `Ctrl + C`
- [ ] Relance la même commande
- [ ] Retourne sur localhost:5678, ton workflow doit être là

**Workflow toujours là ?** Ton install est bonne, le volume fait son job. Tu peux construire sans risquer de perdre quoi que ce soit.

**Workflow disparu ?** Le volume n'est pas bien attaché. Vérifie que ta commande contient bien `-v n8n_data:/home/node/.n8n`, et que le volume existe avec `docker volume ls`.

### Toutes les commandes, résumées

| Commande | Rôle |
|---|---|
| `docker --version` | vérifie que Docker est installé |
| `docker volume create n8n_data` | crée le volume (une seule fois) |
| `docker run ...` | lance n8n |
| `docker pull ...` | télécharge la dernière version |
| `docker rm n8n` | supprime un conteneur arrêté |
| `Ctrl + C` | arrête n8n depuis le terminal |

## Bonnes pratiques

Une fois l'install en route, quelques réflexes la font durer sans mauvaise surprise.

### Coupe n8n quand tu ne l'utilises pas

Avec la commande `-it --rm`, n8n ne tourne que quand ton terminal est ouvert, sans service qui reste actif en tâche de fond 24/7. Ferme-le en fin de session, comme n'importe quelle appli lourde.

Nuance importante : les Schedule Trigger et les webhooks ne se déclenchent que si n8n tourne au moment prévu. Un workflow programmé à 9h ne partira pas si ton n8n local est éteint à 9h. Pour de l'automatisation qui doit tourner sans toi, il faut un hébergement distant, pas ce setup local.

### Sauvegarde le volume, pas juste tes workflows

Le dossier `/home/node/.n8n` contient aussi ta clé de chiffrement, celle qui protège tes credentials. Si elle disparaît ou change, tous tes identifiants stockés deviennent illisibles, même si les workflows sont toujours là.

```bash
# pendant que le conteneur tourne
docker cp n8n:/home/node/.n8n ./backup-n8n-$(date +%Y%m%d)
```

Une copie de temps en temps, sur un disque externe ou un cloud perso, et tu ne repars jamais de zéro.

### Mets à jour régulièrement, mais pas les yeux fermés

n8n sort une nouvelle version quasiment chaque semaine, ce qui est utile pour les nouveautés et risqué si tu casses un workflow en prod perso sans t'en rendre compte. Avant un `docker pull`, jette un œil au changelog (la liste des changements de la version). Et si un workflow est critique, teste la mise à jour avant de l'appliquer partout.

### Configure ton fuseau horaire dès le départ

Sans ça, tes Schedule Trigger peuvent se déclencher à la mauvaise heure. Ajoute ces deux variables à ta commande `docker run` :

```bash
-e GENERIC_TIMEZONE="Europe/Paris" -e TZ="Europe/Paris"
```

`GENERIC_TIMEZONE` pilote les nodes programmés (Schedule Trigger). `TZ` règle l'heure système du conteneur. Il faut les deux, sinon ça se contredit.

### Le tunnel webhook, c'est du dev only

n8n propose un service de tunnel (via cloudflared) pour recevoir des webhooks externes (GitHub, Stripe, etc.) sur ton instance locale. Pratique pour tester, mais l'implémentation change d'une version à l'autre et ce n'est pas fait pour tourner en continu. Pour un usage stable, il faut une vraie instance hébergée, joignable depuis internet.

### SQLite en local, très bien, jusqu'à un certain point

Par défaut, n8n stocke tout dans une base SQLite, dans le volume, ce qui suffit largement pour un usage perso ou des tests. Si tu montes en charge (beaucoup de workflows, exécutions fréquentes, plusieurs personnes), c'est le signe qu'il est temps de passer à PostgreSQL et à une vraie instance, ce qui sort du cadre de ce tuto local.

## Travailler à plusieurs en local

Question qui revient vite : "comment je fais si un collègue bosse sur les mêmes workflows ?" Réponse courte : en édition Community (ce qu'on installe dans ce tuto), il n'y a pas de vraie collab native. Voici ce qui existe réellement.

| Pas possible, gratuit | Possible, gratuit |
|---|---|
| Partage de workflows entre comptes, avec permissions, réservé aux plans payants (Projects, rôles) | Export/import manuel : chacun exporte son workflow en JSON, le partage, l'autre importe |
| Version control Git natif dans l'éditeur (push/pull, branches), fonctionnalité `.ee`, sous licence Enterprise | Export en masse via la CLI, à committer dans un repo Git |
| Édition simultanée à plusieurs sur le même workflow | Extensions tierces gratuites qui connectent l'instance à GitHub pour un push/pull en un clic |

La méthode manuelle, celle qui coûte rien :

```bash
# chacun de son côté
n8n export:workflow --all --output=./backups/
# puis commit + push dans un repo Git partagé
git add backups/ && git commit -m "update workflows" && git push
```

Basique, pas de merge automatique, pas de review façon pull request dans n8n lui-même, mais ça donne un historique de versions et un point de partage commun, sans sortir la carte bleue.

> **Pour une vraie collab à plusieurs, en simultané :** deux options honnêtes. Un plan Business/Enterprise (self-hosted ou Cloud) pour le partage natif avec permissions, ou une instance hébergée à distance sur laquelle tout le monde se connecte, donc plus vraiment "en local". Ce tuto reste pensé pour un poste perso ; au-delà, c'est un autre sujet.

## Questions de pros

Passé un moment, ce setup local montre ses limites. Voici les questions qui reviennent le plus chez les gens qui poussent n8n plus loin, et où ça les mène.

<details>
<summary><strong>SQLite tient jusqu'où, exactement ?</strong></summary>

SQLite verrouille tout le fichier à chaque écriture. Deux workflows qui se terminent en même temps peuvent se percuter. En solo, sur ton poste, c'est invisible. Dès que tu as plusieurs webhooks déclenchés en parallèle ou plusieurs personnes qui bossent sur la même instance, PostgreSQL devient la vraie réponse, c'est d'ailleurs ce que recommande n8n en production.
</details>

<details>
<summary><strong>Pourquoi mes webhooks externes (GitHub, Stripe...) ne marchent jamais en local ?</strong></summary>

Parce que ton instance n'est pas joignable depuis internet, localhost ne veut rien dire pour un serveur externe. Le tunnel cloudflared de n8n dépanne pour tester, mais il est pensé dev-only, pas pour tourner en continu. Pour des webhooks fiables, il faut une instance hébergée avec une vraie URL publique.
</details>

<details>
<summary><strong>C'est quoi le "queue mode" dont tout le monde parle ?</strong></summary>

Un mode d'exécution où n8n distribue les tâches à des workers séparés via Redis, au lieu de tout traiter dans un seul process. Ça évite qu'un workflow long bloque toute l'interface. Utile dès que tu as des exécutions fréquentes, longues, ou beaucoup de trafic simultané. Sur un poste perso, c'est disproportionné : une brique d'infra en plus à maintenir.
</details>

<details>
<summary><strong>Docker en local, c'est sécurisé pour mes credentials ?</strong></summary>

Sur ta propre machine, oui, tant que ton poste l'est. Le vrai risque arrive si tu exposes un jour ce même conteneur sur un serveur accessible depuis internet sans authentification, sans HTTPS, sans restriction d'accès. Ce qui est acceptable en local (pas d'auth, port ouvert) devient une faille béante sur un VPS public.
</details>

<details>
<summary><strong>Je veux automatiser mes sauvegardes plutôt que le faire à la main. Comment ?</strong></summary>

La CLI n8n permet d'exporter tous les workflows en JSON : `n8n export:workflow --all --output=./backups/`. Tu peux brancher ça sur une tâche planifiée (cron) qui commit automatiquement ces fichiers dans un repo Git. Ça te donne un historique de versions sans passer par la fonctionnalité Git native, qui elle est réservée aux licences payantes.
</details>

<details>
<summary><strong>À partir de quand ça vaut le coup de passer sur un VPS ?</strong></summary>

Trois signaux : tu as besoin que ça tourne sans que ton ordi soit allumé, tu reçois des webhooks externes de façon régulière, ou plusieurs personnes doivent y toucher en même temps. Un seul de ces cas coché, et le local a fait son travail, direction un serveur.
</details>

**Ailleurs dans la Toolbox**

- Ton premier workflow une fois n8n lancé → [S'organiser avec n8n, Notion et Airtable](./tutoriels-par-profil.md#sorganiser-avec-n8n-notion-et-airtable) et [le pipeline de contenu](./tutoriels-par-profil.md#construire-ton-pipeline-de-contenu-avec-n8n--airtable)
- À quoi sert n8n, et pour qui → [La boîte à outils IA](../guides/boite-a-outils-ia.md#n8n)

---

*n8n × Docker, installation locale · un tuto, pas un roman.*
