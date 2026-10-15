# Workflow Figma → Webflow (Relume, plan gratuit, site 2 pages)

**Objectif :** construire 2 pages à partir des assets Relume, en partageant un socle de variables commun entre les membres de l'équipe, sur des outils gratuits.

## Prérequis et règle d'or

- **Relume Figma Kit v3.7** : <https://www.figma.com/community/file/1078092050664989246>
- **Composants Webflow gratuits** : <https://www.relume.io/free-components>
- **Style Guide à cloner** : <https://webflow.com/dashboard/sites/clone/relume-library-styleguide>

**Plugins et apps à installer :**

- Côté Figma : un plugin d'export de variables (ex. *Variables Import/Export*, *Design Tokens*) → sort un JSON/CSS.
- Côté Webflow : *Variables Utility* (partage CSV entre projets) et/ou *CSS Variable Importer* (injecte des variables CSS).

> **Règle d'or :** on choisit **un seul système de variables** et on construit **toujours à partir du Style Guide Relume cloné**. On ne greffe pas de variables externes sur un projet vierge (les IDs internes de variables Webflow ne se synchronisent pas autrement).

## Phase 1, Conception (Figma)

1. **Ouvrir le Relume Figma Kit v3.7** et dupliquer le fichier dans ton espace.
2. **Cartographier le "gratuit utilisable".** Parcourir <https://www.relume.io/free-components> et noter quelles sections sont gratuites côté Webflow. Dans Figma, **n'utiliser que les sections Relume qui ont un équivalent gratuit en Webflow**, sinon tu concevras quelque chose que tu ne pourras pas reconstruire gratuitement.
3. **Maquetter les 2 pages** avec ces sections (hiérarchie claire, contenu réaliste).
4. **Définir les tokens** dans Figma (Variables) : typographie, primary, secondary, color schemes. C'est ici qu'on prépare le socle commun.
5. **Exporter les variables** via le plugin Figma → fichier **JSON ou CSS, une collection à la fois** (couleurs, typo, espacements...).

> ⚠️ Le JSON Figma n'entre pas directement dans Webflow. Il sert de **source de vérité** ; le passage concret vers Webflow se fait à la Phase 2.

## Phase 2, Collaboration (socle de variables partagé)

L'idée : une personne crée le socle de variables dans Webflow, puis tout le monde récupère le même socle.

### Étape A, premier passage Figma → Webflow (une seule fois, par 1 personne)

Le format JSON Figma ≠ format Webflow. Trois options, du plus simple au plus manuel :

- **Option 1 (recommandée)** : convertir l'export Figma en **CSS** (`--primary-500: #...;`) puis l'injecter avec l'app **CSS Variable Importer** → crée les variables natives Webflow dans la collection choisie.
- **Option 2** : utiliser le plugin officiel **Figma to Webflow** (sync variables), mais auto-layout obligatoire et **variants non supportés**.
- **Option 3** : saisie manuelle des variables dans le panneau Variables (`V`) de Webflow en recopiant le JSON. Long mais sans dépendance.

### Étape B, partage entre coéquipiers (Webflow → Webflow)

Une fois le socle dans **un** projet Webflow :

1. Installer **Variables Utility**.
2. La personne "source" **exporte chaque collection en CSV** (un export par collection).
3. Chaque coéquipier **importe le CSV** dans son propre projet (cloné depuis le Style Guide Relume).
4. Résultat : tout le monde a le même socle de variables.

> Le CSV Variables Utility est du **Webflow → Webflow uniquement**. C'est l'outil du partage d'équipe, pas du pont depuis Figma.

### Note pragmatique, périmètre retenu

Le socle inclut volontairement :

- **Typographie** : famille(s) de police + **H1, H2, H3** (tailles, graisses, line-heights).
- **Color schemes** : les schémas de couleurs complets (primary, secondary, neutres + leurs déclinaisons par scheme).

C'est précisément ce périmètre qui rend l'étape **chronophage** : chaque niveau de titre et chaque scheme se règle individuellement, puis se rebranche sur les bonnes variables. À assumer dès le départ et à chiffrer dans le temps de l'exercice, c'est la partie la plus longue du workflow, mais aussi celle qui démontre le mieux la maîtrise du design system.

## Phase 3, Développement (Webflow)

1. **Cloner le Style Guide Relume** : <https://webflow.com/dashboard/sites/clone/relume-library-styleguide> → fondation Client-First : classes globales/utilitaires + variables + CSS embed. **Ne rien supprimer.**
2. **Importer le socle de variables** (CSV via Variables Utility, cf. Phase 2-B).
3. **Reconstruire les pages** : depuis <https://www.relume.io/free-components>, **copier-coller les sections gratuites** une par une dans Webflow (le copier-coller n'est pas bridé sur le gratuit), en suivant la maquette Figma.
4. **Brancher les variables sur les styles** dans le panneau de droite :
   - Sélectionner un **H2** dans l'éditeur visuel → champ **Color** → choisir la variable d'un color scheme.
   - Champ **Font** → choisir la variable `font-family`.
   - Idem pour backgrounds, boutons, textes courants.
5. **Ordre malin pour éviter les doublons de classes** (Class Sync est payant) : **coller TOUTES les sections d'abord, PUIS brancher/ajuster les variables.** Comme tout pointe vers les mêmes variables, une seule modif se propage partout.
6. **Publier** sur le sous-domaine `.webflow.io` (2 pages max sur le plan gratuit).

## Récapitulatif des outils par maillon

| Maillon | Outil | Format |
|---|---|---|
| Concevoir | Relume Figma Kit v3.7 | Figma |
| Définir les tokens | Variables Figma + plugin d'export | JSON / CSS |
| Figma → Webflow (1ʳᵉ fois) | CSS Variable Importer **ou** plugin Figma to Webflow | CSS / sync |
| Partage entre coéquipiers | Variables Utility | CSV |
| Construire | Clone Style Guide Relume + free components | copier-coller |
| Brancher les styles | Panneau Variables Webflow (`V`) | natif |

## Pièges à connaître

- **Class Sync = payant.** Contournement : coller d'abord, personnaliser ensuite.
- **Variables Utility = CSV, pas JSON**, et Webflow ↔ Webflow seulement.
- **Plugin Figma to Webflow** : auto-layout obligatoire, variants non gérés, 1 collection/mode à la fois, pas sur Safari.
- **Ne pas mélanger** sync Figma → Webflow ET style guide Relume sur le même projet → doublons de classes/variables ingérables sans Class Sync.
- **Plafond réel = Webflow gratuit** : 2 pages, sous-domaine `.webflow.io`, pas de domaine custom.
