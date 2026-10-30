# Ressources IA générative

**Outils testés · Prompts · Angles photo · Workflow · Stack marketing**
Par Opaline, 2026

*Mis à jour le 30 octobre 2026.*

> Version illustrée avec les captures d'écran : [`ressources-ia-generative.html`](./ressources-ia-generative.html) (à télécharger puis ouvrir dans un navigateur).

## Sommaire

- [01 · Mon parcours, de MidJourney à Higgsfield](#01--mon-parcours-de-midjourney-à-higgsfield)
- [02 · Nano Banana Pro via Google AI Studio](#02--nano-banana-pro-via-google-ai-studio)
- [03 · Alternatives gratuites, résultats concrets](#03--alternatives-gratuites-résultats-concrets)
- [04 · Maîtriser les angles photo](#04--maîtriser-les-angles-photo)
- [05 · Prompts que j'utilise, et comment les lire](#05--prompts-que-jutilise-et-comment-les-lire)
- [06 · Workflow et outils de production](#06--workflow-et-outils-de-production)
- [07 · Marketing et prospection](#07--marketing-et-prospection)
- [08 · Conclusion, ce que je sais, ce que je ne sais pas encore](#08--conclusion-ce-que-je-sais-ce-que-je-ne-sais-pas-encore)
- [09 · Références, qui suivre, quoi lire](#09--références-qui-suivre-quoi-lire)

## 01 · Mon parcours, de MidJourney à Higgsfield

Spoiler : je n'ai pas eu la révélation divine du premier coup, j'ai tâtonné comme tout le monde. Et finalement, ce tâtonnement c'est la meilleure école, du moment qu'on en tire des conclusions utiles.

### Phase 1, MidJourney · *payant*

MidJourney a été mon terrain de jeu de base. Pour la qualité esthétique pure, c'est encore difficile à battre : cohérence stylistique, richesse des textures, rendu cinématographique quasi-instantané, ce qui en fait un outil de direction artistique, pas seulement de génération. → [midjourney.com](https://www.midjourney.com)

> ⚠️ **Limite.** Maintenir la cohérence d'un visage entre plusieurs images sans `--cref` bien calibré relève du parcours du combattant. On obtient "une femme brune qui lui ressemble vaguement", pas la même personne.

### Phase 2, les alternatives gratuites

J'ai fait le tour des outils gratuits avant de sortir la carte bleue. Honnêtement, la bonne nouvelle, c'est que c'est gratuit, et la mauvaise, c'est que ça se voit parfois.

| Outil | Prix | Ce que ça donne |
|---|---|---|
| Gemini | Gratuit limité | Intégré, pratique, mais cohérence du visage capricieuse. |
| ChatGPT Images | Freemium | Excellent pour des concepts rapides et de plus en plus performant en ce moment, même s'il reste moins précis sur les détails anatomiques. |
| Lumeflow.ai | Freemium | Interface soignée, bons portraits, mais paywall rapide. |
| Leonardo.ai | Freemium, ~150 tokens/j | Un des plus généreux en gratuit. Bonne qualité avec Phoenix et Flux. |
| Playground AI | Freemium | Épuré, bonne qualité réaliste. Devenu un studio de design (logos, affiches, t-shirts), il tourne aujourd'hui sur Muse Image, Nano Banana, GPT Image et Seedream. |
| Adobe Firefly | Inclus CC | Usage commercial sécurisé. Manque de punch sur les ultra-réalistes. |

> ✅ **Verdict terrain.** Pour générer 2-3 images ponctuelles, les outils gratuits suffisent largement ; c'est quand il faut maintenir une identité visuelle cohérente sur plusieurs projets que ça coince.

### Phase 3, Higgsfield (aujourd'hui) · *payant*

Après quelques mois à jongler entre les outils gratuits, j'ai sauté le pas pour trois raisons. Soul Characters et Elements gardent le même visage d'une génération à l'autre. L'outil rassemble aussi plusieurs modèles en un seul endroit (Nano Banana, Seedance, Kling 3.0, Cinema Studio), et son interface est pensée pour produire vite et bien.

→ [higgsfield.ai](https://higgsfield.ai) · Grille tarifaire au 30 octobre 2026, hors TVA : Starter à 19 €/mois pour 270 crédits (même prix au mois ou à l'année), Plus à 59 €/mois ou 47 € en annuel pour 1 200 crédits, Ultra à partir de 129 €/mois ou 99 € en annuel pour 3 000 crédits.

> 🔍 **Nuance honnête.** Je ne dis pas que Higgsfield est objectivement le meilleur outil pour tout le monde. Je dis que c'est celui qui répond à mon usage : volume de production + cohérence identitaire + plusieurs projets en parallèle. La vraie question à te poser est donc "quel est MON besoin ?", bien avant "quel est le meilleur outil ?"

**Pour aller plus loin**

- MidJourney, le modèle Edit (jusqu'à quatre images de référence, il remplace `--cref` depuis la V8.2 de juillet 2026) et `--sref` : cohérence avant de changer d'outil → [docs.midjourney.com](https://docs.midjourney.com/hc/en-us/articles/48495453462797-Edit-Model)
- LoRA : mini-modèles entraînés sur un visage. Bibliothèque open source → [civitai.com](https://civitai.com)
- Comparatif des modèles image IA → [artificialanalysis.ai](https://artificialanalysis.ai)
- Remplacer Higgsfield sans abonnement, en ligne, en local ou à l'usage → [Alternatives à Higgsfield](../veille/alternatives-higgsfield.md)

## 02 · Nano Banana Pro via Google AI Studio

Bonne surprise : Nano Banana Pro est accessible avec une clé API sur AI Studio, et je m'en sers depuis avril 2026 avec 0 € facturé. Vérifie quand même ta facturation, parce que la grille de Google au 30 octobre 2026 ne prévoit aucune offre gratuite pour ce modèle dans l'API : chaque image se paie (détail juste en dessous). → [aistudio.google.com](https://aistudio.google.com)

> 🔍 **Comment ça marche vraiment.** Nano Banana dans le Playground requiert un plan Google AI payant ("Upgrade to unlock") : depuis avril 2026, les abonnements Google AI Pro et Ultra donnent accès à Nano Banana Pro dans AI Studio. Avec une clé API reliée à un compte de facturation (carte enregistrée), l'accès est ouvert mais chaque image est facturée, parce qu'aucun modèle Nano Banana n'a d'offre gratuite dans l'API. Selon la grille de Google au 30 octobre 2026, une image de Nano Banana Pro en 1K ou 2K coûte 0,134 $. En post-paiement, Google te débite à la fin du mois, ou plus tôt si ta dépense atteint le plafond de ton niveau. Au niveau payant 1, ce plafond est de 250 $ par mois, et une fois atteint, l'API se met en pause jusqu'au 1er du mois suivant. Tu passes au niveau 2 (plafond de 2 000 $) une fois 100 $ payés et trois jours écoulés depuis ton premier paiement.

### Tutoriel, configurer ta clé API

Voici exactement les étapes.

1. Aller sur aistudio.google.com → menu en bas à gauche → **Get API Key**
2. Cliquer sur **Créer une clé API**
3. Donner un nom à ta clé, choisir un projet (ou en créer un)
4. Copier les données de ta clé et les garder pour toi, jamais sur une capture d'écran ni dans un fichier partagé. **Tu ne pourras plus la revoir après fermeture.**
5. Revenir sur l'interface → icône Clé en bas à gauche → sélectionner ta clé
6. Confirmation : ta clé est "in use", tu es prête
7. Choisir le modèle Nano Banana Pro dans la liste. Prompt and enjoy.

> 🆘 **Si tu te perds.** Vidéo YouTube d'aide à l'installation : [youtu.be/__O2rm_lvIY](https://youtu.be/__O2rm_lvIY)

Ensuite : inspire-toi sur Pinterest ou Cosmo, puis demande à ton modèle de langage (LLM) préféré d'analyser une image pour en déduire un prompt, parce que la délégation, c'est sous-coté.

**Pour aller plus loin**

- Limites de l'API Google AI Studio, free tier → [ai.google.dev/gemini-api/docs/rate-limits](https://ai.google.dev/gemini-api/docs/rate-limits)
- 300 $ de crédits Google Cloud offerts aux nouveaux comptes, qui ne paient pas l'API Gemini ni AI Studio si ton compte a été ouvert après le 2 mars 2026 → [cloud.google.com/free](https://cloud.google.com/free)
- Hugging Face Spaces, modèles FLUX, SDXL, SD en accès direct → [huggingface.co/spaces](https://huggingface.co/spaces)
- n8n, automatiser une pipeline AI Studio (freemium) → [n8n.io](https://n8n.io)

## 03 · Alternatives gratuites, résultats concrets

J'ai testé ChatGPT et Gemini sur le même type de prompt (portrait surréaliste, tête flottante, style collage), pour montrer plutôt que raconter. Les captures de mes vraies sessions sont dans la version HTML, sans tri des plus réussies (pas de cherry-picking).

### ChatGPT Images · *freemium*

L'esthétique tient la route pour une première itération, et surtout ce portrait est beaucoup plus fidèle à mon visage que celui de Gemini. En ce moment (octobre 2026), ChatGPT devient d'ailleurs de plus en plus performant en génération d'image avec ChatGPT Images 2.5, sorti en septembre 2026 et ouvert à toutes les formules. Quant à DALL-E 3, l'ancien modèle d'image d'OpenAI, il a quitté son API en mai 2026. → [chatgpt.com](https://chatgpt.com)

### Gemini · *gratuit*

Le rendu est plus lisse, presque trop propre, et la cohérence du visage reste le problème principal : c'est joli, mais ce n'est pas moi. → [gemini.google.com](https://gemini.google.com)

> ✅ **Ce que ces résultats m'ont confirmé.** Les deux outils font quelque chose de joli, et le portrait de ChatGPT est nettement plus proche de mon visage que celui de Gemini. Pour un usage créatif sans contrainte d'identité, les outils gratuits font le job ; pour du contenu récurrent avec mon visage, il faut aller plus loin. C'est exactement ce moment qui m'a fait prendre l'abonnement Higgsfield.

**Pour aller plus loin**

- Hugging Face Spaces, FLUX, SDXL, SD sans installation → [huggingface.co/spaces](https://huggingface.co/spaces)
- Civitai, bibliothèque communautaire de modèles et LoRA → [civitai.com](https://civitai.com)
- Craiyon, entièrement gratuit, idéal pour prototyper → [craiyon.com](https://www.craiyon.com)

## 04 · Maîtriser les angles photo

Ce lexique, je le copie-colle directement dans mes prompts. Plus tu es précis sur l'angle, moins l'IA improvise, et elle comprend parfaitement "worm's eye view" ou "over-the-shoulder" puisqu'elle a été entraînée sur des millions de photos étiquetées.

### Angles primaires

| Angle | Effet |
|---|---|
| Eye-level shot | neutre, naturel, engagement direct |
| Low-angle shot | caméra sous le sujet, effet de puissance ou domination |
| High-angle shot | caméra au-dessus, vulnérabilité ou mise en perspective |
| Bird's eye view | plongée directe, parfait pour le flat-lay ou l'architecture |
| Worm's eye view | ras du sol, emphase dramatique vers le haut |
| Three-quarter angle | sujet légèrement tourné, très flatteur pour les portraits |
| 45-degree product angle | vue catalogue pro avec profondeur |

### Angles créatifs et artistiques

| Angle | Effet |
|---|---|
| Close-up macro | mise au point sur la texture ou un seul détail |
| Extreme close-up | isole un élément du visage ou de l'objet |
| Diagonal composition | cadrage dynamique guidant l'œil |
| Over-the-shoulder | sujet partiel en avant-plan, profondeur narrative |
| Silhouette backlit | forme forte contre source de lumière |
| Framed-through-foreground | sujet vu à travers porte, feuilles, objet |
| Reflected angle (mirror/glass) | couches et atmosphère supplémentaires |

### Angles contextuels et stylisés

| Angle | Effet |
|---|---|
| Candid street-level | perspective authentique et spontanée |
| Aerial drone-style | composition géométrique vue de haut |
| Shallow depth of field portrait | sujet net, fond flou (bokeh) |
| Symmetrical centered | minimaliste et équilibré |
| Architectural upward angle | légèrement incliné vers les structures hautes |

> 💡 **Astuce de terrain.** Je combine toujours l'angle avec une référence caméra dans le prompt. Exemples : `low-angle shot, handheld feel` / `overhead top-down, shot on ARRI Alexa`. L'IA adapte l'éclairage en conséquence.

**Pour aller plus loin**

- Règle des tiers, leading lines, negative space → [photographylife.com](https://photographylife.com)
- Focal length vs camera distance → [photographylife.com](https://photographylife.com/what-is-lens-compression)
- Negative space / breathing room → [adobe.com](https://www.adobe.com/creativecloud/photography/type/negative-space-photography.html)

## 05 · Prompts que j'utilise, et comment les lire

Ces prompts viennent de ma pratique et de ma veille, et aucun n'est parfait : tous sont à adapter selon le modèle, parce que ce qui fonctionne sur Nano Banana ne fonctionnera pas pareil sur MidJourney.

### Portrait éditorial halftone, style magazine vintage

C'est mon prompt de direction artistique éditoriale : collage papier découpé, impression offset CMJN, effet vintage 70s.

```text
// CONCEPT
Surreal close-up: disembodied floating head as flat hard-edged paper collage element.
Visible cut edge + drop shadow. No neck, no shoulders. Head slightly tilted.

// IDENTITY (from reference images)
Preserve exact facial identity: face shape, eyes, nose, lips, skin tone, hair.
Face 100% recognizable. Preserve jewelry (earrings) exactly.

// PRINT TEXTURE (head only)
CMYK color halftone. Offset lithography simulation.
Visible misregistered dots in cyan/magenta/yellow/black.
Warm newsprint. Vintage 1970s fashion magazine aesthetic.

// BACKGROUND
Solid matte color #568DA3. Fine 35mm film grain. Completely empty.
Soft realistic drop shadow from the cutout head.

// COMPOSITION
Centered, tightly framed on head. Deep focus throughout. Pop-art mood.
```

### Méthode 2 temps, reproduire une ambiance

1. Envoyer l'image de référence à ChatGPT avec ce prompt :

   ```text
   Tu es prompt engineer et directeur artistique. Analyse cette image. Génère un prompt
   pour Nano Banana qui recrée la même ambiance, en changeant le visage pour [description]
   et la tenue pour [description].
   ```

2. Copier le prompt généré dans Nano Banana ou AI Studio.

L'ambiance, la lumière et la composition sont reproduites, sans décoder chaque paramètre moi-même.

### Transformer une illustration en photo réaliste

```text
Recreate the reference image as a realistic 1:1 live-action photograph.
Use the first reference image strictly as the identity reference.
Preserve the exact facial structure, skin tone, proportions, all features.
Match the second reference image exactly:
- Same pose, body position, camera angle, framing, composition, clothing
Translate only into realistic live-action:
- Real human anatomy & skin texture (pores, micro-imperfections)
- Real fabrics, physically accurate lighting
Ultra-realistic cinematic photography. Shot on ARRI Alexa, anamorphic lens.
Natural depth of field, 4K realism. No anime, no illustration, no CGI, no cosplay.
```

### Template, améliorer le grain et le réalisme

Le paramètre qui change tout, c'est `CAMERA FEEL: smartphone photography`, parce qu'il casse l'effet IA quasi immédiatement.

```text
[SHOT TYPE] portrait of [AGE]-year-old, [SKIN TONE / ETHNICITY],
documentary-style photograph.

KEY DETAILS: [skin, age, emotion, texture]
FOCAL AREAS: [face / hands / eyes / body part]
BACKGROUND: [simple, real-world]
SKIN: [pores, wrinkles, dryness, oil, imperfections]
HAIR: [baby hairs, stray hair, texture]
EXPRESSION/POSE: [neutral, smiling, relaxed, unposed]
LIGHT: [window / side / ambient daylight], reveal texture, not hide it.
CAMERA FEEL: smartphone photography.
Organic sharpness, micro-contrast, slight digital grain.
Real, imperfect, human, unretouched. Not AI-generated, not polished.
```

### Character sheet, fiche personnage complète

```text
Create a hyper-realistic photo-real character sheet on a clean white studio background.
Ensure the likeness is exact, all facial and physical details with precision.
Include:
- Two full-body images showcasing the outfit
- Three close-up facial portraits (different angles & expressions)
Modify the outfit: change all [COLOR] elements to [NEW COLOR]
while maintaining original style and texture.
Crisp, professional, high-quality character sheet standards.
```

### Template prompt vidéo

```text
SUBJECT: [précis, "femme trentaine veste bleue", pas juste "une personne"]
ACTION: ["marche lentement" dit plus que "marche"]
SETTING: ["rue urbaine coucher du soleil" ≠ "rue urbaine minuit"]
CAMERA MOVEMENT: ["slow dolly forward" vs "handheld tracking shot"]
LIGHTING: ["soft natural window light" vs "harsh overhead fluorescent"]
STYLE: ["cinematic" / "documentary" / "commercial" / "UGC"]
```

**Pour aller plus loin**

- Negative prompts, dire à l'IA ce qu'on ne veut PAS voir → [learnprompting.org](https://learnprompting.org/docs/image_prompting/fix_deformed_generations)
- Le "seed" pour la reproductibilité → [docs.midjourney.com](https://docs.midjourney.com/hc/en-us/articles/32604356340877-Seeds)
- PromptHero, banque communautaire de prompts → [prompthero.com](https://prompthero.com)

## 06 · Workflow et outils de production

### Image

| Outil | Prix | Usage |
|---|---|---|
| [Flair.ai](https://flair.ai) | Freemium | Visuels produit IA. Packshots éditoriaux sans plateau photo. |
| [Magnific AI](https://www.magnific.com) | Payant | Upscaler + Enhancer. Peut halluciner des détails supplémentaires guidés par prompt. Résultat difficile à distinguer d'une photo 4K. Freepik a pris le nom de Magnific, si bien que l'upscaler fait désormais partie d'une plateforme complète d'image et de vidéo. |
| [Figma Weave (ex-Weavy)](https://weave.figma.com) | Freemium | Plateforme node-based pour pipeline de génération IA, devenue Figma Weave. |

### Vidéo

| Outil | Prix | Usage |
|---|---|---|
| [Clipcut](https://www.clipcut.pro) | Payant (dès 9 $/mois) | Génère des shorts viraux depuis une longue vidéo automatiquement. TikTok, Reels, YouTube Shorts. |
| [Agent Opus](https://opus.pro) | Freemium | Motion graphics et animations depuis un prompt ou une image. |
| [Banger.video](https://banger.video) | Freemium | Vidéos réseaux sociaux complètes depuis une idée ou du footage brut. L'IA monte, toi tu contrôles. Le site était hors ligne le 30 octobre 2026 (« Deployment Paused »), vérifie qu'il répond avant de t'y fier. |
| [FaceFusion 3.9.2](https://docs.facefusion.io) | Gratuit | Face-swap en temps réel. Open source. |

### Présence creator

| Outil | Prix | Usage |
|---|---|---|
| [Beacons.ai](https://beacons.ai) | Gratuit | Link in bio + media kit + boutique + email marketing. |
| [QuillBot](https://quillbot.com) | Freemium | Reformulation, analyse de ton, fluidité. Le meilleur outil pour casser l'effet "écrit par une machine". |
| [Lens Distortions](https://lensdistortions.com) | Payant | Musique instrumentale cinématographique pour cinéastes. Filtrée par mood et style. |

> 🧪 **Idée à creuser, m'automatiser.** Créer plusieurs vidéos de moi dans plusieurs endroits différents sans y être physiquement, en me servant de Higgsfield (Seedance / Kling 3.0) pour générer les variantes de contexte, puis automatiser la diffusion. Ce workflow n'est pas encore formalisé, c'est la prochaine étape.

**Pour aller plus loin**

- remove.bg, détourage automatique et gratuit, mais son site ferme le 1er décembre 2026 et l'outil passe dans Canva → [remove.bg](https://www.remove.bg)
- Adobe Express AI, retouche rapide, inclus Creative Cloud → [express.adobe.com](https://express.adobe.com)
- Kapwing, montage vidéo en ligne avec IA → [kapwing.com](https://www.kapwing.com)
- Canva AI (ex-Magic Studio), visuels de communication rapides → [canva.com](https://www.canva.com/canva-ai/)

## 07 · Marketing et prospection

### Génération de leads

| Outil | Prix | Usage |
|---|---|---|
| [Waalaxy](https://www.waalaxy.com) | Payant (14 jours d'essai) | Prospection LinkedIn + email automatisée, no-code. Sa page de tarifs n'affiche plus de version gratuite au 30 octobre 2026 : la formule Pro coûte 19 € par mois et par utilisateur pour 300 invitations par mois. Sert à construire des listes qualifiées et à lancer des séquences. |

### CRM et automation

| Outil | Prix | Usage |
|---|---|---|
| [ActiveCampaign](https://www.activecampaign.com) | Payant | CRM + automation marketing, gestion des données clients. |
| [DOJO AI](https://www.dojoai.com) | Payant | AI Marketing OS pour challenger brands. Capacités enterprise sans la complexité. |
| [Make (ex-Integromat)](https://www.make.com) | Freemium | Automation de workflows no-code et agentique, visuel. Parfait pour coller les outils entre eux. |
| [Systeme.io](https://systeme.io) | Freemium | Alternative gratuite pour construire son business en ligne : tunnels, emails, cours. |

> 🧩 **Ma logique de stack marketing.**
> 1. Waalaxy, alimenter le haut du funnel
> 2. Systeme.io / ActiveCampaign, nurturing et séquences email
> 3. Make, coller tout ça et automatiser les déclencheurs
>
> Je construis brique par brique plutôt que tout en même temps, c'est plus sain.

**Pour aller plus loin**

- Le hook, première brique de la méthode hook-value-CTA pour structurer tout contenu social → [buffer.com](https://buffer.com/resources/social-media-hooks/)
- Buffer, planification multi-réseaux, plan gratuit généreux → [buffer.com](https://buffer.com)
- Hypefury, planification pour Bluesky, Threads, LinkedIn et Instagram, qui ne gère plus X (Twitter) → [hypefury.com](https://hypefury.com)
- Content calendar dans Notion ou Airtable → [notion.com](https://www.notion.com)

## 08 · Conclusion, ce que je sais, ce que je ne sais pas encore

Ce document, c'est un instantané de là où j'en suis plutôt qu'une vérité absolue, parce que les outils changent vite et que les modèles évoluent encore plus vite.

### Ce que je ferais peut-être différemment

Je me demande parfois si je n'aurais pas dû creuser davantage MidJourney avec `--cref` et `--sref` avant de switcher. La cohérence y a progressé vite et le niveau artistique reste imbattable.

Et je ne suis pas certaine qu'un abonnement Higgsfield soit la bonne décision pour quelqu'un qui génère peu de volume. Dans ce cas, les outils gratuits bien maîtrisés font largement l'affaire.

### Les alternatives que je n'ai pas encore testées

| Outil | Prix | Pourquoi ça m'intéresse |
|---|---|---|
| Runway Gen-4.5 | Payant | Référence de la vidéo IA. Cohérence temporelle et effets cinématographiques avancés. |
| Krea.ai | Freemium | Génération d'image en temps réel : l'image se redessine pendant que tu tapes. |
| ComfyUI | Gratuit | Node-based open source pour Stable Diffusion. Contrôle total, courbe d'apprentissage réelle. |
| Ideogram 4.5 | Freemium | Excellent pour intégrer du texte dans les images, un point fort que Google annonce aussi désormais pour Nano Banana 2.1. |
| Pika Labs | Payant (compte gratuit sans crédit mensuel) | Effets vidéo spectaculaires : transformations, liquides, explosions. |
| Sora (OpenAI) | Fermé | OpenAI a arrêté le site et l'appli Sora le 26 avril 2026, puis son API le 24 septembre 2026. |

### Ce que j'ai appris de tout ça

- La cohérence du visage est le problème #1 non résolu des outils gratuits, et c'est ce critère seul qui peut justifier un abonnement payant.
- Le meilleur prompt est celui que tu comprends, pas celui que tu as copié. Prends le temps d'analyser pourquoi ça fonctionne.
- Les outils changent très vite, d'où l'intérêt de rester pragmatique : tester → comparer → choisir → avancer.
- La stack parfaite n'existe pas, puisque chaque outil a ses angles morts : ce qui compte, c'est de savoir lesquels sont les tiens.

> Le tout, c'est d'avoir un concept clair en tête, ensuite ça va tout seul.
>
> La créativité, c'est le maître mot : les outils changent tous les six mois, toi, tu restes.

## 09 · Références, qui suivre, quoi lire

Elles sont triées par format et taggées par sujet, sans aucun sponsoring : que du vrai.

### YouTube

| Qui | Sujets | Pourquoi |
|---|---|---|
| [Matt Wolfe](https://www.youtube.com/@mreflow) | IA · Veille · Outils · EN | Le rendez-vous hebdo de l'IA : outils testés, démos, comparatifs. |
| [MattVidPro AI](https://www.youtube.com/@MattVidPro) | IA · Actu · Outils | Actu IA quotidienne, outils testés en live. Court, dense, efficace. |
| [Sebastian Kamph](https://www.youtube.com/@sebastiankamph) | ComfyUI · Open source · Avancé | ComfyUI, Flux, Stable Diffusion en profondeur. Pour ceux qui veulent tout comprendre. |
| [Runway](https://www.youtube.com/@runwayml) | Vidéo · IA · Officiel | Tutoriels officiels + showreels de la communauté. |

### Instagram / TikTok

| Qui | Sujets | Pourquoi |
|---|---|---|
| [@higgsfield.ai](https://www.instagram.com/higgsfield.ai) | IA · Vidéo · Image | Créations de la communauté et annonces des nouvelles fonctionnalités. |
| [@runwayapp](https://www.instagram.com/runwayapp) | Vidéo · IA · Cinéma | Showreels et dernières fonctionnalités. |
| [@midjourney](https://www.instagram.com/midjourney) | IA · Image · Inspiration | Inspirations de la communauté + updates. |
| [@georges.pdf](https://www.instagram.com/georges.pdf) | UX · Design · Créatif | Inspiration vidéo UX/UI, format court, œil très affûté. |

### Newsletters et blogs

| Qui | Sujets | Pourquoi |
|---|---|---|
| [Ben's Bites](https://www.bensbites.com) | IA · Daily · EN | Daily AI digest, fun, dense, sans prise de tête. |
| [The Rundown AI](https://www.therundown.ai) | IA · Synthèse | 5 minutes par jour pour tout savoir sur l'IA. Synthétique, bien sourcé. |
| [Lenny's Newsletter](https://www.lennysnewsletter.com) | Product · Marketing · Growth | Product, growth, IA dans le monde du produit. |
| [L'IA Quotidienne](https://aiqu.substack.com) | IA · Français · Veille | La veille en français, sans se noyer. |

### Studios et entreprises

| Qui | Sujets | Pourquoi |
|---|---|---|
| [Runway](https://runway.com) | Vidéo · IA · Research | Le leader de la vidéo IA créative. Blog Research = mine d'or. |
| [ElevenLabs](https://elevenlabs.io) | Audio · Voix · IA | Le grand nom de la voix IA. Clonage vocal, audio génératif. |
| [Pika Labs](https://pika.art) | Vidéo · IA · Effets | Effets vidéo spectaculaires : transformations, liquides. |
| [Krea.ai](https://www.krea.ai) | Image · IA · Temps réel | Génération d'image en temps réel, qui change à chaque mot tapé. |

**Ailleurs dans la Toolbox**

- Les alternatives à Higgsfield, classées par profondeur, avec licences et sources → [veille](../veille/alternatives-higgsfield.md)
- Higgsfield pas à pas, de Soul ID à la production en série → [tutoriel Com & Marketing](../tutoriels/tutoriels-par-profil.md#génération-visuelle-à-léchelle-avec-higgsfield) et [tutoriel Business Instagram](../tutoriels/tutoriels-par-profil.md#construire-une-identité-visuelle-cohérente-avec-higgsfield)
- Brancher la génération visuelle dans un pipeline automatisé → [n8n et Airtable](../tutoriels/tutoriels-par-profil.md#construire-ton-pipeline-de-contenu-avec-n8n--airtable)

---

*Antidote.AI · Par Opaline · 2026*
