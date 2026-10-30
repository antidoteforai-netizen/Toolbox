<sub>[Toolbox](../README.md) › [Veille](./README.md) › Alternatives à Higgsfield</sub>

# Alternatives à Higgsfield

**Générer des images et des vidéos sans abonnement, ou en ne payant que ce que vous consommez.**

Je me sers de Higgsfield pour une raison précise, garder le même visage d'une image à l'autre, et je raconte ce choix dans [mon parcours de MidJourney à Higgsfield](../guides/ressources-ia-generative.md#phase-3-higgsfield-aujourdhui--payant). L'abonnement commence à 19 € par mois (formule Starter, 270 crédits) et la formule gratuite est limitée. Il est de trop si vous générez peu, si vous voulez que vos images restent sur votre machine ou si vous préférez payer à l'usage. Cette page range les solutions de remplacement selon leur profondeur, c'est-à-dire ce qu'elles vous demandent d'installer, de payer et de comprendre.

*Vérifié le 30 octobre 2026 : chaque lien ouvert, chaque licence lue dans son fichier officiel, chaque offre gratuite relue sur la page de l'éditeur. Le détail est dans les [sources](#sources).*

## Sommaire

- [Quatre choses à savoir avant de choisir](#quatre-choses-à-savoir-avant-de-choisir)
- [Profondeur](#profondeur)
- [Ce que fait Higgsfield, et où le retrouver](#ce-que-fait-higgsfield-et-où-le-retrouver)
- [Niveau 1 · Dans le navigateur](#niveau-1--dans-le-navigateur)
- [Niveau 2 · Installé sur votre machine](#niveau-2--installé-sur-votre-machine)
- [Niveau 3 · Studios pro et API](#niveau-3--studios-pro-et-api)
- [Sur Mac (Apple Silicon)](#sur-mac-apple-silicon)
- [Par où commencer](#par-où-commencer)
- [Sources](#sources)
- [Ailleurs dans la Toolbox](#ailleurs-dans-la-toolbox)

## Quatre choses à savoir avant de choisir

1. **Open Higgsfield AI s'appelle maintenant Open Generative AI.** L'ancienne adresse du dépôt redirige vers [Anil-matcha/Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI), sous licence MIT. Téléchargez l'appli depuis la page Releases de ce dépôt, celui de son auteur, plutôt que depuis une copie.
2. **Le code est gratuit, la génération dans le cloud ne l'est pas.** La version web et les modèles en ligne (plus de 600 annoncés) passent par l'API Muapi, payée à l'usage avec une clé. Depuis la version 2.0 de mai 2026, l'appli de bureau sait aussi générer en local, sans clé : les images sur Mac avec son moteur intégré, la vidéo seulement sur un ordinateur équipé d'une carte graphique NVIDIA ou AMD.
3. **Le gratuit et illimité existe, il se paie en matériel et en temps.** Un modèle open-source installé chez vous ne coûte rien par image, à condition d'avoir assez de mémoire, d'espace disque (LTX Desktop demande 100 Go libres) et de patience.
4. **Open-source ne veut pas dire libre pour un usage commercial.** Avant de livrer un visuel à un client, lisez la licence du modèle : celle de HunyuanVideo exclut l'Union européenne, les versions [dev] de FLUX interdisent l'usage commercial, et LTX-2 devient payant pour les entreprises à partir de 10 millions de dollars de chiffre d'affaires annuel. Le tableau du [niveau 2](#niveau-2--installé-sur-votre-machine) reprend chaque cas.

## Profondeur

### Trois niveaux d'engagement

Chaque niveau vous demande d'installer ou de comprendre un peu plus que le précédent, et vous donne en échange davantage de contrôle sur ce que vous produisez.

| | Niveau 1 · Navigateur | Niveau 2 · Votre machine | Niveau 3 · Pro et API |
|---|---|---|---|
| **Ce que vous installez** | Rien | Une appli et des modèles de plusieurs gigaoctets | Rien pour un studio en ligne, une clé API pour automatiser |
| **Ce que ça coûte** | Des crédits gratuits limités, puis un abonnement | Rien par image, mais du matériel puissant | Un abonnement pro ou un paiement à l'usage |
| **Où partent vos images** | Sur les serveurs de la plateforme | Nulle part, elles restent sur votre disque | Sur les serveurs du fournisseur |
| **Ce que vous contrôlez** | Les réglages que l'outil propose | Tout : le modèle, sa version, chaque réglage | Le choix du modèle et son branchement dans vos outils (n8n, scripts) |
| **Pour qui** | Tester, produire quelques visuels | Produire en volume, garder ses images privées, comprendre la mécanique | Produire chaque semaine, automatiser |

### Jusqu'où va cette page

C'est une veille documentée : chaque information vient d'une source officielle listée en bas de page, pas d'un banc d'essai. Elle ne compare pas la qualité des rendus d'un outil à l'autre ; pour ça, le classement de [artificialanalysis.ai](https://artificialanalysis.ai) compare les modèles d'image et de vidéo entre eux. Les offres gratuites changent souvent, la page tarifs de chaque outil a toujours le dernier mot.

## Ce que fait Higgsfield, et où le retrouver

| Ce qui me sert dans Higgsfield | Où le retrouver ailleurs | Niveau |
|---|---|---|
| Le même visage d'une image à l'autre (Soul ID) | Un LoRA, un petit modèle entraîné sur vos photos puis chargé dans ComfyUI, plus exigeant à préparer que Soul ID. Plus simple : l'édition à partir d'images de référence, jusqu'à 14 dans Open Generative AI | 2, ou 1 et 3 |
| Plusieurs modèles au même endroit | Open Generative AI, qui donne accès via Muapi à Kling, Nano Banana et des centaines d'autres modèles ; Runway propose aussi Kling et Seedance à côté de ses propres modèles | 1 et 3 |
| Une image fixe qui s'anime | PixVerse, Adobe Firefly ou Canva en ligne ; Wan 2.2 ou LTX-2 sur votre machine ; Runway ou Kling en studio | 1, 2 et 3 |
| Une voix posée sur un visage (lip sync) | Le Lip Sync Studio d'Open Generative AI (9 modèles), PixVerse ou SeaArt ; les avatars parlants de Vidnoz et DomoAI | 1 |

## Niveau 1 · Dans le navigateur

Rien à installer, vous ouvrez un onglet et vous générez. C'est le bon niveau pour tester une idée ou produire quelques visuels par mois.

Les outils sont classés du plus généreux au moins généreux en gratuit. Un crédit « renouvelé chaque jour » revient le lendemain, un crédit « offert une fois » ne revient pas.

| Outil | Ce qu'il fait | Ce qui est gratuit | Ensuite |
|---|---|---|---|
| [PixVerse](https://pixverse.ai) | Vidéo à partir d'un texte ou d'une image, lip sync, effets | 60 crédits à l'inscription, puis 30 renouvelés chaque jour ; vidéo jusqu'en 540p, avec filigrane | Abonnement dès 8 $/mois en annuel (10 $ au mois) |
| [SeaArt AI](https://www.seaart.ai) | Image, vidéo, lip sync, entraînement de LoRA, ComfyUI en ligne | 130 « Stamina » renouvelés chaque jour, soit environ 21 images ; ils ne se cumulent pas d'un jour à l'autre | Abonnement dès 4,28 €/mois HT en annuel |
| [Adobe Firefly](https://firefly.adobe.com) | Image, vidéo de 5 secondes et audio, à partir d'un texte ou d'une image | Des générations gratuites renouvelées chaque jour, sans abonnement ; Adobe n'en publie pas le nombre | Firefly Standard à 11,08 €/mois TTC, 2 000 crédits |
| [Vidnoz](https://www.vidnoz.com) | Vidéos avec avatars parlants et voix de synthèse | 30 crédits renouvelés chaque jour (60 secondes de vidéo), 720p, avec filigrane | Abonnement dès 19,99 $/mois en annuel |
| [Open Generative AI](https://muapi.ai/open-generative-ai), version web | Des centaines de modèles d'image, de vidéo et de lip sync au même endroit, l'équivalent le plus proche de Higgsfield | Un petit crédit offert à l'inscription chez Muapi, au montant non publié | Paiement à l'usage, sans abonnement ; les crédits n'expirent pas |
| [DomoAI](https://domoai.app) | Anime une image fixe, stylise une vidéo, crée un avatar parlant | Une formule gratuite avec des crédits de départ, au montant non publié | Abonnement dès 9 $/mois en annuel |
| [Canva](https://www.canva.com) | Suite de design qui anime une image en clip de 5 secondes | L'animation d'image, dans la limite du quota IA mensuel. La vidéo à partir d'un texte (8 secondes avec son) est réservée aux formules payantes | Canva Pro à 110 €/an |
| [Renderforest](https://www.renderforest.com) | Vidéo à partir d'un texte, d'images ou d'un son, avatars | 20 crédits de départ, 480p, filigrane, usage personnel seulement | Abonnement dès 9 $/mois en annuel |

> ⚠️ **En gratuit, l'usage commercial est souvent exclu.** Renderforest réserve sa formule gratuite à un usage personnel, Vidnoz n'autorise l'usage commercial qu'avec son filigrane. Avant de livrer un visuel généré gratuitement à un client, relisez les conditions de l'outil.

## Niveau 2 · Installé sur votre machine

Vous installez une appli, elle télécharge des modèles open-source, et chaque génération tourne sur votre ordinateur. Rien ne sort de votre disque et rien ne se paie à l'image.

### Les applis

| Appli | Ce qu'elle fait | Sur Mac | Licence | Liens |
|---|---|---|---|---|
| **ComfyUI** | Interface à nœuds : vous reliez des blocs (modèle, prompt, réglages) pour construire votre chaîne de génération d'images et de vidéos | Appli de bureau pour Windows et macOS, puces Apple Silicon prises en charge | GPL-3.0 | [comfy.org](https://www.comfy.org) · [GitHub](https://github.com/Comfy-Org/ComfyUI) |
| **Pinokio** | Installe et lance des applis d'IA en un clic, sans passer par le terminal | Versions Mac (Apple Silicon et Intel), Windows et Linux | MIT | [pinokio.co](https://pinokio.co) · [GitHub](https://github.com/pinokiocomputer/pinokio) |
| **LTX Desktop** | Vidéo en local avec les modèles LTX de Lightricks, à partir d'un texte, d'une image ou d'un son | Apple Silicon sous macOS 26, 48 Go de mémoire pour la qualité complète (détail [plus bas](#sur-mac-apple-silicon)) | Apache-2.0 pour l'appli, LTX-2 Community License pour les modèles | [ltx.io](https://ltx.io/ltx-desktop) · [GitHub](https://github.com/Lightricks/LTX-Desktop) |
| **Open Generative AI** (bureau) | Une interface pour les modèles en ligne de Muapi (payants) et deux moteurs locaux (gratuits) | Images en local, pas de vidéo locale ; appli non notarisée par Apple | MIT | [Téléchargements](https://github.com/Anil-matcha/Open-Generative-AI/releases) · [GitHub](https://github.com/Anil-matcha/Open-Generative-AI) |

> 🔒 **Pinokio exécute des scripts.** Un script Pinokio peut lancer n'importe quelle commande sur votre machine, comme un programme de terminal. Installez de préférence depuis la page « Discover », dont les scripts sont vérifiés à la main par l'équipe et suivis dans son organisation GitHub officielle.

### Les modèles à faire tourner dedans

| Modèle | Ce qu'il génère | Usage commercial | Matériel indiqué par l'éditeur | Dépôt |
|---|---|---|---|---|
| **Wan 2.2** | Vidéo à partir d'un texte ou d'une image, en 720p à 24 images par seconde | ✅ Oui, licence Apache 2.0 | Le modèle 5B tient sur une carte graphique de 24 Go (RTX 4090) ; les grands modèles en demandent 80 Go | [Wan-Video/Wan2.2](https://github.com/Wan-Video/Wan2.2) |
| **LTX-2** (Lightricks) | Vidéo avec son synchronisé ; succède à [LTX-Video](https://github.com/Lightricks/LTX-Video) | ✅ Oui sous 10 M$ de chiffre d'affaires annuel, licence payante au-delà (LTX-2 Community License) | Voir LTX Desktop ci-dessus | [Lightricks/LTX-2](https://github.com/Lightricks/LTX-2) |
| **HunyuanVideo** (Tencent) | Vidéo | ⛔ Pas en France : la licence exclut l'Union européenne, le Royaume-Uni et la Corée du Sud | Sans objet pour un usage en France | [Tencent-Hunyuan/HunyuanVideo](https://github.com/Tencent-Hunyuan/HunyuanVideo) |
| **FLUX** (Black Forest Labs) | Image à partir d'un texte, édition d'image | ⚠️ Selon la version : oui pour FLUX.1 [schnell] et FLUX.2 [klein] 4B (Apache 2.0), non pour les versions [dev] (licence non commerciale) | FLUX.2 [klein] 4B vise les cartes grand public (RTX 3090 ou 4070) | [flux](https://github.com/black-forest-labs/flux) · [flux2](https://github.com/black-forest-labs/flux2) |

Les chiffres de matériel de Wan, HunyuanVideo et FLUX concernent des cartes graphiques NVIDIA. Aucun de ces éditeurs ne publie de chiffre pour Mac.

## Niveau 3 · Studios pro et API

Deux familles : les studios en ligne, pensés pour réaliser un film ou une campagne, et les API, qui donnent accès à des centaines de modèles depuis un script ou un outil d'automatisation comme n8n.

### Les studios

| Studio | Ce qu'il fait | Ce qui est gratuit | Ensuite |
|---|---|---|---|
| [Runway](https://runway.com) | Vidéo (Gen-4.5, Aleph, et aussi Kling ou Seedance), image, audio ; API | 125 crédits offerts une fois, qui n'expirent pas | Standard à 12 $/mois en annuel (15 $ au mois), 625 crédits |
| [Kling AI](https://kling.ai) | Vidéo et image réalistes, contrôle du mouvement ; API | Une formule à 0 $ sans crédit affiché ; les crédits quotidiens sont réservés aux abonnés, pendant des opérations ponctuelles ; pas d'usage commercial en gratuit | Standard à 8,80 $/mois (6,99 $ le premier mois), 660 crédits |
| [LTX Studio](https://ltx.io/studio) | Storyboards, vidéo et image, pitch decks, chaînes de génération automatisées | 800 crédits offerts une fois, usage personnel seulement | Lite à 12 €/mois en annuel ; usage commercial à partir de la formule Standard |
| [Morphic](https://www.morphic.com) | Création et retouche de vidéos et d'images, son et musique, workflows | Jusqu'à 20 crédits, sur un choix de modèles limité | Basic à 19 $/mois facturé à l'année ; usage commercial à partir de la formule Standard |

### Les API, pour automatiser

Une API se branche sur un script ou sur n8n : vous envoyez un prompt, vous recevez une image ou une vidéo, et vous payez à chaque génération.

| API | Ce qu'elle donne | Ce qui est gratuit | Prix |
|---|---|---|---|
| [Muapi](https://muapi.ai) | Image, vidéo, audio, lip sync et 3D derrière une seule clé ; c'est le moteur d'Open Generative AI | Un petit crédit à l'inscription, au montant non publié | À l'usage, portefeuille rechargeable, crédits sans expiration |
| [WaveSpeed AI](https://wavespeed.ai) | Modèles d'image et de vidéo | 1 $ offert aux nouveaux comptes éligibles, sans carte bancaire ; certains modèles premium exclus | À l'usage, sans abonnement |
| [Fal AI](https://fal.ai) | Image, vidéo, audio et 3D, plus des serveurs de calcul à la demande ; [SDK sur GitHub](https://github.com/fal-ai) | Pas de crédit d'essai affiché ; des crédits ponctuels valables seulement dans le bac à sable du site | À l'usage, prix par modèle, crédits prépayés |

## Sur Mac (Apple Silicon)

Deux applis génèrent des images en local sur un Mac Apple Silicon : l'appli de bureau ComfyUI, et Open Generative AI, dont le moteur intégré s'appuie sur la puce graphique du Mac ; son README indique Dreamshaper 8 (2,1 Go) comme l'option la plus légère testée sur Mac.

Pour la vidéo, LTX Desktop est la seule appli de cette page à publier ses besoins sur Mac. Prévoyez aussi 100 Go d'espace disque libre, et jusqu'à 160 Go si vous ajoutez des LoRA.

| Votre Mac | Ce que LTX Desktop permet |
|---|---|
| Apple Silicon, 48 Go de mémoire ou plus, macOS 26 | Génération locale complète |
| Apple Silicon, 32 Go, macOS 26 | Génération locale limitée à 540p et 5 secondes |
| Moins de 24 Go, ou Mac Intel | Pas de génération locale, l'appli passe par l'API en ligne de Lightricks |
| macOS 14 ou 15 | L'appli s'ouvre mais la génération locale n'est pas encore disponible |

La vidéo locale d'Open Generative AI, elle, ne tourne pas sur Mac, parce que son moteur vidéo (Wan2GP) exige une carte NVIDIA ou AMD, éventuellement sur un autre ordinateur de votre réseau.

Au premier lancement d'Open Generative AI, macOS bloque l'appli, qui n'est pas notarisée par Apple. Pour l'autoriser, ouvrez Réglages Système, puis Confidentialité et sécurité, et cliquez sur « Ouvrir quand même ». Ne le faites que pour une appli téléchargée depuis la [page Releases officielle](https://github.com/Anil-matcha/Open-Generative-AI/releases), puisque vous désactivez pour elle la vérification d'Apple.

Sur un Mac sans beaucoup de mémoire, l'approche hybride reste la plus simple : les images et les essais en local, la vidéo en ligne avec les crédits renouvelés chaque jour de PixVerse, SeaArt ou Adobe Firefly. Le mois où un projet le justifie, un abonnement d'un mois retire le filigrane ; vérifiez quelle formule ouvre l'usage commercial, chez LTX Studio et Morphic ce n'est pas la première.

## Par où commencer

| Votre situation | Commencez par |
|---|---|
| Vous voulez tester sans payer ni rien installer | PixVerse pour la vidéo (30 crédits par jour), SeaArt ou Adobe Firefly pour l'image |
| Vous avez un Mac et voulez des images à volonté | ComfyUI (appli de bureau) avec FLUX.1 [schnell] ou FLUX.2 [klein] 4B, tous deux autorisés pour un client |
| Vous voulez de la vidéo en local sur Mac | LTX Desktop, si votre Mac a au moins 32 Go de mémoire et macOS 26 |
| Vous voulez l'esprit Higgsfield, plusieurs modèles au même endroit, sans abonnement | Open Generative AI en ligne, payé à l'usage via Muapi |
| Vous voulez automatiser votre production | Une API à l'usage, branchée sur [n8n installé chez vous](../tutoriels/installer-n8n-docker.md) |
| Vous livrez des visuels à des clients | Wan 2.2, FLUX.1 [schnell] ou FLUX.2 [klein] 4B en local, ou un service payant dont les conditions autorisent l'usage commercial |

## Sources

Toutes lues le 30 octobre 2026.

Les dépôts et licences :

| Outil ou modèle | Ce qui a été lu |
|---|---|
| Open Generative AI | [README](https://github.com/Anil-matcha/Open-Generative-AI#readme) (Muapi, moteurs locaux, notarisation) et [version 2.0.0 du 23 mai 2026](https://github.com/Anil-matcha/Open-Generative-AI/releases) ; l'ancienne adresse [Open-Higgsfield-AI](https://github.com/Anil-matcha/Open-Higgsfield-AI) y redirige |
| ComfyUI | [README](https://github.com/Comfy-Org/ComfyUI#readme) (plateformes, appli de bureau) et [téléchargement](https://www.comfy.org/download) |
| Pinokio | [README](https://github.com/pinokiocomputer/pinokio#readme) (sécurité des scripts) et [version 8.2.0](https://github.com/pinokiocomputer/pinokio/releases) (Mac, Windows, Linux) |
| LTX Desktop | [README, configuration requise](https://github.com/Lightricks/LTX-Desktop#readme) et [page officielle](https://ltx.io/ltx-desktop) |
| LTX-2 | [Licence LTX-2.x](https://github.com/Lightricks/LTX-2/blob/main/LICENSE-2_x), section 2.1 (seuil de 10 millions de dollars) |
| HunyuanVideo | [Licence](https://github.com/Tencent-Hunyuan/HunyuanVideo/blob/main/LICENSE.txt), définition du territoire ; même clause pour [HunyuanVideo-1.5](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5) |
| FLUX | [Tableau des licences de FLUX.1](https://github.com/black-forest-labs/flux#readme) et [de FLUX.2](https://github.com/black-forest-labs/flux2#readme) |
| Wan 2.2 | [README](https://github.com/Wan-Video/Wan2.2#readme), sections matériel et « License Agreement » ; [guide ComfyUI pour Wan 2.2](https://docs.comfy.org/tutorials/video/wan/wan2_2) |

Les sites et les tarifs ont été relevés depuis la France : certains affichent leurs prix en euros, d'autres en dollars, et ils sont repris tels quels. Quand un éditeur ne publie pas un montant, la page le dit plutôt que de l'estimer.

| Service | Ce qui a été lu |
|---|---|
| Higgsfield | [Formules](https://higgsfield.ai/pricing) |
| Open Generative AI et Muapi | [Tarifs](https://muapi.ai/docs/pricing) et [fonctionnement des crédits](https://muapi.ai/docs/credits) |
| PixVerse | [Formules](https://app.pixverse.ai/subscribe) |
| SeaArt | [Formules et Stamina](https://www.seaart.ai/mall) |
| Adobe Firefly | [Formules](https://www.adobe.com/products/firefly/plans.html) |
| Vidnoz | [Tarifs](https://www.vidnoz.com/pricing.html) ; le tableau annonce 30 crédits par jour et le bandeau du site 60, cette page retient le tableau |
| DomoAI | [Tarifs](https://domoai.app/pricing) et FAQ de la [page d'accueil](https://domoai.app/) |
| Canva | [Accès aux outils IA](https://www.canva.com/help/ai-access/), [image vers vidéo](https://www.canva.com/help/image-to-video/) et [tarifs](https://www.canva.com/fr_fr/tarification/) |
| Renderforest | [Générateur vidéo IA](https://www.renderforest.com/ai-video-generator) et [abonnements](https://www.renderforest.com/subscription) |
| Runway | [Tarifs](https://runwayml.com/pricing) |
| Kling | [Formules](https://kling.ai/app/membership/membership-plan) et [politique de crédits](https://kling.ai/docs/point-policy) ; les « 66 crédits par jour » cités par certains articles ne figurent pas sur le site officiel |
| LTX Studio | [Tarifs](https://ltx.io/studio/pricing) |
| Morphic | [Tarifs](https://www.morphic.com/pricing) |
| WaveSpeed AI | [Tarifs](https://wavespeed.ai/pricing) |
| Fal AI | [Tarifs](https://fal.ai/pricing) et [bac à sable](https://fal.ai/docs/documentation/model-apis/sandbox) |

Depuis le premier recensement, le dépôt Open Higgsfield AI a été renommé, son appli génère aussi en local, et cinq sites ont changé d'adresse : Runway (runway.com), Kling (kling.ai), Pinokio (pinokio.co), LTX Studio (ltx.io/studio) et la page Muapi d'Open Generative AI. Les anciennes adresses redirigent, cette page donne les nouvelles.

## Ailleurs dans la Toolbox

| Dossier | Pour aller plus loin |
|---|---|
| Guides | [Higgsfield dans la boîte à outils IA](../guides/boite-a-outils-ia.md#higgsfield), pour comprendre Soul ID ; [Nano Banana Pro via Google AI Studio](../guides/ressources-ia-generative.md#02--nano-banana-pro-via-google-ai-studio), une autre piste gratuite pour l'image ; [les alternatives gratuites que j'ai testées](../guides/ressources-ia-generative.md#phase-2-les-alternatives-gratuites) |
| Tutoriels | [Génération visuelle à l'échelle](../tutoriels/tutoriels-par-profil.md#génération-visuelle-à-léchelle-avec-higgsfield) et [Identité visuelle cohérente](../tutoriels/tutoriels-par-profil.md#construire-une-identité-visuelle-cohérente-avec-higgsfield), dont la méthode vaut pour tous ces outils ; [Installer n8n avec Docker](../tutoriels/installer-n8n-docker.md), pour automatiser via une API |
| Prompts | [Les prompts d'image et de vidéo commentés](../guides/ressources-ia-generative.md#05--prompts-que-jutilise-et-comment-les-lire) et [les angles photo](../guides/ressources-ia-generative.md#04--maîtriser-les-angles-photo), qui marchent avec chacun de ces modèles ; [tous les prompts](../prompts/) |
| Veille | [Les autres outils de génération](./outils.md), dont Runway, Krea et FLUX |

---

*Par Opaline, Antidote.AI · Vérifié le 30 octobre 2026 · Sous licence [CC BY 4.0](../LICENSE)*
