# Plugin Marketing <!-- omit in toc -->

Le contexte business et les règles de voix de Solecooler, combinés à plus de 20 skills marketing pour la création de contenu, la recherche, la stratégie et l'édition — avant tout conçus pour [Claude Cowork](https://claude.com/product/cowork), l'application de bureau agentique d'Anthropic. Fonctionne aussi dans Claude Code.

- [Installation et mises à jour](#installation-et-mises-à-jour)
- [Ce que fait le plugin](#ce-que-fait-le-plugin)
- [Skills](#skills)
  - [✍️ Rédaction de contenu](#️-rédaction-de-contenu)
  - [🧠 Recherche, stratégie et décisions](#-recherche-stratégie-et-décisions)
  - [🎨 Design, édition et finition](#-design-édition-et-finition)
  - [⚙️ Configuration et méta](#️-configuration-et-méta)
  - [🔍 SEO](#-seo)
  - [📚 Skills de contexte (non invocables)](#-skills-de-contexte-non-invocables)
- [Sources de données](#sources-de-données)
- [Premiers pas](#premiers-pas)

## Installation et mises à jour

**Installer :** voir [Installation](../../README.md#installation) dans le README principal.

**Connectez vos outils :** voir [Connectez vos outils](../../README.md#connectez-vos-outils-optionnel) dans le README principal — optionnel, mais nécessaire pour les brouillons Gmail, les enregistrements Drive, les envois vers HubSpot et les partages Slack.

**Mettre à jour :** voir [Mises à jour](../../README.md#mises-à-jour) dans le README principal.

## Ce que fait le plugin

Le plugin superpose le contexte business et les règles de voix de Solecooler à une bibliothèque complète de plus de 20 skills marketing — couvrant la création de contenu, la recherche, la stratégie et l'édition — pour que les collègues produisent d'excellents résultats sans briefer Claude de zéro à chaque fois.

- **Charger le contexte d'entreprise** — produits, prix, ICP, concurrents et preuves nommées comme connaissance de fond pour toute tâche marketing
- **Garantir la cohérence de la voix** — un ensemble partagé de règles de rédaction, de directives de ton et de phrases interdites en tolérance zéro que tout contenu Solecooler doit respecter
- **Intégrer les collègues** — un entretien guidé qui produit un calque d'Instructions globales personnalisé, étendant le contexte partagé avec le rôle, les preuves et les nuances de voix de chacun
- **Créer du contenu** — landing pages, séquences d'e-mails, newsletters, posts LinkedIn, posts Twitter/X, et plus encore
- **Recherche et stratégie** — recherche de mots-clés, audits SEO, architecture d'offre et conception de lead magnets
- **Affiner et réutiliser** — passes d'édition, nettoyage anti-slop et réutilisation de contenu multi-canal
- **Connecter vos outils** — récupérer du contexte depuis les contacts HubSpot, les briefs Google Drive et les données d'agenda dans n'importe quel skill, et renvoyer les résultats sous forme de brouillons Gmail, de fichiers Drive, d'événements d'agenda ou de messages Slack — toujours avec votre confirmation explicite avant que quoi que ce soit ne quitte la conversation

## Skills

### ✍️ Rédaction de contenu

| Skill | Description |
| --- | --- |
| `/landing-page` | Pages de vente longues avec le framework en 5 parties |
| `/copywriting` | Copy de conversion générale : sections héros, e-mails, CTA, pubs, social |
| `/newsletter` | Éditions de newsletter prêtes à publier (framework en 8 étapes) |
| `/email-sequence` | Séquences d'e-mails de bienvenue / nurturing / lancement / réactivation |
| `/x-article` | Articles longs X/Twitter — tutoriels et décryptages |
| `/linkedin-post` | Posts LinkedIn à partir de vidéos YouTube, d'articles ou d'idées brutes |
| `/linkedin-comment` | Commentaires sur les posts LinkedIn des autres, lus et générant leur propre portée |
| `/x-longform-tweet` | Posts X longs à fort engagement, avec des structures éprouvées |
| `/viral-hooks` | Accroches X/LinkedIn qui arrêtent le scroll, avec 140+ patterns éprouvés |
| `/repurpose` | Transformer une source en posts natifs pour LinkedIn, X, Instagram, TikTok, YouTube |

### 🧠 Recherche, stratégie et décisions

| Skill | Description |
| --- | --- |
| `/keyword-research` | Recherche de mots-clés + plan de contenu, sans outil payant |
| `/interesting` | Affûter des idées fades en angles percutants |
| `/offer-architect` | Conception d'offre : Shell, Map, Protagonist, 90 Days of Offers |
| `/lead-magnet` | Concepts de lead magnets + brouillons de contenu complets |
| `/llm-council` | Stress-tester une décision via 5 conseillers IA + relecture croisée + verdict du président |

### 🎨 Design, édition et finition

| Skill | Description |
| --- | --- |
| `/frontend` | Construire des UI distinctives et de qualité production (HTML, React, Vue) |
| `/editing` | Framework d'édition en 9 passes — couper le superflu, affûter la voix |
| `/antislop` | Retirer les tournures qui sentent l'IA — passe finale obligatoire sur chaque texte produit |

### ⚙️ Configuration et méta

| Skill | Description |
| --- | --- |
| `/personal-interview` | Intégrer un collègue Solecooler avec un entretien de 5 questions et produire son calque d'Instructions globales personnalisé |
| `/business-interview` | Entretien de 11 questions qui construit vos Instructions globales / CLAUDE.md complets |
| `/skill-creator` | Créer des skills de zéro ou à partir de contenu existant, avec des boucles d'évaluation pour les améliorer |
| `/skill-creator-interview` | Extraire les workflows de votre tête vers de nouveaux fichiers de skill |

### 🔍 SEO

| Skill | Description |
| --- | --- |
| `/seo-audit` | Audit SEO on-page avec des correctifs priorisés (sans outil externe) |

### 📚 Skills de contexte (non invocables)

> [!NOTE]
> Ces skills sont chargés automatiquement par d'autres skills. Les invoquer
> directement comme commandes slash n'a aucun effet.

Ces skills sont chargés automatiquement par d'autres skills. Ils ne sont pas appelables directement.

| Skill | Description |
| --- | --- |
| `company-context` | Catalogue produits, prix, ICP, faiblesses des concurrents et preuves nommées de Solecooler |
| `company-instructions` | Voice DNA, règles de rédaction, règles de mise en forme et phrases interdites en tolérance zéro, à l'échelle de l'entreprise |

## Sources de données

Connectez votre messagerie, votre CRM, votre bibliothèque de contenu et vos outils de communication pour un contexte marketing complet et une automatisation maximale des workflows. Sans eux, fournissez le contexte et partagez les résultats manuellement.

**Connecteurs inclus :**

Les outils suivants peuvent être connectés et utilisés avec ce plugin. Les skills y font référence par des noms d'espace réservé (par ex. `~~crm`) qui correspondent aux clés des serveurs MCP configurées dans [`.mcp.json`](.mcp.json).

- Messagerie (`~~email`) pour les brouillons de campagne et la correspondance avec l'audience
- Agenda (`~~calendar`) pour planifier le contenu et les calendriers de campagne
- Stockage cloud (`~~cloud-storage`) pour les assets de marque, les briefs et le contenu publié
- CRM (`~~crm`) pour les données d'audience, les listes de contacts et le contexte des deals
- Chat (`~~chat`) pour distribuer les brouillons et les discussions marketing internes

> [!NOTE]
> Voir [CONNECTORS.md](CONNECTORS.md) pour vérifier les noms et sources exacts des outils préconfigurés pour chaque catégorie et explorer les alternatives possibles.

## Premiers pas

Voir [TUTORIAL.md](TUTORIAL.md) pour un guide pas à pas — installer le plugin, configurer votre calque de contexte personnel, puis parcourir des ateliers qui vont de la recherche d'audience aux landing pages finies et conformes à la marque.
