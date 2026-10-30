# Tutoriels par profil

**Neuf tutoriels en trois parcours, sans sauter une seule étape** : c’est la suite logique de [la boîte à outils](../guides/boite-a-outils-ia.md). Ici, pas de vue d’ensemble, mais des étapes numérotées, des commandes à coller et des astuces placées à l’endroit précis où tu vas en avoir besoin. Suis ton parcours du début à la fin, une seule fois, et tu n’auras plus besoin de revenir sur les bases.

## Sommaire

- [Comment utiliser ça](#comment-utiliser-ça)
- [Parcours 1 · Product Designer & Builder](#parcours-1--product-designer--builder)
- [Prendre en main Claude Code & le vibe coding](#prendre-en-main-claude-code--le-vibe-coding)
- [Vibe coding, tester ce que tu construis avec Playwright](#vibe-coding-tester-ce-que-tu-construis-avec-playwright)
- [Webflow, de la maquette au site en ligne](#webflow-de-la-maquette-au-site-en-ligne)
- [Parcours 2 · Com & Marketing](#parcours-2--com--marketing)
- [S’organiser avec N8N, Notion et Airtable](#sorganiser-avec-n8n-notion-et-airtable)
- [Génération visuelle à l’échelle avec Higgsfield](#génération-visuelle-à-léchelle-avec-higgsfield)
- [Sites & landing pages : Webflow et les alternatives rapides](#sites--landing-pages--webflow-et-les-alternatives-rapides)
- [Parcours 3 · Business Instagram](#parcours-3--business-instagram)
- [Construire une identité visuelle cohérente avec Higgsfield](#construire-une-identité-visuelle-cohérente-avec-higgsfield)
- [Construire ton pipeline de contenu avec N8N & Airtable](#construire-ton-pipeline-de-contenu-avec-n8n--airtable)
- [Ce qui marche vraiment sur Instagram en 2026](#ce-qui-marche-vraiment-sur-instagram-en-2026)
- [Sources vérifiées](#sources-vérifiées)

## Comment utiliser ça

Il y a trois parcours, un par profil, et chacun contient trois tutoriels à suivre dans l’ordre, parce que chaque tutoriel part du principe que tu as fait le précédent. Chaque tutoriel se lit en une session : installe, teste, passe au suivant un autre jour si besoin. Les blocs de code sont des commandes ou du texte à coller tel quel. Les encadrés 💡 sont des astuces qui évitent l’erreur classique du débutant sur cette étape précise. Les encadrés ⚠️ sont des points de vigilance, lis-les, ils ne sont pas là pour décorer.

Tu n’es pas obligé·e de rester dans ton parcours : un designer qui gère aussi le compte Instagram de sa boîte a tout intérêt à lire le parcours Business Instagram en plus du sien. Choisis selon ce que tu dois vraiment faire cette semaine, pas selon ton titre de poste.

## Parcours 1 · Product Designer & Builder

De la maquette au lien qu’on peut envoyer à un client, en trois tutoriels qui suivent l’ordre logique d’un vrai projet : tu construis, tu vérifies que ça marche vraiment, tu livres.

1. Claude Code & vibe coding
2. Tester avec Playwright
3. Webflow

*Parcours Designer · tutoriel 1/3 · ~40 min*

## Prendre en main Claude Code & le vibe coding

Installer, donner ta première vraie instruction, et comprendre la différence entre explorer vite et livrer proprement.

**Prérequis :** Node.js installé sur ta machine, un terminal, un compte Claude (Pro, Max, ou accès API).

### Installer Claude Code

Depuis ton terminal, installe le paquet officiel puis lance-le dans le dossier de ton projet (ou un dossier vide pour t’entraîner).

```bash
npm install -g @anthropic-ai/claude-code
cd mon-projet
claude
```

La première fois, on te demande de te connecter à ton compte. Une fois fait, tu es dans une session interactive : tu peux discuter, mais aussi laisser Claude lire, écrire et exécuter du code directement dans ce dossier.

### Donner une instruction précise, pas une idée vague

"Fais-moi un site" est le meilleur moyen d’obtenir un résultat générique. Donne le contexte, le format, et un exemple si tu en as un.

```text
Crée une landing page en Next.js avec un formulaire
d'inscription email. Palette : noir, blanc, un accent
orange. Le texte du hero est : "Rejoins la liste
d'attente". Le formulaire doit valider l'email et
afficher un message de confirmation.
```

Claude va d’abord t’exposer un plan avant de commencer à écrire, c’est le moment de corriger si l’interprétation ne colle pas à ce que tu voulais.

### Comprendre le cycle Explore → Plan → Code → Commit

C’est le rythme de travail qui distingue un usage professionnel d’un usage jetable : Claude explore le code existant (ou pose des questions si le projet est neuf), propose un plan, écrit le code par itérations, puis tu valides avant de passer à la suite. Ne saute pas l’étape "plan" sur un vrai projet, c’est là que tu rattrapes un malentendu avant qu’il ne devienne 200 lignes de code à défaire.

### Créer ton fichier CLAUDE.md

À la racine du projet, un fichier texte qui décrit les conventions, la stack, ce qu’il ne faut jamais faire. Claude le lit à chaque session, tu arrêtes de tout réexpliquer à chaque fois.

```markdown
# CLAUDE.md
Stack : Next.js, Tailwind, déployé sur Vercel.
Style : composants fonctionnels, pas de classes.
Toujours écrire les textes en français.
Ne jamais commit de clé API en dur dans le code.
```

### Savoir quand tu vibe-codes, et quand tu relis

Pour explorer une idée un week-end, accepte les suggestions et avance vite, c’est l’esprit d’origine du vibe coding. À partir du moment où un vrai client ou un vrai utilisateur va toucher le résultat, relis le code avant d’envoyer, même en diagonale. C’est la seule règle qui protège ta crédibilité professionnelle sur ce point précis.

### Les réflexes de debug qui font gagner du temps

Colle les messages d’erreur bruts, sans les résumer, Claude Code s’en sort mieux avec le texte exact qu’avec ta reformulation. Si une session part dans une mauvaise direction, reviens en arrière au lieu d’accumuler les corrections successives.

> 💡 **Astuce.** Demande explicitement à Claude Code de te présenter son plan avant d’écrire quoi que ce soit ("explique ton plan avant de commencer") si tu sens que la tâche est ambiguë, ça coûte trente secondes et ça évite de défaire une heure de travail.

> ➡️ **Pour aller plus loin.** Une fois ce tutoriel terminé, la suite logique est d’écrire tes premières Claude Skills pour arrêter de réexpliquer les mêmes tâches répétitives, voir le module dédié dans la boîte à outils.

*Parcours Designer · tutoriel 2/3 · ~35 min*

## Vibe coding, tester ce que tu construis avec Playwright

Le complément obligatoire du tutoriel précédent, parce que du code qui "a l’air" de marcher n’est pas forcément du code qui marche : Playwright le vérifie dans un vrai navigateur.

**Prérequis :** Avoir terminé le tutoriel 1, une application qui tourne en local (ex. localhost:3000).

### Comprendre pourquoi ce tutoriel existe

Playwright est un framework de test qui pilote un vrai navigateur (Chromium, Firefox, WebKit) et vérifie ce qui s’affiche réellement à l’écran. Sans lui, tu demandes à Claude Code de construire un formulaire, il t’assure que c’est fait, et la seule façon de savoir si c’est vrai est de tester toi-même à la main, écran par écran. Avec Playwright branché à Claude Code, c’est Claude qui ouvre le navigateur, clique, remplit, et te dit ce qu’il a observé.

### Installer le serveur MCP Playwright

Une seule commande depuis ton terminal, dans le dossier de ton projet Claude Code :

```bash
claude mcp add playwright npx @playwright/mcp@latest
```

Redémarre Claude Code. Le serveur lit l’arbre d’accessibilité de la page au lieu de prendre des captures d’écran, ce qui va plus vite et produit des sélecteurs stables, alors que des clics aux coordonnées cassent au moindre changement visuel.

### Vérifier que la connexion fonctionne

Demande simplement, en langage naturel :

```text
Ouvre https://demo.playwright.dev/todomvc et
ajoute trois tâches à la liste.
```

Si Claude ouvre effectivement un navigateur et manipule la page, la connexion est bonne. Passe à ton propre projet.

### Le premier vrai test : ton propre parcours utilisateur

Décris le parcours à vérifier en une phrase précise, sans écrire toi-même de code de test :

```text
Ouvre mon app sur localhost:3000, remplis le
formulaire d'inscription avec un email de test,
soumets-le, et vérifie que le message de
confirmation s'affiche.
```

Claude gère les sélecteurs, les temps d’attente, les vérifications, et te renvoie un rapport étape par étape de ce qu’il a constaté, succès ou échec.

### Tester le responsive

Par défaut, Claude teste en desktop. Précise les largeurs d’écran explicitement si tu veux couvrir mobile et tablette :

```text
Teste le menu de navigation à 375px, 768px
et 1440px de large.
```

### Transformer une exploration en test réutilisable

Une fois qu’une vérification décrite en une phrase fonctionne bien, demande à Claude de générer le code de test correspondant, que tu pourras relancer automatiquement à chaque changement futur sans repasser par une conversation.

> ⚠️ **Point de vigilance.** Tout ce que Claude voit à travers Playwright MCP (contenu de page, console, données de formulaire) part vers l’API Anthropic pour être traité. Réserve cet usage aux environnements de développement avec des données de test, jamais à un environnement de production avec de vraies données utilisateur.

> 💡 **Astuce.** Pour des tests répétés en intégration continue plutôt que de l’exploration ponctuelle, Microsoft propose depuis 2026 une variante en ligne de commande de Playwright, plus économe en tokens. Garde le MCP pour explorer et déboguer, la CLI pour les tests qui tournent en boucle.

> 📎 **Ressource.** Playwright MCP, documentation officielle.

*Parcours Designer · tutoriel 3/3 · ~40 min*

## Webflow, de la maquette au site en ligne

Quand ouvrir Webflow au lieu de Claude Code, et comment ne pas livrer un site qui sent le générateur IA à trois kilomètres.

**Prérequis :** Un compte Webflow (l’offre gratuite suffit pour ce tutoriel), une idée claire de ton contenu.

### Décider si Webflow est le bon outil

Règle simple : un site vitrine, une landing page, un portfolio → Webflow. Un produit avec une vraie logique applicative (comptes utilisateurs, logique métier complexe) → Claude Code, comme au tutoriel 1. Les deux se combinent bien : beaucoup d’équipes montent la vitrine sur Webflow et codent le produit qui est derrière.

### Générer un premier jet avec l’AI Site Builder

Depuis ton espace Webflow, choisis "AI Site Builder" et décris ton activité aussi précisément que possible : nom, ce que tu fais, ton audience, les pages dont tu as besoin. Plus le prompt de départ est précis, plus la structure générée est exploitable telle quelle. Tu obtiens un site multi-pages avec un vrai système de design derrière, pas une maquette figée.

### Reprendre la main dans le Designer

Le site généré repose sur Flowkit, le système de design modulaire de Webflow : composants, variables, styles réutilisables. Ajuste les couleurs, la typographie et l’espacement à ta charte plutôt que de garder les réglages par défaut, c’est ce qui différencie un site qui a l’air pensé d’un site qui a l’air généré.

### Remplacer systématiquement le contenu générique

Le point faible de tous les générateurs IA de site, sans exception : le texte reste générique et les images restent des placeholders. Ne publie jamais un site sans être passé sur chaque section pour remplacer la copie par tes vrais mots, c’est repérable au premier coup d’œil sinon, et ça décrédibilise tout le reste du travail.

### Connecter le CMS à tes automatisations

Si le site a besoin de contenu qui change régulièrement (articles, études de cas), configure les collections CMS puis connecte-les à N8N ou Zapier : un nouvel article publié peut par exemple déclencher un post LinkedIn automatique, sans ticket ni intervention manuelle.

### Vérifier avant de publier

Teste sur mobile, vérifie que chaque formulaire envoie bien ses données quelque part, contrôle la vitesse de chargement des images. C’est le moment de rappeler le tutoriel précédent : si le site embarque une brique applicative testable, Playwright peut vérifier ce parcours pour toi avant la mise en ligne.

> ⚠️ **Point de vigilance.** L’éditeur historique de Webflow (le "legacy Editor") ferme le 4 août 2026. Si ton équipe ou toi passez encore par lui pour les mises à jour de contenu au quotidien, planifie la bascule vers la nouvelle expérience d’édition avant cette date.

> 📎 **Ressource.** Webflow AI Site Builder.

## Parcours 2 · Com & Marketing

Le volume de contenu à produire ne baisse jamais, l’équipe si. Trois tutoriels pour construire l’infrastructure qui absorbe le volume sans y laisser tes soirées : organisation, production visuelle, diffusion.

1. N8N + Notion/Airtable
2. Higgsfield à l’échelle
3. Landing pages

*Parcours Marketing · tutoriel 1/3 · ~35 min*

## S’organiser avec N8N, Notion et Airtable

Le trio qui remplace le tableur partagé illisible et les briefs perdus dans Slack : Notion pour la doc, Airtable pour le suivi, N8N pour relier les deux.

**Prérequis :** Un compte Notion, un compte Airtable (les offres gratuites suffisent pour démarrer).

### Comprendre pourquoi ce ne sont pas deux outils interchangeables

Notion est un espace de documents avant d’être une base de données : c’est là que vivent les briefs, les guides de style, les comptes-rendus, tout ce qui se lit comme du texte. Airtable est une vraie base de données relationnelle déguisée en tableur : c’est là que vivent le calendrier de contenu, le suivi de statut, les données structurées qui doivent rester fiables et filtrables. Le schéma qui revient le plus souvent chez les équipes marketing : Notion pour la connaissance, Airtable pour l’opérationnel.

### Construire ta base Airtable de calendrier de contenu

Décris ton besoin en langage naturel à Omni, l’assistant conversationnel d’Airtable, plutôt que de construire les tables à la main :

```text
Je veux suivre mes contenus marketing avec :
titre, canal, statut (idée / brief / en cours /
prêt / publié), date de publication, personne
assignée, et un lien vers le brief Notion.
```

Tu obtiens une base fonctionnelle en quelques minutes, à ajuster ensuite avec les champs et vues qui te manquent (vue calendrier, vue par canal).

### Construire ton espace Notion de briefs

Une page par campagne, avec un gabarit fixe : objectif, audience, ton, contraintes, deadline. C’est ce document que toute personne de l’équipe, ou tout pipeline automatisé, vient lire pour comprendre le contexte avant de produire quoi que ce soit.

### Connecter les deux avec N8N

Construis un premier workflow simple : quand une nouvelle page de brief est créée dans Notion, une ligne correspondante apparaît automatiquement dans ton calendrier Airtable, pré-remplie avec le titre et la date. Plus besoin de dupliquer l’information à la main entre les deux outils.

### Ajouter une étape d’intelligence dans le pipeline

Une fois la mécanique de base posée, ajoute un nœud IA qui lit le brief et propose automatiquement une catégorie, un ton, et trois angles de titres possibles, directement dans le champ Airtable correspondant, prêt à être validé par un humain plutôt que produit de zéro.

### Garder une étape de validation humaine

Rien ne doit partir en production sans qu’une personne l’ait vu passer. Ajoute une notification Slack ou email avant toute action finale (publication, envoi), parce que la régularité gagnée par l’automatisation ne vaut rien si elle publie aussi vite ses erreurs que ses réussites.

> 💡 **Astuce.** Ne construis pas Notion et Airtable en parallèle dès le premier jour. Commence par un seul, sers-t’en deux semaines, et ajoute le second seulement quand la limite du premier devient concrètement gênante, tu sauras alors exactement quoi lui demander.

> 📎 **Ressource.** Airtable, AI agent software · N8N, AI agents.

*Parcours Marketing · tutoriel 2/3 · ~35 min*

## Génération visuelle à l’échelle avec Higgsfield

Un porte-parole ou une identité de campagne, décliné en dizaines de visuels cohérents, sans reprogrammer un shooting à chaque déclinaison.

**Prérequis :** Un compte Higgsfield, entre 20 et 30 photos de référence de haute qualité (personne réelle ou mannequin, avec les droits d’usage).

### Définir l’identité avant d’ouvrir l’outil

Choisis qui incarne la campagne : un vrai porte-parole de marque, un mannequin sous licence, ou un personnage entièrement fictif. Cette décision a des implications légales et de communication, tranche-la avant de lancer le moindre entraînement.

### Entraîner Soul ID

Dans Higgsfield, section Characters, importe 20 à 30 photos : plusieurs angles de visage, éclairage cohérent, rien qui masque les traits (pas de lunettes de soleil, pas de chapeau qui cache le front). L’entraînement prend 3 à 5 minutes. Nomme l’identité pour la retrouver facilement ensuite.

### Générer une première série de test

Avant de lancer une vraie production, teste ton identité sur 3 styles différents (preset éditorial, preset lifestyle, plan large) pour vérifier que la cohérence tient. Attends-toi à "clairement la même personne" plutôt qu’à du pixel identique, c’est le niveau de fidélité normal.

### Construire un pipeline de production en masse

Connecte Higgsfield à N8N (support MCP natif) pour industrialiser : un brief de campagne entre, une série de déclinaisons visuelles sort, un visuel par format, par canal, avec la même identité verrouillée sur chacun.

### Contrôle qualité avant diffusion

Passe chaque lot généré en revue avant publication : les scènes d’action ou de mouvement rapide restent le point faible de la cohérence de visage, privilégie les scènes posées pour ta production récurrente et réserve les tests plus ambitieux à des allers-retours de validation.

> ⚠️ **Point de vigilance.** Les visuels générés embarquent un marquage de provenance (C2PA). Vérifie les obligations de divulgation IA de chaque plateforme où tu publies en contexte publicitaire, les règles varient déjà selon les régions et se durcissent.

> 📎 **Ressource.** Soul ID, Higgsfield.

> 💸 **Sans abonnement Higgsfield ?** La méthode reste la même (identité définie avant l'outil, série de test, contrôle qualité). Les outils qui peuvent prendre le relais, et leurs licences : [Alternatives à Higgsfield](../veille/alternatives-higgsfield.md).

*Parcours Marketing · tutoriel 3/3 · ~30 min*

## Sites & landing pages : Webflow et les alternatives rapides

Cadrer l’objectif de conversion avant d’ouvrir un outil, puis choisir entre Webflow et une option plus rapide selon l’enjeu réel de la page.

**Prérequis :** Avoir défini l’offre ou le message de la campagne (le tutoriel 1 t’y aide).

### Cadrer l’objectif avant tout

Une seule question compte avant d’ouvrir un outil : que doit faire le visiteur sur cette page (s’inscrire, acheter, réserver un appel) ? Tout le reste (structure, ton, longueur) en découle. Une landing page sans objectif de conversion unique convertit toujours moins bien qu’une page qui n’en vise qu’un.

### Webflow pour une page complète, connectée au CMS

Si la campagne dure et doit évoluer (nouvelles offres, nouveaux témoignages), pars sur Webflow : la logique de génération et de personnalisation avec l’AI Site Builder est la même que dans le tutoriel dédié du parcours Designer.

### Une alternative pour un one-pager rapide

Pour une page de campagne courte, qui ne vivra que quelques semaines, un outil comme Framer permet d’aller du prompt à une page publiée en une seule session, avec une courbe d’apprentissage plus légère que Webflow, au prix d’un contrôle plus limité sur le CMS et la structure long-terme.

### Connecter analytics et formulaire

Avant de considérer la page terminée : vérifie que chaque soumission de formulaire arrive bien quelque part (Airtable, CRM), et que le tracking de conversion est actif. Une belle page qui ne mesure rien ne permet aucune décision derrière.

### Prévoir une boucle de test simple

Change une seule variable à la fois (le titre, l’image ou le bouton d’action) : c’est la seule façon de savoir, plus tard, ce qui a réellement fait la différence.

> 💡 **Astuce.** Confie à l’IA le squelette et la structure, jamais le texte final tel quel : la copie générée reste générique et se repère à l’œil nu. Réécris chaque titre et chaque accroche dans ta propre voix avant publication.

## Parcours 3 · Business Instagram

Tu es le produit, la marque et l’équipe de contenu à toi seul·e. Trois tutoriels pour construire un système (identité, production, méthode) plutôt que de courir après l’algorithme un post à la fois.

1. Identité visuelle
2. Pipeline de contenu
3. La méthode 2026

*Parcours Instagram · tutoriel 1/3 · ~30 min*

## Construire une identité visuelle cohérente avec Higgsfield

Le même visage, la même vibe, sur des dizaines de posts, sans reprendre une séance photo chaque semaine.

**Prérequis :** Un compte Higgsfield, 20 à 30 photos de toi-même (ou de ton personnage de marque), bien éclairées.

### Choisir tes photos de référence

La qualité de départ détermine presque tout le résultat. Vise 20 à 30 photos avec un éclairage cohérent (naturel de préférence), plusieurs angles de visage (face, trois-quarts, profil), sans lunettes de soleil ni chapeau qui masque les traits. Un jeu de photos faible donne systématiquement une identité faible, n’essaie pas de compenser ça après coup.

### Entraîner ton Soul ID

Dans la section Characters de Higgsfield, importe tes photos et lance l’entraînement (3 à 5 minutes). Donne un nom clair à ton identité, tu la retrouveras à chaque génération future sans avoir à réimporter quoi que ce soit.

### Tester avant de produire en volume

Génère 3 à 5 visuels dans des styles différents et compare : est-ce clairement toi sur chacun ? Les scènes posées ou à mouvement lent donnent les meilleurs résultats de cohérence, garde les scènes d’action pour plus tard, une fois l’identité bien calibrée.

### Construire ta bibliothèque de presets récurrents

Choisis 3 à 4 styles ou ambiances que tu vas réutiliser en boucle (ex : lumière naturelle pour le lifestyle, fond neutre pour l’expertise, plan large pour les coulisses). Un feed reconnaissable vient autant de cette répétition volontaire que de ton visage lui-même.

### Connaître les limites

Deux limites à intégrer dès maintenant : la cohérence baisse sur les mouvements rapides, et deux personnes qui interagissent dans un même visuel restent un point faible général de ces outils en 2026, pas seulement de Higgsfield. Prévois tes scènes en conséquence, sans forcer un rendu qui ne viendra pas.

> 📎 **Ressource.** Soul ID, Higgsfield.

> 💸 **Sans abonnement Higgsfield ?** Les photos de référence et les tests restent valables avec d'autres outils : [Alternatives à Higgsfield](../veille/alternatives-higgsfield.md), du gratuit en ligne à l'installation locale.

*Parcours Instagram · tutoriel 2/3 · ~35 min*

## Construire ton pipeline de contenu avec N8N & Airtable

De l’idée griffonnée sur le pouce au post publié, sans que chaque publication te prenne une soirée entière.

**Prérequis :** Avoir terminé le tutoriel 1 (ton identité Soul ID), un compte Airtable, un compte N8N.

### Construire ta base Airtable

Une table simple suffit pour démarrer : idée, statut (brute / en écriture / prête / publiée), date prévue, format (Reel, carrousel, photo), lien vers le visuel final, et une colonne performance à remplir après publication. Si tu veux gagner du temps, décris-la à Omni et laisse-le la générer.

### Noter l’idée brute, sans la travailler

Un titre, une phrase, une note vocale transcrite, dans Airtable directement. Le perfectionnisme à cette étape précise est ce qui tue le plus sûrement la régularité de publication.

### Construire le pipeline N8N : idée → script → légende

Un déclencheur (nouvelle ligne Airtable) → un nœud IA qui développe l’idée brute en angle et en script court, dans ton ton, idéalement à partir d’une Skill ou d’un prompt entraîné sur tes propres meilleurs posts, pas un ton IA générique.

### Brancher la génération visuelle

Connecte Higgsfield à la suite du pipeline : le script généré déclenche la production du visuel avec ton identité Soul ID, cohérent avec le reste de ton feed sans intervention manuelle supplémentaire.

### Garder une étape de relecture humaine, et une part de brut

Le pipeline te sert pour la structure et la régularité ; ne le laisse jamais publier sans relecture. Et retiens ce point pour le tutoriel suivant : lisse trop, et le contenu perd exactement ce qui le rend partageable en 2026.

### Suivre la performance dans Airtable

Après chaque publication, note ce qui a bien fonctionné, en particulier les partages en DM, le signal qui compte le plus désormais. Cette colonne devient, avec le temps, la meilleure source d’idées pour les posts suivants.

> 💡 **Astuce.** Commence avec un pipeline qui produit un brouillon, pas un post fini. La dernière passe (relecture, ajustement du ton, décision finale) reste la tienne ; c’est elle qui différencie ton compte des dizaines d’autres qui tournent sur le même type d’automatisation.

*Parcours Instagram · tutoriel 3/3 · ~35 min*

## Ce qui marche vraiment sur Instagram en 2026

Une méthode, sans outil cette fois : comment l’algorithme classe réellement le contenu, comment construire un ton reconnaissable, et ce qu’il faut arrêter de faire.

### Comprendre ce que l’algorithme regarde vraiment

Adam Mosseri, le responsable d’Instagram, a confirmé trois signaux principaux : le temps de visionnage, les likes rapportés à la portée, et les partages en message privé, ces derniers pesant 3 à 5 fois plus lourd que les likes pour la diffusion des Reels. Cent likes comptent moins que dix partages en DM : un partage privé est interprété comme un vrai signal de confiance, quelqu’un qui met sa crédibilité en jeu en envoyant ton contenu à un ami.

### Connaître le système d’audition

Chaque nouveau post est d’abord montré à un petit groupe de non-abonnés. S’il performe bien auprès de ce groupe test, il est poussé à une audience de plus en plus large ; s’il ne performe pas, il est freiné avant même d’atteindre tes propres abonnés. Conséquence directe : les deux à trois premières secondes de chaque post décident de tout. "Salut tout le monde" est le pire départ possible : commence par le résultat, une affirmation forte, ou une rupture visuelle.

### Utiliser les Trial Reels pour tester sans risque

Cette fonctionnalité montre un Reel à des non-abonnés avant de le publier sur ton profil principal. Si un format ou un sujet inhabituel te fait hésiter, teste-le en Trial Reel d’abord : s’il performe auprès d’une audience froide, c’est ton feu vert pour le publier plus largement, sans avoir pris de risque sur la perception de ton audience existante.

### Construire un tone of voice reconnaissable, méthode concrète

Reprends tes 15 à 20 posts qui ont le mieux performé. Note pour chacun : la structure de la phrase d’accroche, les mots que tu répètes naturellement, ce que tu n’écrirais jamais. Tu obtiens, loin de l’exercice abstrait de "trouver sa voix", un inventaire de tes tournures réelles que tu peux ensuite donner en exemple à une Skill ou à un pipeline IA, pour que ce qu’il génère te ressemble au lieu de sonner comme n’importe quel autre compte IA-assisté.

### Appliquer la formule de partage avant de publier

Une question simple avant chaque publication : quelqu’un enverrait-il ça à un ami, et pourquoi ? Les quatre raisons qui poussent réellement au partage en DM : c’est utile, c’est drôle, ça donne raison à quelqu’un, ou ça déclenche un léger désaccord. Si tu ne trouves pas de réponse claire à cette question, le post a de bonnes chances de rester à l’intérieur de ta bulle d’abonnés déjà acquis.

### Ce qu’il faut arrêter de faire

Le bourrage de hashtags ne sert plus la découverte comme avant, les hashtags ne permettent même plus de "suivre" un sujet. Le contenu recyclé depuis un autre réseau (en particulier avec son filigrane visible) est activement pénalisé. Et surtout, contre-intuitif mais confirmé par Instagram lui-même : à mesure que l’IA rend le contenu parfaitement poli trivial à produire pour tout le monde, c’est le contenu qui a l’air brut et humain qui se distingue. Tes outils servent la régularité et la structure, ils ne doivent jamais lisser ce qui rend ta voix reconnaissable.

### Mesurer ce qui compte, pas ce qui rassure

Suis dans ta base Airtable (tutoriel précédent) les partages en DM et le taux de rétention plutôt que le seul nombre de likes. Ce sont ces deux métriques, pas ton nombre d’abonnés, qui prédisent aujourd’hui si Instagram va pousser ton prochain post au-delà de ta bulle actuelle.

> ⚠️ **Point de vigilance.** Aucun de ces signaux n’est figé : Instagram ajuste son système en continu, et ce qui est vrai en juillet 2026 ne le sera pas nécessairement dans un an. Reviens vérifier les dernières annonces d’Adam Mosseri plutôt que de traiter cette méthode comme définitive.

> 📎 **Ressource.** Instagram algorithm tips for 2026 (Hootsuite) · Instagram Algorithm Updates 2026 (MeetEdgar).

## Sources vérifiées

Chaque commande, chaque affirmation technique de ces neuf tutoriels a été vérifiée sur une documentation officielle en juillet 2026. Les interfaces changent vite, si une commande ne fonctionne plus telle quelle, la doc officielle est toujours le bon réflexe avant de chercher plus loin.

### Claude Code & Playwright

- [Not all AI-assisted programming is vibe coding](https://simonwillison.net/2025/Mar/19/vibe-coding/) · simonwillison.net
- [Playwright MCP, documentation officielle](https://playwright.dev/docs/getting-started-mcp) · playwright.dev

- [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) · github.com

### Webflow

- [Webflow AI Site Builder](https://webflow.com/ai-site-builder) · webflow.com
- [Webflow AI overview](https://help.webflow.com) · help.webflow.com

### Organisation & données

- [Airtable, AI agent software](https://www.airtable.com) · airtable.com
- [N8N, AI agents](https://n8n.io/ai-agents/) · n8n.io

### Higgsfield

- [Soul ID, Higgsfield](https://higgsfield.ai) · higgsfield.ai

### Instagram & algorithme

- [Instagram algorithm tips for 2026](https://blog.hootsuite.com/instagram-algorithm/) · blog.hootsuite.com
- [Instagram Algorithm Updates 2026](https://meetedgar.com/blog) · meetedgar.com

Aucun de ces neuf tutoriels ne vaut quoi que ce soit tant que tu ne l’as pas fait tourner toi-même, une fois, sur un vrai projet. Choisis le premier de ton parcours, ouvre l’outil en même temps que ce document, et avance étape par étape plutôt que de tout lire d’une traite.

**Ailleurs dans la Toolbox**

- Pourquoi ces outils et pas d'autres → [La boîte à outils IA](../guides/boite-a-outils-ia.md)
- n8n chez toi plutôt que dans le cloud → [Installer n8n avec Docker](./installer-n8n-docker.md)
- Les prompts d'image commentés et les angles photo → [Ressources IA générative](../guides/ressources-ia-generative.md)
- Quoi publier, et quand → [Le système de contenu ACRV](../guides/strategie-contenu.md)
- Vérifier ce que Claude Code dit avoir fait → [Prompt maître du harnais](../prompts/prompt-maitre-harnais.md)

---

*Tutoriels conçus sur-mesure · Sources vérifiées en juillet 2026 · Les outils et commandes cités évoluent vite, retourne à la documentation officielle pour toute donnée sensible au temps.*
