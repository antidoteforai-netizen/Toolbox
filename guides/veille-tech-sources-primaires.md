<sub>[Toolbox](../README.md) › [Guides](./README.md) › Veille tech à la source</sub>

# Veille tech à la source

**Apprendre une nouveauté tech le jour où elle sort, avec un lecteur RSS gratuit, Claude ou n8n.**

Quand une annonce tech arrive dans ton fil LinkedIn, elle existe déjà ailleurs depuis des heures, parfois des jours. Elle est sortie sur la page d'actualités de l'entreprise, dans une nouvelle version publiée sur GitHub ou dans un document déposé auprès d'un régulateur. Les journalistes lisent ces sources au moment où elles tombent, et rien ne t'empêche d'en faire autant. Ce guide montre où l'info naît, quels flux suivre (27 sont testés et prêts à importer d'un coup) et comment trier tout ça en cinq minutes par matin, à la main, avec Claude ou avec n8n.

## Sommaire

- [Démarrer en dix minutes avec un lecteur RSS gratuit](#démarrer-en-dix-minutes-avec-un-lecteur-rss-gratuit)
- [Les médias relaient une info née ailleurs](#les-médias-relaient-une-info-née-ailleurs)
- [Les endroits où l'info apparaît en premier](#les-endroits-où-linfo-apparaît-en-premier)
- [Hacker News, Product Hunt et GitHub font remonter l'info avant la presse](#hacker-news-product-hunt-et-github-font-remonter-linfo-avant-la-presse)
- [Les flux à suivre, testés le 30 octobre 2026](#les-flux-à-suivre-testés-le-30-octobre-2026)
- [Choisir son lecteur RSS](#choisir-son-lecteur-rss)
- [Les API et alertes gratuites, avec leurs limites](#les-api-et-alertes-gratuites-avec-leurs-limites)
- [Trois montages selon le temps que tu peux y mettre](#trois-montages-selon-le-temps-que-tu-peux-y-mettre)
- [Faire son brief du matin avec une IA](#faire-son-brief-du-matin-avec-une-ia)
- [Automatiser le tri avec n8n](#automatiser-le-tri-avec-n8n)
- [Les sources que la plupart des veilles oublient](#les-sources-que-la-plupart-des-veilles-oublient)
- [Le prompt du brief, prêt à coller](#le-prompt-du-brief-prêt-à-coller)
- [Les pièges d'une veille trop rapide](#les-pièges-dune-veille-trop-rapide)
- [Ta première semaine, jour par jour](#ta-première-semaine-jour-par-jour)
- [Sources et vérifications](#sources-et-vérifications)

## Démarrer en dix minutes avec un lecteur RSS gratuit

Un flux RSS, c'est la boîte aux lettres d'un site : chaque nouvel article y tombe, et un lecteur RSS relève toutes tes boîtes au même endroit, sans algorithme qui choisit à ta place. Le fichier [veille-tech-flux.opml](./veille-tech-flux.opml) en contient 27, rangés en quatre dossiers. Un OPML est simplement une liste de flux, dans un format que tous les lecteurs savent importer.

1. Crée un compte gratuit sur [Feeder](https://feeder.co) ou sur [Inoreader](https://www.inoreader.com), par exemple (le comparatif est [plus bas](#choisir-son-lecteur-rss)).
2. Télécharge [veille-tech-flux.opml](./veille-tech-flux.opml) : sur GitHub, ouvre le fichier puis clique sur le bouton « Download raw file ».
3. Dans les réglages du lecteur, cherche « Importer » ou « OPML » et choisis le fichier. Les flux arrivent dans quatre dossiers : Avance sur l'actu (4 flux), Sources primaires (7), Médias US / Silicon Valley (7), French Tech et Europe (9).
4. Épingle en tête les quatre flux d'avance : Techmeme, Hacker News, Product Hunt et GitHub Trending.
5. Lis cinq minutes le matin, sans aller au-delà la première semaine, le temps de repérer les flux que tu sautes à chaque fois.

## Les médias relaient une info née ailleurs

Si Techmeme, Hacker News et les grands médias américains ont toujours un temps d'avance, c'est qu'ils sont placés plus haut dans la chaîne qui va de la décision d'une entreprise à ton fil d'actualité. Ils reçoivent les communiqués sous embargo, c'est-à-dire envoyés aux journalistes avant l'heure de publication. Ils ont aussi des contacts à l'intérieur des entreprises et lisent les sources publiques à la minute où elles paraissent. La plupart des scoops sont publics dès leur naissance, sous la forme d'un fichier déposé, d'une version de code ou d'une page modifiée, et presque personne ne les lit à ce moment-là.

| Étape | Ce qui se passe | Délai indicatif |
|---|---|---|
| 0. Décision interne | Une entreprise décide de lever des fonds, de lancer un produit ou de licencier | Inaccessible |
| 1. Fuite | Une personne de l'intérieur parle à un journaliste | De quelques minutes à plusieurs jours avant la publication |
| 2. Publication à la source | Blog officiel, version publiée sur GitHub, document déposé à la SEC (l'autorité des marchés américaine), page produit modifiée, post d'un dirigeant | Quasi immédiat |
| 3. Fin de l'embargo | Le communiqué reçu à l'avance par les journalistes est publié à l'heure prévue | Immédiat pour eux, tout le monde le voit ensuite |
| 4. Agences et grands médias américains | Reuters, Bloomberg, The Information, TechCrunch, The Verge | De quelques minutes à quelques heures |
| 5. Agrégateurs et communautés | Techmeme, Hacker News, Product Hunt, Reddit | De quelques minutes à quelques heures |
| 6. Médias français | Reprise et traduction de la presse américaine | De quelques heures à plusieurs jours |
| 7. LinkedIn et newsletters | Prises de position et résumés | Plusieurs jours |

Ces délais sont des ordres de grandeur, qui varient d'une histoire à l'autre. Plus tu lis bas dans ce tableau, plus tu arrives tard, alors vise les étapes 2 à 5. Garde les médias français pour le contexte et pour ce que la presse américaine ne couvre pas, la French Tech en tête. Comme ces médias reprennent souvent la presse américaine avec du retard, lire la source primaire te donne aussi de l'avance pour ton propre contenu.

## Les endroits où l'info apparaît en premier

Une bonne partie de ces sources sont des dépôts réglementaires, les documents qu'une entreprise est obligée de déposer auprès d'une autorité : ils sont publics, gratuits et très peu lus.

| Source | Ce qui y apparaît en premier | Où regarder |
|---|---|---|
| Salles de presse des entreprises | Les annonces officielles, à la seconde où l'embargo tombe | Les flux RSS de leurs blogs et pages d'actualités ([liste plus bas](#les-flux-à-suivre-testés-le-30-octobre-2026)) |
| Dépôts réglementaires américains | Événements importants (formulaire 8-K), levées de fonds de startups (Form D), introductions en bourse (S-1), règles sur l'IA, les puces et les données | [SEC EDGAR](https://www.sec.gov/edgar/search/), [Federal Register](https://www.federalregister.gov), [Congress.gov](https://www.congress.gov) |
| Textes européens et français | AI Act, DMA, DSA, annonces légales, augmentations de capital, marques et brevets, lois en discussion | [EUR-Lex](https://eur-lex.europa.eu), [BODACC](https://www.bodacc.fr), [INPI](https://data.inpi.fr), [Légifrance](https://www.legifrance.gouv.fr), les dossiers législatifs de l'[Assemblée nationale](https://www.assemblee-nationale.fr) et du [Sénat](https://www.senat.fr) |
| Le code et les produits | Nouvelles versions, fonctions pas encore annoncées, changements de doc ou de tarifs, offres d'emploi, nouveaux noms de domaine | Les versions publiées sur GitHub, les journaux de modifications (changelogs), les pages carrières, [crt.sh](https://crt.sh) pour les certificats des nouveaux domaines |
| Tribunaux et brevets | Plaintes, procès, dépôts de brevets | [CourtListener](https://www.courtlistener.com) pour les tribunaux américains |
| Réseaux et communautés | Les annonces de dirigeants et de chercheurs, souvent en pleine nuit française | X, Bluesky, LinkedIn, Discord, forums de développeurs |
| Recherche | Les papiers et les résultats de tests, avant leur reprise par la presse | [arXiv](https://arxiv.org), les blogs des labos, [Hugging Face Daily Papers](https://huggingface.co/papers) |

Les médias gardent un avantage, leurs sources internes (salariés, investisseurs, avocats), auxquelles tu n'auras jamais accès directement, mais tu peux suivre les journalistes qui les publient. Pour les données d'entreprises françaises, [Pappers](https://www.pappers.fr) et [data.gouv.fr](https://www.data.gouv.fr) simplifient l'accès ; lis les conditions de leurs API avant d'automatiser quoi que ce soit.

## Hacker News, Product Hunt et GitHub font remonter l'info avant la presse

Sur [Hacker News](https://news.ycombinator.com), des humains (souvent les fondateurs eux-mêmes) postent des liens que la communauté classe par votes. Comme cette communauté lit les sources primaires en continu, une annonce y remonte souvent avant d'arriver dans la presse. Trois portes d'entrée existent, toutes gratuites et sans clé :

```text
API officielle, en temps réel :    https://hacker-news.firebaseio.com/v0/topstories.json
Recherche par date (Algolia) :     https://hn.algolia.com/api/v1/search_by_date?tags=story&numericFilters=points%3E100
Flux RSS filtré (hnrss.org) :      https://hnrss.org/newest?q=mistral&points=50
```

La dernière adresse renvoie les nouveaux sujets qui parlent de Mistral et ont dépassé 50 points : remplace `mistral` par ton sujet. Le service hnrss.org est communautaire, pas officiel, mais il a répondu à tous les tests.

[Product Hunt](https://www.producthunt.com) liste les outils lancés chaque jour. Son flux (`https://www.producthunt.com/feed`) suffit pour lire. Son API GraphQL demande un jeton développeur gratuit et reste réservée, par défaut, à un usage non commercial, d'après sa documentation.

GitHub Trending montre les dépôts de code qui décollent. Il n'a pas de flux officiel, mais un [flux communautaire](https://mshibanami.github.io/GitHubTrendingRSS/) le reprend chaque jour. Pour un sujet précis, l'API de recherche de GitHub liste les dépôts récents classés par étoiles, par exemple ceux qui portent le sujet `mcp` créés depuis le 23 octobre 2026 :

```text
https://api.github.com/search/repositories?q=topic:mcp+created:%3E2026-10-23&sort=stars
```

Reste [Techmeme](https://www.techmeme.com), qui regroupe les articles parlant d'une même histoire, grâce à un algorithme relu par des éditeurs humains. C'est le radar de ce que la presse reprend : idéal pour voir en un coup d'œil l'histoire du jour, moins pour la voir naître.

## Les flux à suivre, testés le 30 octobre 2026

Chaque adresse ci-dessous a été ouverte ce jour-là et renvoie un flux valide. Les flux marqués « Oui » sont dans le [fichier d'import](./veille-tech-flux.opml) ; les autres s'ajoutent à la main si le sujet t'intéresse. Les adresses changent avec le temps, alors prévois de vérifier tes flux une fois par mois.

### Les flux qui donnent de l'avance

| Source | Flux | Dans le fichier |
|---|---|---|
| Techmeme | `https://www.techmeme.com/feed.xml` | Oui |
| Hacker News, la une | `https://hnrss.org/frontpage` | Oui |
| Hacker News, flux officiel | `https://news.ycombinator.com/rss` | Non |
| Product Hunt | `https://www.producthunt.com/feed` | Oui |
| GitHub Trending (flux communautaire) | `https://mshibanami.github.io/GitHubTrendingRSS/daily/all.xml` | Oui |

### Les entreprises et les fonds, à la source

| Source | Ce que tu y lis | Flux | Dans le fichier |
|---|---|---|---|
| OpenAI | Annonces de produits et de modèles | `https://openai.com/news/rss.xml` | Oui |
| Google DeepMind | Recherche et modèles Gemini | `https://deepmind.google/blog/rss.xml` | Oui |
| Mistral AI | Le laboratoire d'IA français | `https://mistral.ai/news/rss` | Oui |
| Hugging Face | Modèles open source | `https://huggingface.co/blog/feed.xml` | Oui |
| Y Combinator | Les startups de son programme | `https://www.ycombinator.com/blog/rss` | Oui |
| a16z | Les analyses du fonds Andreessen Horowitz | `https://a16z.substack.com/feed` | Oui |
| Sequoia Capital | Les essais du fonds | `https://www.sequoiacap.com/feed/` | Oui |
| Versions publiées sur GitHub | Chaque nouvelle version d'un dépôt, par exemple le SDK Python d'Anthropic | `https://github.com/ORG/DEPOT/releases.atom`, testé avec `https://github.com/anthropics/anthropic-sdk-python/releases.atom` | Non |

Anthropic n'a pas de flux RSS : la parade est dans [les sources sans flux](#les-sources-sans-flux-et-comment-les-suivre-quand-même).

### Les médias américains et la Silicon Valley

| Source | Ce que tu y lis | Flux | Dans le fichier |
|---|---|---|---|
| TechCrunch | Startups et levées de fonds | `https://techcrunch.com/feed/` | Oui |
| The Verge | Produits et grandes plateformes | `https://www.theverge.com/rss/index.xml` | Oui |
| Ars Technica | Le fond technique | `https://feeds.arstechnica.com/arstechnica/index` | Oui |
| Wired | Culture tech et coulisses | `https://www.wired.com/feed/rss` | Oui |
| CNET | Produits grand public | `https://www.cnet.com/rss/news/` | Oui |
| NYT Technology | La rubrique tech du New York Times | `https://rss.nytimes.com/services/xml/rss/nyt/Technology.xml` | Oui |
| 404 Media | Enquêtes indépendantes, média sur abonnement | `https://www.404media.co/rss/` | Oui |
| MIT Technology Review | Recherche et enjeux | `https://www.technologyreview.com/topnews.rss` | Non |
| Engadget | Produits et matériel | `https://www.engadget.com/rss.xml` | Non |
| Gizmodo | Tech et sciences, grand public | `https://gizmodo.com/rss` | Non |
| Stratechery | Les analyses stratégiques de Ben Thompson | `https://stratechery.com/feed/` | Non |
| GeekWire | La tech vue de Seattle | `https://www.geekwire.com/feed/` | Non |

### La French Tech et l'Europe

| Source | Ce que tu y lis | Flux | Dans le fichier |
|---|---|---|---|
| Maddyness | Startups et levées de fonds en France | `https://www.maddyness.com/feed/` | Oui |
| FrenchWeb | Le numérique français | `https://www.frenchweb.fr/feed` | Oui |
| Siècle Digital | Tech et société | `https://siecledigital.fr/feed/` | Oui |
| Presse-citron | Produits grand public | `https://www.presse-citron.net/feed/` | Oui |
| Journal du Net | Le business du numérique | `https://www.journaldunet.com/rss/` | Oui |
| L'Usine Digitale | Industrie et B2B | `https://www.usine-digitale.fr/rss` | Oui |
| Les Pépites Tech | Les jeunes pousses de la French Tech | `https://lespepitestech.com/feed` | Oui |
| Sifted | Startups européennes, média soutenu par le Financial Times | `https://sifted.eu/feed` | Oui |
| tech.eu | Startups et financements européens | `https://tech.eu/feed/` | Oui |
| Numerama | Tech et culture numérique | `https://www.numerama.com/feed/` | Non |
| French Tech Journal | La French Tech racontée en anglais | `https://www.frenchtechjournal.com/latest/rss/` | Non |

### Les sources sans flux, et comment les suivre quand même

| Source | Ce qui manque | Comment la suivre |
|---|---|---|
| Anthropic | Aucun flux RSS sur [anthropic.com/news](https://www.anthropic.com/news) au moment de la vérification | Un outil de surveillance de page ([Visualping](https://visualping.io), [changedetection.io](https://changedetection.io)), ou un flux généré ([RSS-Bridge](https://github.com/RSS-Bridge/rss-bridge), [RSS.app](https://rss.app), les flux IA de Feeder) ; les versions de ses SDK ont, elles, un flux GitHub |
| [Defend Intelligence](https://www.defendintelligence.com) | Site français d'actualité IA très actif, sans flux RSS trouvé | Sa newsletter, reçue dans ta boîte mail ou directement dans ton lecteur |
| X (Twitter) | Pas de flux fiable sans compte payant | Les médias qui citent les posts, ou Bluesky, où chaque profil a son flux |

## Choisir son lecteur RSS

Les 27 flux du fichier d'import tiennent dans le plan gratuit de tous les lecteurs ci-dessous. Feeder, que le guide prend souvent en exemple, détaille ses plans ainsi :

| | Free | Plus | Professional |
|---|---|---|---|
| Prix | 0 $ | 7,99 $ par mois en annuel, 9,99 $ au mois | 14,99 $ par utilisateur et par mois en annuel, 19,99 $ au mois |
| Flux suivis | 200 | 2 500 | 10 000 |
| Mise à jour des flux | Toutes les 30 minutes | Toutes les 5 minutes | Toutes les minutes |
| Résumés IA | 2 par jour | 10 par jour | 60 par jour |

Source : [la grille tarifaire de Feeder](https://feeder.co/pricing), lue le 30 octobre 2026. Aucun plan n'affiche de publicité, et le gratuit reçoit déjà les newsletters par e-mail et propose 3 flux IA pour les sites sans RSS. Il n'a en revanche ni alertes par e-mail ni règles de tri automatiques. Feeder publie aussi des comparatifs où il se recommande lui-même, à lire avec ce recul.

| Lecteur | Plan gratuit | À savoir |
|---|---|---|
| [Inoreader](https://www.inoreader.com/pricing) | 150 flux | Sans publicité, même en gratuit |
| [Feedly](https://feedly.com/i/pro) | 100 flux, rangés dans 3 dossiers | Le plan Pro vend l'option « masquer les publicités sponsorisées », le gratuit en affiche donc |
| [NewsBlur](https://newsblur.com) | 64 sites | |
| [NetNewsWire](https://netnewswire.com) | Entièrement gratuit et open source | Sur Mac, iPhone et iPad |
| [FreshRSS](https://freshrss.org) | Gratuit et open source | À installer sur ton propre serveur |

Limites relevées sur la page officielle de chaque lecteur, à la même date.

## Les API et alertes gratuites, avec leurs limites

Une API, c'est un guichet où un programme vient chercher des données sans passer par la page web : c'est par là que passe toute veille automatisée.

| Outil | Coût | Ce qu'il apporte | Limite |
|---|---|---|---|
| API Hacker News (officielle et Algolia) | Gratuit, sans clé | Le temps réel, la meilleure base pour un flux automatisé | Pas de tri par thème, sauf avec la recherche Algolia |
| API Product Hunt | Gratuit, avec un jeton développeur | Les lancements du jour | Usage non commercial par défaut |
| API GitHub | Gratuit, avec des quotas | Dépôts récents par sujet, versions publiées | Nombre de requêtes limité |
| SEC EDGAR | Gratuit | Les formulaires 8-K, Form D et S-1 | Ton script doit se présenter avec un User-Agent qui donne un contact (sa carte de visite auprès du serveur), et pas plus de 10 requêtes par seconde |
| Google Alerts | Gratuit | Des alertes sur un mot-clé : une entreprise, un outil, une loi | Pertinence variable |
| NewsAPI | Gratuit en développement seulement | Des articles de presse agrégés | Articles retardés de 24 h, 100 requêtes par jour, interdit en production : inutile pour avoir de l'avance |
| API Anthropic | Payant à l'usage, facturé à part de l'abonnement Claude | Trier et rédiger le brief dans n8n ou dans un script | Un coût à mesurer sur ton propre volume |

Sources : les pages officielles de [NewsAPI](https://newsapi.org/pricing), de la [SEC](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) et de l'[API Product Hunt](https://api.producthunt.com/v2/docs), lues en octobre 2026.

## Trois montages selon le temps que tu peux y mettre

| Montage | Mise en place | Ce que tu montes | Pour qui |
|---|---|---|---|
| Minimum | Une soirée | Un lecteur RSS gratuit avec le fichier d'import, et un projet Claude « Veille » pour résumer quand tu en as envie | Tu veux lire mieux, sans rien automatiser |
| Équilibré | Un week-end | n8n collecte, dédoublonne et filtre les flux, range chaque alerte dans une base Notion et t'envoie les sources primaires sur Telegram ou Discord ; chaque matin, une IA lit la base et rédige le brief ; le dimanche, une synthèse de la semaine | Tu veux un brief qui t'attend au réveil |
| Maximum | Deux à trois semaines | L'équilibré, plus un brief rédigé par l'API, la surveillance des pages sans RSS, un fichier par jour versionné sur GitHub, une note « utile ou pas » sur chaque alerte et des flux Bluesky et YouTube | Ta veille nourrit ton métier ou ton contenu |

Si tu hésites, commence par le minimum : au bout d'une semaine, tu sauras si tu lis vraiment tes flux, et c'est la seule question qui compte avant d'automatiser. Le détail de chaque brique suit, l'IA d'abord, n8n ensuite.

## Faire son brief du matin avec une IA

### Ce qu'un bon brief contient

Les États-Unis dorment pendant que tu te lèves : un brief à 7 h 30 ou 8 h 30 capte donc la nuit américaine et le début de matinée européenne. San Francisco commence sa journée vers 17 h ou 18 h, heure de Paris, si bien que beaucoup d'annonces de la Silicon Valley tombent en fin d'après-midi ou le soir chez toi. Pour ne pas les rater, prévois un second passage en fin de journée, ou des alertes immédiates réservées aux sources primaires.

Pour tenir en cinq minutes de lecture, le brief suit toujours le même ordre. Il ouvre sur les trois infos à savoir aujourd'hui, passe une rubrique par zone ou par sujet (Silicon Valley, French Tech et Europe, IA, régulation, ton sujet de niche), propose trois pistes à creuser au plus et finit sur les signaux faibles. Le [prompt complet](#le-prompt-du-brief-prêt-à-coller) est plus bas.

Chaque info porte une étiquette de confiance : « Confirmé » quand elle vient de la source primaire ou d'au moins deux sources indépendantes, « À vérifier » quand un seul média la rapporte, « Rumeur » pour une fuite ou un post que personne n'a confirmé.

### Avec Claude, sans rien installer

| Façon | Comment | Limite |
|---|---|---|
| Un projet « Veille » dans Claude | Le prompt de ce guide en instructions, ta liste de flux en connaissances et la recherche web activée ; chaque matin, tu écris « Brief du jour » | Tu dois ouvrir la conversation, et la recherche web ne remplace pas un vrai dédoublonnage |
| Claude avec Gmail ou Notion | Tes newsletters rangées sous un libellé « Veille », puis « résume les mails du libellé Veille des dernières 24 h » ; le brief peut atterrir dans une page Notion | C'est toujours toi qui déclenches |
| Claude dans Chrome | « Ouvre ces cinq pages et dis-moi ce qui a changé depuis hier », pratique pour les sites sans RSS comme les pages tarifs | Manuel, page par page |

### Avec Claude Code, en une commande

Si tu travailles dans [Claude Code](https://code.claude.com/docs), une commande personnalisée `/veille` (un fichier `.claude/commands/veille.md`) peut lire ta liste de flux, garder les articles des dernières 24 heures et écrire un brief en Markdown dans un dossier `briefs/`. Pour qu'elle tourne sans toi, le mode non interactif `claude -p` lance une demande sans ouvrir l'interface ([documentation de Claude Code](https://code.claude.com/docs/en/headless)). Un planificateur la déclenche ensuite chaque matin : launchd sur Mac, cron sur Linux, le Planificateur de tâches sur Windows.

```bash
#!/bin/zsh
cd ~/veille
claude -p "$(cat prompt-veille.md)" > "briefs/$(date +%F).md"
```

Ce script est un point de départ à tester chez toi. Selon ta version de Claude Code, il faudra autoriser les outils dont Claude a besoin, comme la lecture du web ou l'écriture de fichiers. L'ordinateur doit aussi être allumé à l'heure dite, et l'usage non interactif compte dans ton abonnement : regarde comment ton offre le décompte avant d'automatiser.

### Avec un assistant IA qui t'envoie un brief à heure fixe

Certains assistants IA savent envoyer un brief programmé. Le partage des rôles qui tient la route confie la collecte, le dédoublonnage et le tri à n8n ou à un script, parce qu'un programme sans IA ne s'invente rien et va vite. L'assistant, lui, explique et relie l'actualité à tes projets. Pour lui donner sa matière, tu as le choix :

- une base Notion « Veille » que n8n remplit et que l'assistant lit avant son brief ;
- un fichier `veille/AAAA-MM-JJ.md` que n8n ou GitHub Actions dépose chaque jour dans un dépôt GitHub ;
- les flux eux-mêmes, si l'assistant sait ouvrir des adresses web : donne-lui le fichier OPML et demande-lui de lire les sources primaires en premier ;
- un brouillon produit par n8n à 7 h 45, que l'assistant réécrit à 8 h 30 avec ton angle et ton ton.

Sans sources précises (Légifrance, EUR-Lex, dossiers législatifs), ses alertes sur les lois en discussion resteront vagues. Et si ton assistant limite la longueur des messages, envoie le prompt de ce guide en trois fois, un bloc par message.

## Automatiser le tri avec n8n

[n8n](https://n8n.io) enchaîne des étapes automatiques, ce qu'on appelle un workflow, sans écrire de code. Cinq workflows couvrent toute la veille ; commence par le premier, les autres s'ajoutent quand il tourne.

| Workflow | Quand il tourne | Ce qu'il fait |
|---|---|---|
| A. Alertes | Toutes les 15 minutes | Lit les flux, garde le titre, le lien et la date, écarte les doublons, filtre par mots-clés et t'envoie le reste sur Telegram |
| B. Brief du matin | Chaque jour à 7 h 30 | Relit les 24 dernières heures, regroupe les articles d'une même histoire, fait noter leur pertinence de 1 à 5 par un petit modèle rapide (Haiku, chez Anthropic), garde les notes de 3 et plus, fait rédiger le brief par un modèle plus capable (Sonnet) et le publie dans Notion, sur GitHub, Discord ou Telegram |
| C. Boîte de réception Notion | À chaque alerte | Range l'alerte dans une base Notion « Veille » avec le statut « À lire » et une case « Utile ? », qui servira à affiner tes mots-clés |
| D. Synthèse du dimanche | Le dimanche à 18 h | Relit la semaine et dresse la carte des signaux faibles : ce qui revient, ce qui monte, ce qui retombe |
| E. Pages sans RSS | Une ou plusieurs fois par jour | Télécharge une page, la compare à la version précédente et t'alerte si elle a changé (pages tarifs, offres d'emploi) |

Pour le workflow E, Visualping ou changedetection.io font la même chose sans rien construire. Côté sortie, choisis un canal de lecture et un canal d'alerte, pas davantage : recevoir le même brief sur Telegram, Discord, Notion et par e-mail, c'est la meilleure façon de ne plus le lire nulle part. Pour faire tourner n8n chez toi, suis le tutoriel [Installer n8n avec Docker](../tutoriels/installer-n8n-docker.md).

## Les sources que la plupart des veilles oublient

| Idée | Comment faire |
|---|---|
| Les newsletters dans ton lecteur | Feeder, même en gratuit, reçoit les newsletters par e-mail et les range comme des flux, ce qui règle le cas des sources sans RSS |
| Google Alerts en flux | Crée une alerte sur un nom d'entreprise, d'outil ou de loi, et choisis la remise en flux RSS si ton compte te la propose |
| Bluesky et Mastodon | Chaque profil a son flux : `https://bsky.app/profile/HANDLE/rss` chez Bluesky, l'adresse du profil suivie de `.rss` chez Mastodon |
| YouTube et les podcasts | Chaque chaîne YouTube a son flux (`https://www.youtube.com/feeds/videos.xml?channel_id=ID`), chaque podcast en est un ; Claude peut ensuite en résumer la transcription |
| Reddit | Ajoute `.rss` à l'adresse d'un subreddit, par exemple `https://www.reddit.com/r/LocalLLaMA/.rss` |
| Les offres d'emploi | Surveille les pages carrières d'une dizaine d'entreprises : celle qui recrute dix ingénieurs hardware prépare un virage |
| Les sites sans flux | RSS-Bridge (open source, à héberger), RSS.app, ou les 3 flux IA du plan gratuit de Feeder |
| L'écoute | Le mode vocal de l'app Claude pour te faire lire le brief en préparant ton café, ou NotebookLM pour transformer une sélection de sources en audio |

## Le prompt du brief, prêt à coller

Il se colle dans un projet Claude, dans les instructions de ton assistant ou dans l'étape de rédaction de n8n. Remplace ce qui est entre accolades, et garde les trois blocs séparés : chacun tient dans un message, même chez un assistant qui limite la longueur.

Bloc 1, le contexte :

```text
Tu es mon analyste de veille. Nous sommes le {date}, heure de Paris.
Je suis {ton métier} et je travaille sur {tes projets}.
Mes priorités : Silicon Valley, French Tech, IA (modèles, agents, outils),
régulation (France et Europe), {ton sujet de niche}.
```

Bloc 2, les règles :

```text
Appuie-toi UNIQUEMENT sur les éléments fournis ci-dessous ou sur ceux
que tu as trouvés avec un lien. Chaque affirmation doit avoir son lien.
Étiquette chaque information : Confirmé (source primaire ou deux sources
indépendantes), À vérifier (une seule source média), Rumeur.
Si une source primaire existe, cite-la avant les médias.
Si rien de nouveau, dis-le : ne remplis pas pour faire du volume.
```

Bloc 3, le format :

```text
Brief de 5 minutes de lecture (environ 700 mots) :
1. Les 3 à savoir aujourd'hui
2. Silicon Valley
3. French Tech et Europe
4. IA : modèles, outils, agents
5. Régulation et opportunités
6. {Ton sujet de niche}
7. À creuser aujourd'hui (3 maximum) et le lien avec mes projets
8. Signaux faibles
Ton direct et chaleureux, une pointe d'humour.
```

## Les pièges d'une veille trop rapide

| Piège | Parade |
|---|---|
| Une source primaire brute, personne ne l'a vérifiée : un 8-K mal lu, une version de code abandonnée, un faux compte | Une étiquette de confiance sur chaque info, gardée jusqu'à preuve du contraire |
| Une IA peut inventer | Lui imposer de ne résumer que des liens fournis, et ouvrir toi-même les liens des trois infos du jour avant de les citer en public |
| Sans tri, des centaines de titres par jour | Démarrer à 20 flux plutôt qu'à 100, parce que le tri compte plus que le nombre de sources |
| Vouloir battre les embargos | Gagner plutôt sur ce que les rédactions regardent peu : les niches, les sources primaires ignorées, la France |
| Des flux qui changent d'adresse | Une vérification une fois par mois |
| Aspirer des pages avec un robot (scraping) | Préférer les flux, les API officielles et les données ouvertes, et respecter les conditions des sites |
| Des coûts d'API qui grimpent | Mesurer ton usage pendant deux semaines avant d'automatiser |
| Un brief que tu ne lis plus | Cinq minutes le matin et une synthèse le dimanche, pas davantage |

Deux habitudes rendent la veille plus fiable avec le temps. Dès qu'une rumeur t'arrive, colle-la à Claude avec la consigne « trouve une source primaire ou deux sources indépendantes, sinon dis-moi que ce n'est pas confirmé ». Et relis le brief du matin en fin de journée pour voir quelles rumeurs se sont confirmées : c'est comme ça que tu apprends quelles sources méritent ta confiance.

## Ta première semaine, jour par jour

1. Jour 1 : un compte gratuit sur un lecteur RSS, le fichier OPML importé, les quatre flux d'avance épinglés en tête.
2. Jour 2 : un projet Claude « Veille » avec le prompt de ce guide, testé trois matins de suite.
3. Jour 3 : n8n installé, le workflow d'alertes branché sur Telegram avec les flux du fichier OPML.
4. Jour 4 : la base Notion « Veille » créée et reliée au workflow.
5. Jour 5 : ton projet Claude ou ton assistant IA branché sur cette base pour le brief du matin, prompt ajusté.
6. Jour 6 : un seul endroit choisi pour lire le brief chaque matin, et tous les autres coupés.
7. Jour 7 : la semaine relue, les flux inutiles supprimés, les mots-clés ajustés, et la décision de passer ou non au brief rédigé par l'API.

## Sources et vérifications

Ce qui a été vérifié le 30 octobre 2026 :

- les 27 flux du fichier d'import, les 9 flux à ajouter à la main et les adresses d'exemple (recherche Hacker News, Reddit, Bluesky, YouTube, versions GitHub) ont été ouverts un par un et renvoient un flux ou des données valides, après correction de l'adresse de French Tech Journal ;
- les tarifs et limites des lecteurs ont été relus sur les pages officielles de [Feeder](https://feeder.co/pricing), [Inoreader](https://www.inoreader.com/pricing), [Feedly](https://feedly.com/i/pro), [NewsBlur](https://newsblur.com) et [NetNewsWire](https://netnewswire.com) ;
- les règles d'accès viennent des pages de [NewsAPI](https://newsapi.org/pricing), de la [SEC](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data), de l'[API Product Hunt](https://api.producthunt.com/v2/docs) et de la [documentation de Claude Code](https://code.claude.com/docs/en/headless).

Ce qui n'a pas été vérifié : l'option de remise en flux RSS de Google Alerts (elle n'apparaît qu'une fois connecté à un compte Google), les conditions des API françaises (BODACC, Pappers) et les fonctions de planification propres à chaque assistant IA. Les outils changent vite : en cas de doute, la page officielle a le dernier mot.

**Ailleurs dans la Toolbox**

- n8n chez toi en une commande → [Installer n8n avec Docker](../tutoriels/installer-n8n-docker.md)
- Ranger tes infos avec n8n, Notion et Airtable → [S'organiser avec n8n, Notion et Airtable](../tutoriels/tutoriels-par-profil.md#sorganiser-avec-n8n-notion-et-airtable)
- Ce que Claude Code et n8n savent faire, et pour qui → [La boîte à outils IA](./boite-a-outils-ia.md)
- Vérifier ce qu'un agent dit avoir fait → [Prompt maître du harnais](../prompts/prompt-maitre-harnais.md)
- Les outils design et IA déjà triés → [la veille](../veille/)

---

*Par Opaline, Antidote.AI · Vérifié le 30 octobre 2026 · Sous licence [CC BY 4.0](../LICENSE)*
