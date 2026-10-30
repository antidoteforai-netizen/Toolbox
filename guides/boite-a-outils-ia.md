# La boîte à outils IA

**Arrête de collectionner les outils IA et commence à t’en servir.**

Ce document te dit précisément quoi faire avec Claude Code, les Skills, Figma, Webflow, Higgsfield, N8N et Airtable, que tu t’en serves déjà tous les jours ou que tu n’aies encore jamais ouvert aucun d’entre eux. Les sept outils y sont répartis selon trois profils, sans le blabla générique sur "l’IA qui va tout changer".

## Sommaire

- [Tu te reconnais ?](#tu-te-reconnais-)
- [Trois profils, un seul document](#trois-profils-un-seul-document)
- [Trois notions avant de foncer](#trois-notions-avant-de-foncer)
- [Ce que les sept outils font vraiment pour toi](#ce-que-les-sept-outils-font-vraiment-pour-toi)
- [Claude Code & vibe coding](#claude-code--vibe-coding)
- [Claude Skills](#claude-skills)
- [Figma & Figma Make](#figma--figma-make)
- [Webflow](#webflow)
- [Higgsfield](#higgsfield)
- [N8N](#n8n)
- [Airtable](#airtable)
- [Les outils combinés, pas juste listés](#les-outils-combinés-pas-juste-listés)
- [Du brief au prototype cliquable](#du-brief-au-prototype-cliquable)
- [Du brief à la campagne multi-format](#du-brief-à-la-campagne-multi-format)
- [De l’idée au post publié](#de-lidée-au-post-publié)
- [Le cheat-sheet, pour plus tard](#le-cheat-sheet-pour-plus-tard)
- [Sources vérifiées](#sources-vérifiées)

## Tu te reconnais ?

Avant de te donner un seul outil ou une seule méthode, fais une vérification rapide. Si rien ici ne te parle, ferme cette page, elle n’est pas pour toi ; si tout te parle, continue, c’est pour ça qu’elle existe.

1. Tu vois passer douze nouveaux outils IA par semaine sur LinkedIn, et t’as l’impression de prendre du retard, alors que tu te sers déjà de la moitié d’entre eux tous les jours sans le formaliser.
2. On te demande trois fois plus de contenu qu’il y a un an, avec la même équipe, "parce que l’IA fait gagner du temps", sauf que personne ne t’a montré comment, précisément.
3. Tu postes tous les jours, tu suis tous les conseils qu’on te donne, et ta portée stagne pendant que des comptes bien moins soignés que le tien explosent.
4. T’as testé six outils IA différents ce mois-ci et tu ne t’en sers plus que de deux, sans savoir dire pourquoi ceux-là et pas les autres.
5. Tu sais, quelque part, que tu devrais construire un vrai système plutôt que d’empiler des prompts au coup par coup, mais tu n’as jamais le temps de t’arrêter pour le faire proprement.

## Trois profils, un seul document

Personne ne lit un document de ce genre du début à la fin, et c’est très bien comme ça. Chaque outil ci-dessous précise à qui il parle le plus ; chaque astuce est taguée par profil. Trouve le tien, saute directement dedans depuis le menu, reviens piocher ailleurs quand tu veux.

### Product Designer & Builder

Tu designs des produits, tu prototypes, tu codes un peu ou beaucoup. L’IA t’intéresse comme matériau de travail, pas comme gadget.

- Claude Code, vibe coding, Skills
- Figma Make, prototypage IA-natif
- Webflow pour livrer vite

### Com & Marketing

Tu produis des campagnes, des contenus, des assets, pour une marque, une équipe, des clients. Le volume ne baisse jamais, le temps si.

- Pipelines de production (N8N, Airtable)
- Génération visuelle à l’échelle (Higgsfield)
- Sites et landing pages (Webflow)

### Business Instagram

Tu es le produit, la marque et l’équipe de contenu à toi seul·e. Tu as besoin de systèmes, pas de plus d’heures dans la journée.

- Identité visuelle cohérente (Higgsfield)
- Pipeline de contenu (N8N + Airtable)
- Ce qui marche vraiment sur Instagram en 2026

Cette ressource n’est pas pour toi si tu cherches une explication de ce qu’est ChatGPT, ou si l’idée de coller un prompt dans une interface te terrifie encore. Il existe d’excellents contenus gratuits pour ce niveau-là, celui-ci part du principe que tu es prêt·e à agir, pas juste à comprendre.

## Trois notions avant de foncer

Si tu vis déjà dans Claude Code au quotidien, saute cette section entière et va directement aux outils. Si certains des sept outils de ce document te sont inconnus, ces trois blocs te donnent le vocabulaire commun qui revient partout dans la suite, cinq minutes de lecture, pas plus.

### Un bon prompt, en vrai

Un prompt qui marche donne assez de contexte pour qu’il n’y ait plus qu’une seule bonne façon de comprendre la demande, et qu’il soit "malin" n’y change rien. "Écris-moi un post sur mon produit" est un mauvais prompt, pas parce qu’il est mal formulé, mais parce qu’il manque tout ce qui compte : pour qui, quel ton, quelle longueur, quel objectif. Trois réflexes suffisent pour progresser plus que n’importe quelle liste de 50 templates : donne le contexte avant la demande (qui es-tu, pour qui c’est, ce que tu as déjà essayé) ; donne un exemple du résultat que tu attends plutôt que de le décrire en abstrait ; et itère à voix haute, "trop long, coupe de moitié" fonctionne mieux qu’un nouveau prompt de zéro à chaque fois.

### Outil, agent, Skill : la différence qui évite les malentendus

Un outil, c’est une capacité ponctuelle : générer une image, chercher sur le web, lire un fichier. Un agent, c’est un système qui enchaîne plusieurs étapes tout seul vers un objectif, en décidant lui-même l’ordre et les outils à mobiliser en cours de route ; Claude Cowork ou Manus en sont des exemples grand public. Une Skill (spécifique à Claude) est un mode d’emploi réutilisable que tu écris une fois et que Claude charge automatiquement quand la tâche correspond : la procédure, pas l’action elle-même. Retiens l’essentiel : plus le besoin est répétitif, plus une Skill vaut le coup ; plus la tâche est longue et à plusieurs étapes, plus un agent devient pertinent.

### Texte, image, vidéo : qui fait quoi en 2026

Pour le texte et le raisonnement (rédaction, code, structuration), les modèles de langage comme Claude dominent. Pour l’image fixe, deux familles se distinguent : Nano Banana Pro (Gemini 3 Pro Image, chez Google) excelle sur le texte lisible dans l’image (mockups, posters, infographies), et Higgsfield sur la cohérence d’un même personnage ou visage à travers des dizaines de générations. Pour la vidéo, le paysage bouge vite : Veo 3.1 et Runway Gen-4.5 mènent aujourd’hui, Kling 3.0 reste l’option économique, et Sora, qui dominait les conversations il y a un an, a été mis à l’arrêt par OpenAI en 2026, faute de rentabilité. Retiens la leçon plus que le classement : dans cette catégorie, ne construis jamais un système qui dépend d’un seul fournisseur.

## Ce que les sept outils font vraiment pour toi

Plutôt qu’un classement ou un comparatif générique, chaque outil a droit à quatre rubriques : ce qu’il fait sans le blabla marketing, pourquoi ça compte selon ton profil, comment démarrer si tu ne le connais pas, et des astuces concrètes si tu le connais déjà.

## Claude Code & vibe coding

Un agent qui code dans ton terminal, et une façon de travailler qui change selon que tu livres à un client ou que tu explores un week-end.

#### C’est quoi, sans le blabla

Claude Code est un agent qui travaille directement dans ton terminal ou ton éditeur : il lit ton code, en écrit, exécute des commandes, corrige ses propres erreurs. Le "vibe coding", un terme lancé par Andrej Karpathy début 2025, désigne la pratique consistant à laisser l’IA écrire sans tout relire, pour aller vite sur un prototype jetable. La nuance qui compte, popularisée par le développeur Simon Willison : si tu relis, testes et comprends chaque ligne, ce n’est plus du vibe coding, c’est de la programmation assistée, et c’est la seule des deux approches qu’on peut raisonnablement livrer à un client.

#### Pourquoi ça compte pour toi

- **Designer & Builder** · C’est l’outil qui te fait passer de la maquette au prototype cliquable et fonctionnel dans la même session, sans attendre un développeur pour valider une idée.
- **Com & Marketing** · Une landing page de campagne, un petit outil interne (générateur de visuels, calculateur), un tracker, tu peux les construire toi-même en une aprèm plutôt que d’ouvrir un ticket dev.
- **Business Instagram** · Un site portfolio, une page de capture email, un configurateur simple pour tes offres, sans payer un développeur pour un site à trois pages.

#### Comment démarrer

Installe Claude Code, ouvre un dossier vide, et donne-lui une demande précise plutôt qu’une idée vague : "Crée une landing page avec un formulaire d’inscription email, en Next.js, avec ce texte" fonctionne infiniment mieux que "fais-moi un site". Accepte les premières suggestions, regarde ce qui se passe, corrige à voix haute plutôt que de tout recommencer.

#### Astuces

- 💡 vibe-code pour explorer, relis pour livrer. La règle simple : si un client ou un vrai utilisateur va toucher le résultat, tu relis le code avant d’envoyer, même en diagonale.
- 💡 colle les messages d’erreur tels quels, sans les reformuler. Claude Code s’en sort mieux avec le texte brut de l’erreur qu’avec ta version résumée.
- 💡 un fichier CLAUDE.md à la racine de ton projet, avec tes conventions et le contexte du projet, évite de tout réexpliquer à chaque session.

> 📎 **Ressource.** Not all AI-assisted programming is vibe coding, l’article de référence sur la nuance qui compte.

## Claude Skills

Le moyen d’arrêter de réexpliquer la même chose à Claude chaque semaine.

#### C’est quoi, sans le blabla

Une Skill, c’est un simple fichier texte (SKILL.md) que tu écris une fois (un nom, une description de ce qu’elle fait et du moment où s’en servir, puis des instructions claires) et que Claude charge tout seul dès qu’une tâche correspond. Rien à coder : rédiger une Skill ressemble à écrire une consigne limpide pour un collègue compétent, pas à programmer.

#### Pourquoi ça compte pour toi

- **Designer & Builder** · Une Skill "audit heuristique", une Skill "spec technique à partir d’une maquette", le travail répétitif de chaque nouvelle fonctionnalité devient un système, pas une nouvelle explication à chaque fois.
- **Com & Marketing** · Une Skill "voix de marque" qui relit chaque texte produit par l’équipe et le corrige dans le ton exact de la marque, le genre de cohérence qu’un guide de style PDF de 40 pages n’obtient jamais en pratique.
- **Business Instagram** · Une Skill "légendes dans mon style" entraînée sur tes 20 meilleurs posts : elle écrit dans ta voix, pas dans une voix IA générique reconnaissable à trois kilomètres.

#### Comment démarrer

Repère une tâche que tu refais presque à l’identique au moins une fois par semaine. Écris son nom et une description au format "fait X, à employer quand Y", c’est ce champ qui détermine si la Skill se déclenchera au bon moment. Ajoute un exemple concret du résultat attendu : un bon exemple vaut mieux qu’une longue liste de règles.

#### Astuces

- 💡 si une Skill ne se déclenche jamais toute seule, le problème est presque toujours dans la description, pas dans les instructions.
- 💡 cinq Skills étroites et bien nommées valent mieux qu’une seule Skill "fourre-tout" que tu ne sais plus quand invoquer six mois plus tard.
- 💡 quand une Skill rate, demande directement à Claude d’analyser pourquoi et de reformuler, souvent plus rapide que de deviner seul.

> 📎 **Ressource.** Agent Skills, documentation officielle · Exemples de Skills.

## Figma & Figma Make

Ton outil du quotidien, plus une couche IA qui transforme une maquette en prototype cliquable sans sortir de Figma.

#### C’est quoi, sans le blabla

Figma Make transforme un prompt, ou un frame Figma existant, en prototype interactif et fonctionnel, sans quitter l’environnement Figma : il peut se synchroniser avec ta bibliothèque de styles et tes packages, se connecter à des outils externes via MCP, et propose un plan avant de générer plutôt que de foncer tête baissée. C’est un outil d’exploration et de démonstration, pas un générateur de code de production tel quel.

#### Pourquoi ça compte pour toi

- **Designer & Builder** · Le pont direct entre une maquette statique et une démo qu’un client ou un product manager peut réellement manipuler, en gardant la cohérence avec ton design system.
- **Com & Marketing** · Utile pour prototyper rapidement une landing page ou un flux d’acquisition avant de le passer à Webflow pour la mise en production réelle.

#### Comment démarrer

Pars d’un frame Figma existant plutôt que d’une page blanche, l’outil hérite alors du contexte visuel et colle davantage à ta charte dès le premier essai. Décris l’interaction voulue en une phrase précise ("ce menu déroulant doit afficher ces options") plutôt qu’un vague "rends ça interactif".

#### Astuces

- 💡 une fois le prototype validé, ne t’attends pas à ce qu’il soit "production-ready" tel quel, c’est un outil d’exploration, pas de livraison finale.
- 💡 synchronise ta bibliothèque de composants avant de générer : ça évite l’effet "joli mais générique" que produit l’outil livré à lui-même.

> 📎 **Ressource.** Figma Make.

## Webflow

Le constructeur de site qui ne t’enferme ni dans un template ni dans du code imposé, et qui a désormais sa propre couche IA pour démarrer plus vite.

#### C’est quoi, sans le blabla

Webflow est un constructeur de site visuel qui produit du vrai code propre derrière, avec un gestionnaire de contenus (CMS) et un contrôle fin du design. Son AI Site Builder transforme un prompt en site complet, multi-pages, avec animations et système de design de base, un vrai point de départ, pas un site fini : les textes restent génériques, les images restent des placeholders, et la structure fine reste à construire. Sa fonctionnalité la plus intéressante en 2026 est sans doute l’AEO (l’optimisation pour les moteurs de réponse IA) : des agents qui auditent comment les IA comme ChatGPT ou Perplexity représentent ta marque, et proposent des correctifs.

#### Pourquoi ça compte pour toi

- **Designer & Builder** · Un vrai design system derrière chaque site généré, que tu peux reprendre en main pixel par pixel, contrairement à la plupart des générateurs IA qui produisent du jetable.
- **Com & Marketing** · Des landing pages de campagne que tu peux lancer et itérer toi-même, sans dépendre d’un développeur à chaque changement de texte.
- **Business Instagram** · Un vrai site, portfolio, page de vente, lien en bio, qui ne ressemble pas à un Linktree, pour un coût très inférieur à un développeur freelance.

#### Comment démarrer

Avant de toucher l’IA Site Builder, sache précisément ce que tu veux : tes pages, tes collections de contenu, ton objectif de conversion. Plus le prompt de départ est précis sur ton activité et ton audience, plus le résultat généré est exploitable tel quel.

#### Astuces

- 💡 confie à l’IA le squelette (structure, sections, système de design), pas le texte final : la copie générée reste générique et se repère à l’œil nu.
- 💡 Webflow se connecte à N8N et Zapier : ton CMS peut déclencher des automatisations (nouvel article publié → post LinkedIn généré) sans code.
- 💡 l’éditeur historique de Webflow ferme le 4 août 2026, si ton équipe s’appuie encore dessus pour les mises à jour de contenu, planifie la bascule maintenant.

> 📎 **Ressource.** Webflow AI Site Builder.

## Higgsfield

L’outil qui résout le vrai problème de la génération d’image : garder le même visage, la même identité, d’une génération à l’autre.

#### C’est quoi, sans le blabla

Le problème que tout le monde connaît sans le nommer : tu génères un visuel avec ton visage ou ton personnage de marque, et à la génération suivante, ce n’est plus vraiment la même personne, la mâchoire a changé, les yeux ont dérivé. Higgsfield règle ça avec Soul ID : tu entraînes une identité une seule fois, à partir d’une vingtaine de photos (3 à 5 minutes de traitement), et cette identité reste ensuite verrouillée quel que soit le style ou l’angle demandé. L’outil agrège aussi plusieurs modèles (dont Nano Banana Pro) sous un seul abonnement.

#### Pourquoi ça compte pour toi

- **Business Instagram** · Ton identité visuelle reste reconnaissable sur des dizaines de visuels sans reprendre une séance photo à chaque fois, la base d’une marque personnelle qui se reconnaît au premier coup d’œil dans un feed.
- **Com & Marketing** · Un porte-parole de marque cohérent sur toute une campagne, décliné en dizaines de visuels et de formats, sans reprogrammer un shooting à chaque déclinaison.
- **Designer & Builder** · Des personnages cohérents pour des maquettes qui doivent raconter une histoire (onboarding, cas d’usage) plutôt que des photos de stock interchangeables.

#### Comment démarrer

La qualité des photos de départ détermine presque tout le résultat : une vingtaine de photos avec un éclairage cohérent, plusieurs angles de visage, sans lunettes de soleil ni éléments qui masquent les traits. Un jeu de photos faible donne systématiquement une identité faible.

#### Astuces

- 💡 teste ton identité sur 3 styles différents avant de t’en servir en production, attends-toi à "clairement la même personne", pas à du pixel pour pixel.
- 💡 les scènes d’action ou de mouvement rapide restent le point faible de la cohérence de visage, privilégie les scènes posées ou à mouvement lent pour ton contenu récurrent.
- 💡 les contenus générés embarquent un marquage de provenance (C2PA), vérifie les règles de divulgation IA de ta plateforme avant de publier en contexte commercial.

> 📎 **Ressource.** Soul ID, Higgsfield.

> 💸 **L'abonnement ne se justifie pas pour ton volume ?** [Les alternatives à Higgsfield](../veille/alternatives-higgsfield.md) vont du gratuit dans le navigateur à l'installation sur ta machine, avec les licences à vérifier avant un usage commercial.

## N8N

L’outil qui transforme une suite de tâches manuelles répétées en un système qui tourne pendant que tu fais autre chose.

#### C’est quoi, sans le blabla

N8N est un outil d’automatisation visuel, des nœuds reliés entre eux sur un canevas, avec un vrai bloc "agent IA" capable de raisonner et d’appeler des outils, pas seulement d’enchaîner des étapes fixes. Il se connecte à MCP dans les deux sens : il peut piloter des serveurs MCP existants, et tes propres workflows N8N peuvent devenir un serveur MCP que Claude appelle directement. Concrètement : c’est l’outil qui relie tous les autres de ce document entre eux.

#### Pourquoi ça compte pour toi

- **Com & Marketing** · Un pipeline "brief → contenu → visuel → planification" qui tourne sans intervention manuelle à chaque étape, le levier le plus direct pour absorber plus de volume sans plus d’heures.
- **Business Instagram** · Le système qui transforme une idée de post en brouillon prêt à publier, texte et visuel, sans que chaque post te prenne une heure de travail manuel.
- **Designer & Builder** · Automatiser ce qui ne relève pas du design pur : notifications, synchronisation entre outils, rapports, pour garder ton temps de cerveau disponible sur le travail créatif.

#### Comment démarrer

Ne commence pas par un pipeline complexe. Prends une seule tâche répétitive que tu fais à la main chaque semaine, construis les 2-3 nœuds qui l’automatisent et fais-la tourner une fois de bout en bout, puis complexifie, jamais l’inverse.

#### Astuces

- 💡 ajoute toujours une étape de validation humaine avant publication automatique, un pipeline sans relecture publie aussi vite ses erreurs que ses réussites.
- 💡 teste ton pipeline sur 5 sujets différents plutôt que de peaufiner un seul cas en boucle : c’est en comparant plusieurs sorties que le maillon faible du système devient visible.
- 💡 N8N se branche nativement sur Webflow, Airtable et la plupart des outils de ce document : commence par connecter deux outils dont tu te sers déjà avant d’en ajouter un troisième.

> 📎 **Ressource.** Build custom AI agents with logic & control, n8n.

## Airtable

Un tableur qui pense : chaque cellule peut analyser, générer ou aller chercher de l’info toute seule.

#### C’est quoi, sans le blabla

Airtable reste une base de données relationnelle facile à prendre en main, mais deux ajouts changent la donne : les Field Agents, des champs IA qui peuvent lire un document, chercher sur le web ou générer du contenu directement dans une cellule, et Omni, un assistant conversationnel qui configure tes tables et automatisations à partir d’une simple description en langage naturel. Limite honnête à connaître : les agents natifs d’Airtable restent cantonnés à l’intérieur de ta base, pour aller chercher au-delà (vérifier un statut ailleurs, publier sur un réseau), il faut les brancher à un outil comme N8N.

#### Pourquoi ça compte pour toi

- **Com & Marketing** · Un calendrier de contenu où chaque idée soumise se catégorise, se transforme en 3 titres possibles et se documente toute seule, avant même qu’un humain y touche.
- **Business Instagram** · Un CRM léger pour tes partenariats et collaborations, et un calendrier de contenu qui te dit d’un coup d’œil ce qui est prévu, publié, et ce qui manque cette semaine.
- **Designer & Builder** · Un référentiel de recherche utilisateur ou de composants qui se met à jour et se résume tout seul, plutôt qu’un Notion qui devient illisible après trois mois.

#### Comment démarrer

Décris ton besoin à Omni en langage naturel plutôt que de construire les tables à la main, "je veux suivre mes posts Instagram, avec statut, date et performance" suffit pour obtenir une base fonctionnelle en quelques minutes, à ajuster ensuite.

#### Astuces

- 💡 inclus explicitement les champs pertinents dans tes prompts de Field Agent (avec les accolades {nom du champ}) plutôt que de laisser l’agent deviner le contexte.
- 💡 pour des prompts complexes, demande à l’agent de procéder étape par étape et précise le format de sortie attendu, la régularité du résultat s’améliore nettement.

> 📎 **Ressource.** Airtable, AI agent software.

## Les outils combinés, pas juste listés

Un outil seul ne change pas grand-chose. Voici comment ils s’enchaînent en vrai, pour chacun des trois profils, de l’idée brute jusqu’à la chose publiée ou livrée.

## Du brief au prototype cliquable

Claude Code · Skills · Figma Make · Webflow, de l’idée à un lien qu’on peut envoyer.

1. **Cadre avant de coder.** Une spec d’une page : scénario utilisateur, 3 critères d’acceptation vérifiables, ce qui est explicitement hors scope. Cette seule page t’évite bien des allers-retours.
2. **Pars d’un frame Figma existant.** Génère avec Figma Make plutôt que d’une page blanche, le résultat hérite du contexte visuel et colle à ta charte dès le départ.
3. **Branche un vrai modèle.** Bascule vers Claude Code pour la partie qui doit être réellement intelligente, pas un texte statique qui fait semblant, un vrai appel à l’API avec réponse en streaming.
4. **Polish & déploie.** Corrige les écarts avec ton design system, déploie sur Webflow ou Vercel. Un lien imparfait envoyé aujourd’hui vaut mieux qu’un lien parfait promis pour la semaine prochaine.
5. **Documente pendant que c’est frais.** Trois phrases sur les décisions prises deviennent, plus tard, la matière d’un case study ou d’un post, capture-les tout de suite plutôt que de compter sur ta mémoire.

## Du brief à la campagne multi-format

Airtable · N8N · Higgsfield · Webflow, un brief qui devient une campagne sans réunion de trois heures.

1. **Le brief atterrit dans Airtable.** Un Field Agent le catégorise, en extrait l’audience, le ton et les contraintes, sans que personne ne remplisse un formulaire à la main.
2. **N8N prend le relais.** Un pipeline génère plusieurs angles de messages et de copy à partir du brief structuré, avec ta Skill "voix de marque" pour garder la cohérence.
3. **Higgsfield produit les déclinaisons visuelles.** Le même porte-parole ou la même identité visuelle, décliné en formats multiples pour chaque canal, sans reprogrammer un shooting.
4. **Webflow héberge la landing page.** Connectée au reste du pipeline pour que les mises à jour de contenu suivent sans ticket dev à chaque changement.
5. **Relecture humaine, puis suivi dans Airtable.** Rien ne part sans validation ; la performance de chaque asset revient nourrir la base pour la campagne suivante.

## De l’idée au post publié

Airtable · N8N · Higgsfield, sans que ça bouffe ta soirée à chaque fois.

1. **Note l’idée brute, sans la travailler.** Un titre, une phrase, dans Airtable ou même une note vocale. Le perfectionnisme à cette étape est ce qui tue la régularité.
2. **N8N structure l’angle et la légende.** À partir de l’idée brute, avec ta Skill "légendes dans mon style" pour éviter le ton IA générique que tout le monde repère désormais.
3. **Higgsfield génère le visuel, avec ton identité Soul ID.** Cohérent avec le reste de ton feed, sans nouvelle séance photo.
4. **Relis, et garde une part de brut.** Point important et contre-intuitif : Instagram privilégie en 2026 le contenu qui a l’air authentique, précisément parce que le contenu parfaitement poli devient trivial à produire pour tout le monde. Sers-toi du pipeline pour la structure et la régularité, pas pour lisser ce qui fait la voix reconnaissable d’une vraie personne.
5. **Publie, puis suis dans Airtable.** Ce qui partage bien (en DM, pas juste en likes) est le signal qui compte le plus pour la distribution en 2026, note-le pour orienter les prochaines idées.

## Le cheat-sheet, pour plus tard

Reviens ici plutôt que de tout relire : une ligne par outil dit ce qu’il fait, pour qui il compte le plus et par où commencer.

| Outil | Ça sert à | Profil principal | Démarre par |
|---|---|---|---|
| Claude Code | Coder avec un agent, du prototype au produit | Designer & Builder | Une demande précise, pas une idée vague |
| Claude Skills | Automatiser une tâche répétitive, dans ta voix | Designer, Marketing | Une description "quoi + quand" claire |
| Figma Make | Maquette → prototype cliquable, sans coder | Designer & Builder | Partir d’un frame existant |
| Webflow | Site ou landing page, vrai code derrière | Les trois profils | Cadrer pages & objectif avant l’IA |
| Higgsfield | Identité visuelle cohérente, génération après génération | Instagram, Marketing | 20 photos de référence, bien éclairées |
| N8N | Relier tous les outils en un pipeline automatisé | Marketing, Instagram | Une seule tâche répétitive à la fois |
| Airtable | Base de données qui pense, calendrier, CRM, suivi | Marketing, Instagram | Décrire le besoin à Omni en langage naturel |

> La règle qui traverse tout ce document : commence petit, une seule tâche répétitive à la fois, mesure ce qui marche et complexifie ensuite, jamais l’inverse.

## Sources vérifiées

Les affirmations techniques de ce document ont été vérifiées en juillet 2026 sur la documentation des éditeurs ou sur une source primaire. Seule exception, la partie Instagram s’appuie sur deux blogs spécialisés, Hootsuite et MeetEdgar, eux-mêmes fondés sur les déclarations d’Adam Mosseri. Les outils évoluant vite, reviens à ces liens plutôt qu’à ce document pour toute donnée sensible au temps.

### Claude, Skills & vibe coding

- [Agent Skills, Claude Platform Docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [anthropics/skills, dépôt public d’exemples](https://github.com/anthropics/skills)
- [Not all AI-assisted programming is vibe coding](https://simonwillison.net/2025/Mar/19/vibe-coding/)

### Figma, Webflow

- [Figma Make](https://www.figma.com/make/)
- [Webflow AI Site Builder](https://webflow.com/ai-site-builder)
- [Webflow AI overview](https://help.webflow.com)

### Génération visuelle

- [Soul ID, Higgsfield](https://higgsfield.ai)
- [Introducing Nano Banana Pro](https://blog.google/technology/ai/nano-banana-pro/)
- What to know about the Sora discontinuation · [help.openai.com](https://help.openai.com)

### Automatisation & données

- [Build custom AI agents with logic & control](https://n8n.io/ai/)
- [Airtable, AI agent software](https://www.airtable.com/platform/ai)

### Instagram & algorithme

- [Instagram algorithm tips for 2026](https://blog.hootsuite.com/instagram-algorithm/) (blog Hootsuite)
- [Instagram Algorithm Updates 2026](https://meetedgar.com/blog/instagram-algorithm-updates) (blog MeetEdgar, mars 2026)

Aucun de ces sept outils ne va "tout changer" tout seul pendant que tu regardes ailleurs. Ce qui change les choses, c'est de choisir un outil et une astuce cette semaine, puis de la mettre en pratique avant d'en lire une nouvelle. Referme cette page, ouvre celui des sept qui te parle le plus, et fais quelque chose avec.

**Ailleurs dans la Toolbox**

- Les mêmes outils en étapes numérotées → [Tutoriels par profil](../tutoriels/tutoriels-par-profil.md)
- n8n installé chez toi en une commande → [Installer n8n avec Docker](../tutoriels/installer-n8n-docker.md)
- Les outils que je n'ai pas retenus ici → [la veille](../veille/), dont [les alternatives à Higgsfield](../veille/alternatives-higgsfield.md)
- Un prompt prêt à l'emploi pour encadrer Claude Code → [Prompt maître du harnais](../prompts/prompt-maitre-harnais.md)

---

*Ressource conçue sur-mesure · Sources vérifiées en juillet 2026 · Les outils, tarifs et fonctionnalités cités évoluent vite, retourne aux liens ci-dessus pour toute donnée sensible au temps.*
