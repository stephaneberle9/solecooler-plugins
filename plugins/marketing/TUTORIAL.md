# Plugin Marketing — Tutoriel <!-- omit in toc -->

Guide pas à pas du plugin marketing Solecooler. Parcourez les labs dans l'ordre la première fois, puis allez directement à celui qui vous intéresse. Les labs 1 à 6 construisent le moteur grand public (de la recherche d'audience à l'offre et à la distribution) ; le lab 7 prépare une page de lancement et fait la transition vers les labs 8 et 9, qui ouvrent les canaux B2B et médical autour de WarnFeet.

- [Configuration](#configuration)
- [Découvrir Cowork](#découvrir-cowork)
- [Votre contexte personnel](#votre-contexte-personnel)
- [Le moteur grand public](#le-moteur-grand-public)
  - [Lab 1 : Rechercher les points de douleur de l'audience](#lab-1--rechercher-les-points-de-douleur-de-laudience)
  - [Lab 2 : Recherche de mots-clés et plan de contenu](#lab-2--recherche-de-mots-clés-et-plan-de-contenu)
  - [Lab 3 : Concevoir un lead magnet qui segmente](#lab-3--concevoir-un-lead-magnet-qui-segmente)
  - [Lab 4 : Séquence e-mail de bienvenue via les connecteurs](#lab-4--séquence-e-mail-de-bienvenue-via-les-connecteurs)
  - [Lab 5 : Architecturer une offre saisonnière](#lab-5--architecturer-une-offre-saisonnière)
  - [Lab 6 : Décliner un contenu sur tous les canaux](#lab-6--décliner-un-contenu-sur-tous-les-canaux)
- [Préparer le lancement](#préparer-le-lancement)
  - [Lab 7 : Construire une landing page de pré-lancement](#lab-7--construire-une-landing-page-de-pré-lancement)
  - [Lab 7.1 : Habiller la landing page à la marque](#lab-71--habiller-la-landing-page-à-la-marque)
- [Les canaux B2B et médical](#les-canaux-b2b-et-médical)
  - [Lab 8 : Toucher la distribution et les acheteurs B2B sur LinkedIn](#lab-8--toucher-la-distribution-et-les-acheteurs-b2b-sur-linkedin)
  - [Lab 9 : Raconter l'histoire WarnFeet au public médical](#lab-9--raconter-lhistoire-warnfeet-au-public-médical)
- [Aller plus loin](#aller-plus-loin)
  - [Lab 10 : Créer votre propre skill](#lab-10--créer-votre-propre-skill)
- [D'autres labs à venir](#dautres-labs-à-venir)

## Configuration

À faire une fois. Tous les labs en dépendent.

### Prérequis <!-- omit in toc -->

- [ ] **Système à jour sur votre ordinateur** — Windows ou macOS dans sa dernière version, toutes les mises à jour installées, et redémarré si nécessaire
- [ ] **Claude Desktop** installé et à jour — [claude.ai/download](https://claude.ai/download) (Mac + Windows)
- [ ] **Un abonnement Claude personnel (Pro ou Max)** — Cowork fonctionne avec les plans personnels Pro et Max ; abonnez-vous sur [claude.ai](https://claude.ai) si vous n'en avez pas encore

### Étape 1 : Installer le plugin <!-- omit in toc -->

**Ajouter la marketplace (une seule fois) :**

1. Ouvrez Claude Desktop et allez dans l'onglet **Cowork**
2. Cliquez sur **Personnaliser** dans la barre latérale gauche
3. Sous **Plugins personnels**, cliquez sur **+** → **Créer un plugin** → **Ajouter une marketplace**
4. Collez : `https://github.com/solecooler/solecooler-plugins.git`
5. Cliquez sur **Synchroniser** — suivez les instructions à l'écran pour autoriser l'accès à GitHub

**Parcourir et installer le plugin :**

1. Cliquez sur **+** → **Parcourir les plugins**
2. Cliquez sur l'onglet **Personnel**
3. Sélectionnez la marketplace **solecooler-plugins**
4. Cliquez sur **Marketing** puis sur **Installer**

### Étape 1.1 : Garder le plugin à jour <!-- omit in toc -->

Allez dans **Personnaliser** → **Plugins personnels** → cliquez sur **Marketing** dans la barre latérale.

- **Si le bouton Mettre à jour est actif** — cliquez sur **Mettre à jour**. Cela récupère les nouvelles versions officielles.
- **Si le bouton Mettre à jour est grisé** — le numéro de version n'a pas changé, mais les skills ont peut-être tout de même été mis à jour. Cliquez sur **Désinstaller**, puis réinstallez en suivant l'étape 1 ci-dessus pour récupérer le contenu le plus récent.

### Étape 2 : Connectez vos outils (optionnel) <!-- omit in toc -->

> [!NOTE]
> Cette étape est optionnelle. Tous les skills fonctionnent sans connecteurs — les résultats restent dans la conversation et vous les copiez manuellement. Les connecteurs ajoutent la possibilité de récupérer des données en direct et de renvoyer le résultat directement vers vos outils. N'hésitez pas à sauter cette étape et à y revenir plus tard quand vous serez prêt.

Avec les connecteurs, les skills peuvent récupérer du contexte depuis vos outils externes et y renvoyer des résultats — lire des contacts HubSpot, récupérer des briefs Drive, rédiger dans Gmail, créer des événements d'agenda ou publier sur Slack.

Chaque connecteur nécessite deux étapes : **Installer** et **Connecter** (authentifier).

1. Cliquez sur **Personnaliser** dans la barre latérale gauche
2. Sous **Plugins personnels**, sélectionnez **Marketing** → **Connecteurs**
3. Pour chaque connecteur, vérifiez son état et agissez :
   - Bouton **Installer** → cliquez pour installer
   - Bouton **Connecter** → cliquez pour authentifier (OAuth ou demandes de connexion)
   - Aucun bouton → déjà connecté, rien à faire
4. Répétez pour chaque connecteur : Gmail, Google Drive, Google Calendar, HubSpot, Slack

> [!NOTE]
> Certains connecteurs peuvent déjà être présents — apportés par un autre plugin ou configurés à l'échelle de l'organisation par votre administrateur Claude AI. Si un connecteur n'affiche aucun bouton, c'est qu'il est déjà connecté ; il vous suffit peut-être de le connecter, sans l'installer.
>
> Quand un skill propose une action de connecteur (par ex. « Rédiger dans Gmail ? »), il demande toujours votre confirmation. Refusez et il garde tout dans la conversation.

---

## Découvrir Cowork

Trois concepts qui structurent le fonctionnement de tout le reste. Une fois compris, les labs prendront sens.

**1. Les tâches pour démarrer vite, les projets pour rester organisé**
Cowork vous laisse travailler en **tâches** ou en **projets**. Une tâche est un chat rapide : vous l'ouvrez, vous travaillez, vous la fermez. Le fil reste tant que vous ne le supprimez pas — mais c'est une conversation isolée qui s'allonge et devient de moins en moins organisée si vous y travaillez longtemps.

Un projet regroupe toutes les conversations d'un même sujet, garde les fichiers et l'historique d'une session à l'autre, et se reprend là où vous l'aviez laissé — on s'y retrouve plus facilement et on garde une bien meilleure vue d'ensemble. Utilisez un projet par sujet (par ex. « ClimFeet Hiver », « Lancement WarnFeet ») et gardez tout ce qui concerne ce sujet à l'intérieur.

> [!TIP]
> **Vous changez de sujet ?** Ouvrez un autre projet. Chacun porte son propre brief, ses fichiers et son historique de conversation.

**2. Claude travaille dans un dossier local.**
Chaque tâche et chaque projet a un répertoire de travail. Claude peut lire, écrire et créer des fichiers librement dans ce dossier — et nulle part ailleurs. Tout le résultat atterrit là. Choisissez un dossier explicite que vous saurez retrouver (par ex. dans Documents) plutôt que de vous fier au dossier par défaut.

> [!NOTE]
> Si vous ne choisissez pas de dossier, Cowork utilise un dossier par défaut dans sa zone de données : `%APPDATA%\Claude` sur Windows, `~/Library/Application Support/Claude` sur macOS. Les dossiers par défaut des projets portent le nom du projet ; ceux des simples tâches reçoivent un nom générique.

**3. Le contexte se charge en trois couches — automatiquement.**
Vous n'avez pas besoin de briefer Claude de zéro à chaque fois. Trois couches de contexte s'empilent et garantissent que Claude sait beaucoup de choses avant même que vous tapiez un seul mot :

| Couche | Ce qu'elle apporte | Comment |
| --- | --- | --- |
| **Skills du plugin** | Produits Solecooler, ICP, règles de voix, phrases interdites | Chargés automatiquement (`company-context` + `company-instructions`) |
| **Instructions globales** | Votre rôle, vos domaines de focus, votre calque de voix personnel | Défini une fois dans [Votre contexte personnel](#votre-contexte-personnel) via `/personal-interview` |
| **Instructions du projet** | Brief spécifique au sujet : audience, angle, contraintes | Ouvrir le projet → panneau de droite → **Instructions** → icône de modification |

**Comment définir les Instructions du projet :** ouvrez votre projet → dans le panneau de droite, trouvez la section **Instructions** → cliquez sur l'icône de modification → collez un brief en texte brut → enregistrez. Exemple :

> *« Contenu sur les semelles chauffantes pour le travail en extérieur. Audience : ouvriers du BTP, frigoristes et pompiers exposés au froid prolongé. Focus : confort et sécurité sur le terrain, preuves concrètes (plage de température, durée). Ton : pair de terrain, pas commercial. »*

---

## Votre contexte personnel

La dernière couche de configuration : apprenez à Claude qui *vous* êtes, puis vérifiez que tout est en place.

### Étape 3 : Ajouter votre contexte personnel <!-- omit in toc -->

Le plugin inclut déjà deux couches de contexte partagé qui se chargent automatiquement chaque fois que vous invoquez un skill marketing : `company-context` (produits, prix, ICP, concurrents et preuves nommées) et `company-instructions` (Voice DNA, règles de rédaction et phrases interdites en tolérance zéro).
Ce dont vous avez besoin, c'est un calque personnel : votre rôle, vos domaines de focus et votre voix. Le skill `/personal-interview` vous guide à travers cinq questions rapides et produit le calque pour vous.

1. Ouvrez une **nouvelle** tâche Cowork
2. Tapez `/personal-interview` et appuyez sur **Entrée**
3. Répondez aux 5 questions (environ 3 minutes)
4. Quand Claude affiche le bloc markdown résultant à la fin, copiez-le dans le presse-papiers

Puis enregistrez-le dans les Instructions globales :

1. Cliquez sur votre **profil** (en bas à gauche) → **Paramètres**
2. Allez dans **Cowork** → **Instructions globales**
3. Cliquez sur **Modifier**
4. Collez le bloc → **Enregistrer**

> [!TIP]
> **Vous avez déjà des Instructions globales ?** N'écrasez rien. Dites à Claude : « Voici mes Instructions globales actuelles : [collez]. Voici les nouvelles : [collez]. Fusionne-les en gardant le meilleur des deux. » Puis collez la version fusionnée.

### Étape 4 : Vérifier que ça a marché <!-- omit in toc -->

1. Ouvrez un **nouveau** chat Cowork (pas le même — un chat neuf)
2. Demandez à Claude : **« Qui suis-je ? »**
3. Claude devrait répondre avec votre rôle, vos domaines de focus et le contexte Solecooler — sans briefing.

Si ce n'est pas le cas, les Instructions globales n'ont pas été enregistrées. Revenez à l'étape 3.

---

## Le moteur grand public

De la recherche d'audience à l'offre et à la distribution — la chaîne qui transforme un visiteur en client.

### Lab 1 : Rechercher les points de douleur de l'audience

**Ce que vous allez produire :** un dossier `research/` avec un `.csv` de points de douleur réels et de lacunes des concurrents, tirés d'avis, de forums et des réseaux sociaux — pour un segment d'audience Solecooler (runners, frigoristes, pompiers, pieds froids).

#### Étapes <!-- omit in toc -->

1. Ouvrez Claude Desktop → onglet **Cowork**
2. Cliquez sur **Projets** → **Nouveau projet** → **Partir de zéro**
3. Donnez un nom au projet (par ex. « Recherche ClimFeet »)
4. Choisissez un dossier local comme répertoire de travail — tout le résultat (comme le sous-dossier `research/`) y sera créé
5. Remplissez les trois espaces réservés du prompt ci-dessous, collez le tout dans Cowork et appuyez sur **Entrée**

#### Prompt <!-- omit in toc -->

```text
Cherche sur le web ce qui pose problème, frustre, et ce que les gens cherchent activement à résoudre autour des pieds froids ou trop chauds pour [VOTRE SEGMENT D'AUDIENCE, par ex. les runners, les frigoristes, les pompiers, les personnes à mauvaise circulation]. Trouve des points de douleur réels, des plaintes et des besoins non satisfaits dans les avis, forums et réseaux sociaux. Recherche aussi [CONCURRENT 1, par ex. les semelles chauffantes à batterie] et [CONCURRENT 2, par ex. les chauffe-pieds chimiques jetables] — que disent leurs clients ? Qu'est-ce qui manque (autonomie, recharge, chaleur seulement, déchets) ? Crée un sous-dossier nommé `research/` dans le répertoire de travail du projet et enregistre les résultats dans UN SEUL CSV. N'inclus que des points de douleur appuyés par une source réelle — avis, fils de forum, posts précis. N'invente jamais de citations clients ni de statistiques.

Ne continue que si tous les espaces réservés sont remplis. Sinon, rappelle-moi de te donner plus d'informations.
```

#### Résultat attendu <!-- omit in toc -->

Vous devriez voir un sous-dossier `research/` dans votre répertoire de travail, contenant un fichier `.csv`. Double-cliquez pour l'ouvrir dans Excel, Numbers ou Google Sheets.

> [!TIP]
> **Envie d'aller plus loin ?** Demandez à Claude de prendre votre CSV et de construire une page interactive de comparaison avec les semelles à batterie et les chauffe-pieds chimiques. Enregistrez-la en fichier HTML et ouvrez-la dans votre navigateur.

---

### Lab 2 : Recherche de mots-clés et plan de contenu

**Ce que vous allez produire :** un plan de contenu scoré — clusters de mots-clés organisés en thèmes, avec intention, format et un calendrier de publication sur 90 jours — pour capter le trafic de recherche.

> [!TIP]
> **Idée clé :** en vente directe, le SEO est le moteur de trafic. `/keyword-research` transforme le langage réel de votre audience (et la recherche du Lab 1) en plan de contenu, sans aucun outil payant. Il couvre tout l'entonnoir : « comment éviter les pieds froids au travail » (haut), « meilleures semelles chauffantes pour la course » (milieu), « acheter semelles ClimFeet » (bas).

#### Étapes <!-- omit in toc -->

1. Restez dans le projet Cowork du [Lab 1](#lab-1--rechercher-les-points-de-douleur-de-laudience) (le skill réutilise le contexte Solecooler et la recherche du dossier `research/`)
2. Remplissez les espaces réservés dans le prompt ci-dessous, collez-le dans Cowork et appuyez sur **Entrée**

#### Prompt <!-- omit in toc -->

```text
Construis un plan de mots-clés et de contenu pour [VOTRE PRODUIT/GAMME, par ex. les semelles ClimFeet]. Appuie-toi sur le contexte Solecooler et sur la recherche du dossier `research/`. Vendu à : [VOTRE AUDIENCE PRINCIPALE]. URL actuelle : [URL DE LA PAGE PRODUIT, ou « aucune pour l'instant »]. Objectif : [trafic / ventes / autorité]. Concurrents : [CONCURRENT 1], [CONCURRENT 2]. Mets en avant l'angle défendable de Solecooler (chauffe ET rafraîchit, sans batterie ni produit chimique, alimenté par les pas). Utilise /keyword-research.

Ne continue que si tous les espaces réservés sont remplis. Sinon, rappelle-moi de te donner plus d'informations.
```

#### Résultat attendu <!-- omit in toc -->

Un plan de contenu : un résumé des plus grosses opportunités et du premier coup à jouer, des tables par thème (intention + format), et un calendrier de publication sur 90 jours.

> [!TIP]
> **Poussez plus loin :** si vous avez connecté Google Drive ou Google Calendar (Configuration [Étape 2](#étape-2--connectez-vos-outils-optionnel)), le skill propose d'enregistrer le plan dans Drive ou de créer les événements du calendrier de publication directement dans votre agenda.

---

### Lab 3 : Concevoir un lead magnet qui segmente

**Ce que vous allez produire :** 3 à 5 concepts de lead magnet, puis le contenu complet de celui que vous choisissez — par exemple un quiz « Quel est votre type de pieds froids ? » qui capte l'e-mail **et** oriente chaque personne vers la bonne variante (ClimFeet, ClimFeet Perf ou ClimFeet+).

> [!TIP]
> **Idée clé :** un produit qui sert plusieurs audiences (runners, ouvriers en extérieur, circulation) a besoin de **segmenter**. Un quiz ou une checklist fait deux choses à la fois : il construit la liste e-mail et il recommande la bonne semelle selon le profil.

#### Étapes <!-- omit in toc -->

1. Restez dans le projet Cowork d'un lab précédent (ou ouvrez un nouveau projet)
2. Remplissez les espaces réservés dans le prompt ci-dessous, collez-le dans Cowork et appuyez sur **Entrée**

#### Prompt <!-- omit in toc -->

```text
Propose des concepts de lead magnet pour [VOTRE GAMME, par ex. les semelles ClimFeet]. Le but : capter l'e-mail de prospects froids et segmenter les personas (runner, ouvrier en extérieur, pompier/frigoriste, pieds froids/mauvaise circulation), puis orienter chacun vers la bonne variante (ClimFeet, ClimFeet Perf, ClimFeet+). La douleur n°1 que je veux résoudre tout de suite : [DOULEUR #1]. Quand j'ai choisi un concept, rédige son contenu complet. Utilise /lead-magnet.

Ne continue que si tous les espaces réservés sont remplis. Sinon, rappelle-moi de te donner plus d'informations.
```

#### Résultat attendu <!-- omit in toc -->

3 à 5 concepts de lead magnet (format, angle, promesse, pont vers l'offre payante), puis le contenu complet du concept retenu — titre, intro, sections, et CTA vers la bonne variante ClimFeet.

> [!TIP]
> **Prêt à le mettre en ligne ?** Avec HubSpot ou Google Drive connecté (Configuration [Étape 2](#étape-2--connectez-vos-outils-optionnel)), le skill propose de créer la liste/le formulaire associé ou d'enregistrer le contenu dans Drive. Ce lead magnet alimente directement la séquence d'e-mails du [Lab 4](#lab-4--séquence-e-mail-de-bienvenue-via-les-connecteurs).

---

### Lab 4 : Séquence e-mail de bienvenue via les connecteurs

**Ce que vous allez produire :** une séquence de bienvenue de 5 e-mails — rédigée directement dans Gmail sous forme de brouillons individuels — qui délivre le lead magnet du [Lab 3](#lab-3--concevoir-un-lead-magnet-qui-segmente) et amène vers le bon produit ClimFeet.

> [!TIP]
> **Idée clé :** les skills peuvent écrire dans vos outils externes. À la fin de `/email-sequence`, Claude demande s'il faut sortir la séquence en texte ou rédiger chaque e-mail directement dans Gmail. Vous décidez — rien n'est envoyé ni enregistré sans votre confirmation.
>
> **Prérequis :** [Étape 2](#étape-2--connectez-vos-outils-optionnel) — connectez Gmail avant de faire ce lab.

#### Avant de commencer <!-- omit in toc -->

- [ ] Gmail est connecté dans Cowork → plugin Marketing → Connecteurs
- [ ] Vous savez quel lead magnet (Lab 3) et quel produit la séquence accompagne

#### Étapes <!-- omit in toc -->

1. Restez dans le projet Cowork d'un lab précédent (ou créez un nouveau projet)
2. Remplissez les espaces réservés dans le prompt ci-dessous, collez-le dans Cowork et appuyez sur **Entrée**
3. Quand `/email-sequence` demande le format de livraison au début, dites : **« Rédige chaque e-mail directement dans Gmail »**
4. Une fois la séquence écrite, confirmez quand on vous le demande
5. Vérifiez Gmail → Brouillons pour 5 nouveaux brouillons d'e-mail

#### Prompt <!-- omit in toc -->

```text
Écris une séquence de bienvenue de 5 e-mails pour les nouveaux abonnés qui ont téléchargé [LE LEAD MAGNET DU LAB 3, par ex. le quiz « type de pieds froids »]. L'audience est [VOTRE AUDIENCE]. Amène progressivement vers [VOTRE PRODUIT, par ex. la bonne variante ClimFeet]. Utilise les règles de voix partagées de Solecooler et mon contexte personnel.

Utilise /email-sequence.

Ne continue que si tous les espaces réservés sont remplis. Sinon, rappelle-moi de te donner plus d'informations.
```

#### Résultat attendu <!-- omit in toc -->

Cinq brouillons d'e-mail dans votre dossier Brouillons Gmail, prêts à relire, éditer et envoyer. Chaque e-mail doit avoir un objet et un corps complets — pas d'espaces réservés sauf si vous avez laissé un placeholder vide.

> [!TIP]
> **Pas de Gmail connecté ?** Le skill se termine normalement et sort la séquence complète en texte. Connectez Gmail plus tard et relancez-le pour obtenir la version brouillon.

---

### Lab 5 : Architecturer une offre saisonnière

**Ce que vous allez produire :** un package d'offre prêt à copier — une gamme de tiers (semelle d'entrée, bundle pro, abonnement de remplacement) avec une accroche « Pourquoi maintenant » saisonnière.

> [!TIP]
> **Idée clé :** `/offer-architect` empile des tiers de prix et crée l'urgence. Pour Solecooler : ClimFeet d'entrée pour le premier achat, un bundle « Pro froid extrême » (pompiers, frigoristes), et un abonnement de remplacement pour les semelles qui s'usent. L'angle « Pourquoi maintenant » s'appuie sur la saison (l'hiver arrive) ou le stock limité.

#### Étapes <!-- omit in toc -->

1. Restez dans un projet Cowork d'un lab précédent (ou créez un nouveau projet)
2. Remplissez les espaces réservés dans le prompt ci-dessous, collez-le dans Cowork et appuyez sur **Entrée**

#### Prompt <!-- omit in toc -->

```text
Construis une offre pour [VOTRE GAMME, par ex. les semelles ClimFeet]. Empile des tiers : une entrée de gamme pour le premier achat, un bundle premium pour un usage pro ou extrême (par ex. « Pack Pro froid extrême »), et un abonnement de remplacement des semelles usées. Promesse concrète et terre-à-terre (par ex. « tenir une garde de 12 heures dans le froid en sentant encore ses pieds »), pas une promesse gonflée. Angle « Pourquoi maintenant » : [SAISON / STOCK LIMITÉ / DATE LIMITE]. Utilise /offer-architect.

Ne continue que si tous les espaces réservés sont remplis. Sinon, rappelle-moi de te donner plus d'informations.
```

#### Résultat attendu <!-- omit in toc -->

Un package d'offre copiable : nom de l'offre, promesse en une ligne, tableau des tiers, ce qui est inclus, accroche « Pourquoi maintenant » et CTA.

> [!TIP]
> **Poussez plus loin :** avec Google Drive ou HubSpot connecté (Configuration [Étape 2](#étape-2--connectez-vos-outils-optionnel)), le skill propose d'enregistrer l'offre dans Drive ou de l'attacher à un deal HubSpot. Demandez aussi le calendrier de promotion sur 12 semaines pour étaler les messages sans saturer votre audience.

---

### Lab 6 : Décliner un contenu sur tous les canaux

**Ce que vous allez produire :** 8 à 13 pièces natives par canal à partir d'une seule source — orientées vers les canaux visuels grand public (Instagram, TikTok) plus LinkedIn et X.

> [!TIP]
> **Idée clé :** une bonne pièce est la partie la plus difficile. Le reste, c'est de la distribution. `/repurpose` prend ce que vous avez déjà — une démo de la techno « alimentée par vos pas », un témoignage client, un moment au CES — et le multiplie, conçu pour chaque canal.

#### Étapes <!-- omit in toc -->

1. Restez dans le projet Cowork d'un lab précédent (ou créez un nouveau projet)
2. Ayez une pièce finie sous la main — un témoignage client, une démo produit, une annonce de lancement ou votre page produit existante
3. Remplissez l'espace réservé dans le prompt ci-dessous et collez le texte source complet

#### Prompt <!-- omit in toc -->

```text
Je veux multiplier cette pièce sur plusieurs canaux.

[COLLEZ VOTRE CONTENU SOURCE — texte complet de votre témoignage, démo produit, page ou annonce]

Utilise /repurpose. Crée des variantes pour :
- Instagram : carrousel + script de Reel (démo « alimentée par vos pas »)
- TikTok : script court
- LinkedIn : post écrit
- X/Twitter : thread + 3 tweets autonomes

Ancre chaque pièce dans ma voix et mon ICP. Lance /antislop sur chaque pièce avant de me montrer le résultat.

Ne continue que si le contenu source est collé. Si l'espace réservé est toujours là, rappelle-moi de le remplir.
```

#### Résultat attendu <!-- omit in toc -->

8 à 13 pièces, chacune formatée pour son canal. Chacune doit se lire comme écrite pour cette plateforme — pas copiée de l'original.

> [!TIP]
> **La qualité de la source détermine la qualité du résultat.** Une source avec une démo claire, des chiffres concrets (plage de température, durée) et une vraie histoire se multiplie proprement. Une source mince produit des variantes minces. Si le résultat semble faible, renforcez d'abord la source.

---

## Préparer le lancement

Construire la page d'un produit à venir — le pont vers le lancement de WarnFeet.

### Lab 7 : Construire une landing page de pré-lancement

**Ce que vous allez produire :** deux landing pages de pré-lancement pour un produit à venir (par ex. WarnFeet), ancrées dans le contexte Solecooler et écrites dans votre voix.

> [!TIP]
> **Idée clé :** les skills sont des playbooks enregistrés — appelez-en un, Claude le suit. Ce lab brille pour un **nouveau lancement** : ClimFeet a déjà sa page, mais WarnFeet (à venir) a besoin d'une page de pré-lancement avec inscription à la liste d'attente. C'est aussi la transition vers les labs 8 et 9, qui ouvrent les canaux B2B et médical de WarnFeet.

#### Étapes <!-- omit in toc -->

1. Ouvrez un projet Cowork dédié au lancement (par ex. « Lancement WarnFeet »)
2. Remplissez `[VOTRE PRODUIT À VENIR]` dans le prompt ci-dessous, collez-le dans Cowork et appuyez sur **Entrée**

#### Prompt <!-- omit in toc -->

```text
Construis 2 landing pages de pré-lancement pour [VOTRE PRODUIT À VENIR, par ex. WarnFeet]. Ancre chaque affirmation dans le contexte d'entreprise Solecooler, l'ICP du produit (pour WarnFeet : personnes diabétiques à risque d'ulcère du pied, et les cliniciens/podologues qui les suivent), les règles de voix et de rédaction partagées, et mes Instructions globales personnelles. Chaque page cible un angle différent (par ex. patient vs clinicien/système de santé). Le CTA est l'inscription à la liste d'attente. N'invente aucune donnée clinique ni allégation médicale ; marque [PLACEHOLDER — preuve réelle nécessaire] partout où une preuve manque.

Fais-le en 3 étapes :

1. LE DESIGN D'ABORD — Utilise /frontend pour construire la mise en page et le design visuel des deux pages. Donne à chacune un schéma complètement différent. Enregistre chacune en fichier HTML dans un dossier `landing-pages/`.

2. LA COPY ENSUITE — Utilise /landing-page pour écrire la copy de chaque page. Remplace tout texte d'espace réservé par une vraie copy de pré-lancement (promesse, preuve disponible, CTA liste d'attente).

3. LE NETTOYAGE EN DERNIER — Utilise /antislop pour éditer les deux pages. Retire tout ce qui sonne comme écrit par une IA.

Montre-moi tous les résultats dans l'aperçu Cowork.

Ne continue que si tous les espaces réservés sont remplis. Sinon, rappelle-moi de te donner plus d'informations.
```

#### Résultat attendu <!-- omit in toc -->

Vous devriez voir un dossier `landing-pages/` avec 2 fichiers HTML de pré-lancement. Double-cliquez pour les ouvrir dans votre navigateur.

---

### Lab 7.1 : Habiller la landing page à la marque

**Ce que vous allez produire :** votre meilleure landing page reconstruite pour correspondre à la vraie marque Solecooler.

> [!TIP]
> **Idée clé :** Claude reproduit votre style quand vous lui donnez un fichier de référence de marque.

Vous avez un premier brouillon de landing page du [Lab 7](#lab-7--construire-une-landing-page-de-pré-lancement). Il ne ressemble juste pas encore à la marque. Cette étape tire la marque dans un fichier que Claude lit, puis reconstruit votre meilleure page à la marque.

#### Étape 1 : Tirer la marque dans un design.md <!-- omit in toc -->

1. Allez sur [stitch.withgoogle.com](https://stitch.withgoogle.com)
2. Dans la barre d'outils en bas, assurez-vous que **Web** est sélectionné (pas App)
3. Cliquez sur le bouton **+** → collez l'URL d'une page Solecooler (par ex. `https://solecooler.com/en/insoles/the-climfeet-range/`) → Entrée
4. Collez le prompt ci-dessous → Entrée
5. Clic droit sur le résultat → **Télécharger**
6. Glissez le fichier `design.md` dans le dossier de votre projet

#### Prompt <!-- omit in toc -->

```text
Analyse le site web et les images que j'ai ajoutés. Extrais l'identité visuelle complète et rends-la sous forme d'un seul fichier markdown que je peux télécharger en `design.md`. Une autre IA lira ce fichier pour reconstruire des pages dans ce style de marque exact — sois donc précis et exhaustif.

Formate-le en markdown propre. Nomme le fichier `design.md`.
```

#### Étape 2 : Reconstruire votre meilleure page à la marque <!-- omit in toc -->

Choisissez votre préférée parmi les 2 landing pages du Lab 7. Puis copiez ce prompt :

```text
Lis tous les fichiers design.md joints. Reconstruis [INDIQUE QUELLE PAGE RECONSTRUIRE] pour qu'elle corresponde exactement à la marque Solecooler — couleurs, polices, espacements, styles de boutons. Garde toute la copy. Enregistre-la en `on-brand-landing-page.html` dans le dossier `landing-pages/`.
```

#### Résultat attendu <!-- omit in toc -->

Vous devriez voir la même page, les mêmes mots, désormais habillée de la marque Solecooler. Double-cliquez `on-brand-landing-page.html` dans le dossier `landing-pages/` pour l'ouvrir dans votre navigateur.

---

## Les canaux B2B et médical

Atteindre les distributeurs, la santé au travail et le public médical — les audiences de WarnFeet et de l'usage professionnel de ClimFeet.

### Lab 8 : Toucher la distribution et les acheteurs B2B sur LinkedIn

**Ce que vous allez produire :** un post LinkedIn qui parle aux acheteurs B2B — distributeurs, responsables santé/sécurité au travail, gestionnaires de flotte — autour de l'usage professionnel de ClimFeet (pompiers, frigoristes, BTP).

> [!TIP]
> **Idée clé :** pour Solecooler, LinkedIn sert le B2B, pas le grand public. Un angle « coût des pieds froids » ou « sécurité au travail » parle aux acheteurs pro bien mieux qu'un message produit grand public. `/interesting` affûte l'angle, `/linkedin-post` le construit pas à pas, `/viral-hooks` muscle la première ligne.

#### Étapes <!-- omit in toc -->

1. Restez dans un projet Cowork (ou ouvrez-en un nouveau)
2. Procurez-vous une source : une statistique de santé au travail, une histoire de client pro, ou une mise à jour (par ex. un retour du CES)
3. Remplissez l'espace réservé dans le prompt ci-dessous et collez la source

#### Prompt <!-- omit in toc -->

```text
Transforme la source ci-dessous en post LinkedIn pour un public B2B (distributeurs, santé/sécurité au travail, gestionnaires de flotte). Angle : l'usage professionnel des semelles ClimFeet dans le froid extrême (pompiers, frigoristes, BTP) — confort, sécurité et productivité sur des postes longs, sans batterie à recharger. Guide-moi pas à pas : laisse-moi choisir le résultat d'audience, le cadre et l'accroche. Si une accroche manque de mordant, propose-m'en via /viral-hooks, et affûte l'angle avec /interesting si besoin.

[COLLEZ VOTRE SOURCE — une statistique, une histoire de client pro, ou une mise à jour]

Ancre-le dans ma voix et le contexte Solecooler. Utilise /linkedin-post.

Ne continue que si le contenu source est collé. Si l'espace réservé est toujours là, rappelle-moi de l'ajouter d'abord.
```

#### Résultat attendu <!-- omit in toc -->

Un post LinkedIn fini, à angle B2B, dans votre voix — avec une accroche qui arrête le scroll d'un acheteur professionnel et un propos clair sur le confort et la sécurité sur le terrain.

> [!TIP]
> **Vérifiez-le d'abord :** avec Slack connecté (Configuration [Étape 2](#étape-2--connectez-vos-outils-optionnel)), le skill propose de déposer le brouillon dans un canal pour un second avis avant publication.

---

### Lab 9 : Raconter l'histoire WarnFeet au public médical

**Ce que vous allez produire :** un article ou un post qui présente WarnFeet — la semelle connectée de prévention des ulcères du pied diabétique — à un public médical : podologues, diabétologues, systèmes de santé.

> [!TIP]
> **Idée clé :** WarnFeet est pré-commercial. Ici, le marketing construit l'autorité et une liste d'attente, pas des ventes. Le ton médical exige des preuves et de la prudence.
>
> **Règle stricte (depuis `company-instructions`) :** ne fabriquez jamais de chiffre clinique, de témoignage ou d'allégation médicale. Si une preuve manque, le skill doit la marquer `[PLACEHOLDER — preuve réelle nécessaire]` plutôt que de l'inventer.

#### Étapes <!-- omit in toc -->

1. Restez dans un projet Cowork (ou ouvrez-en un nouveau dédié au public médical)
2. Rassemblez les faits connus sur WarnFeet : sans batterie, alimenté par les pas, capteurs piézoélectriques, 150 zones de mesure (pression et température), prévention des ulcères du pied diabétique, prototype présenté au CES 2024, essais cliniques à venir
3. Remplissez l'espace réservé dans le prompt ci-dessous et collez ces faits

#### Prompt <!-- omit in toc -->

```text
Écris [un article X long OU un post LinkedIn] qui présente WarnFeet à un public médical (podologues, diabétologues, systèmes de santé). Mets en avant : sans batterie et alimenté par les pas, 150 zones de mesure de la pression et de la température, surveillance continue, prévention des ulcères du pied diabétique. Précise le statut pré-commercial (essais cliniques à venir, prototype vu au CES 2024) et termine par un CTA clair (liste d'attente / prise de contact). N'invente aucune donnée clinique ni allégation médicale ; marque [PLACEHOLDER — preuve réelle nécessaire] partout où une preuve manque. Affûte l'angle avec /interesting si besoin. Utilise /x-article.

[COLLEZ LES FAITS CONNUS SUR WARNFEET]

Ne continue que si le contenu source est collé. Si l'espace réservé est toujours là, rappelle-moi de l'ajouter d'abord.
```

#### Résultat attendu <!-- omit in toc -->

Un article ou un post à destination du public médical — factuel, prudent, sans allégation inventée — avec un CTA vers la liste d'attente ou une prise de contact, et des `[PLACEHOLDER]` partout où une preuve clinique réelle reste à fournir.

---

## Aller plus loin

Capturer vos propres workflows dans des skills réutilisables.

### Lab 10 : Créer votre propre skill

**Ce que vous allez produire :** votre propre fichier de skill réutilisable — un playbook que Claude suit chaque fois que vous l'appelez, construit à partir de quelque chose que vous savez déjà faire.

> [!TIP]
> **Idée clé :** chaque skill utilisé dans ces labs a été construit de l'une de deux façons. Soit Claude a lu du contenu existant et en a extrait le framework, soit Claude a interviewé quelqu'un et a construit le skill à partir de ses réponses. Si vous avez expliqué la même chose plus de trois fois — un process de vente, votre façon d'écrire un certain e-mail, comment vous évaluez une idée — c'est un skill qui ne demande qu'à naître.

#### Étapes <!-- omit in toc -->

1. Restez dans un projet Cowork d'un lab précédent (ou créez un nouveau projet)
2. Choisissez votre voie :
   - **Option A — Extraire de contenu existant.** Vous avez une transcription YouTube, une newsletter, un tweet, un article ou des notes qui capturent votre façon de faire ? Vous utiliserez `/skill-creator` et le prompt ci-dessous. Récupérez d'abord le texte source (pour une vidéo, cherchez un extracteur de transcription YouTube gratuit, collez le lien et copiez la transcription).
   - **Option B — Construire à partir de votre expertise.** Pas de contenu sous la main ? Tapez simplement `/skill-creator-interview` et appuyez sur **Entrée** : il vous pose 8 questions, une à la fois, et construit le skill à partir de vos réponses — aucun prompt à coller.
3. Pour l'option A, remplissez les espaces réservés du prompt ci-dessous, collez-le dans Cowork avec votre texte source et appuyez sur **Entrée**. Pour l'option B, répondez aux questions une à une jusqu'à ce que le workflow soit assez concret pour être exécuté.

#### Prompt <!-- omit in toc -->

```text
Utilise /skill-creator pour transformer le contenu ci-dessous en skill réutilisable. Enregistre-le sous [NOM DU SKILL]. Extrais la méthode réelle — les étapes, les arbitrages et les contrôles qualité — pas juste un résumé.

[COLLEZ VOTRE CONTENU SOURCE — transcription, tweet, article ou notes]

Ne continue que si le contenu source est collé. Si l'espace réservé est toujours là, rappelle-moi de l'ajouter d'abord.
```

#### Résultat attendu <!-- omit in toc -->

Un nouveau skill dans votre liste de skills personnels (et un fichier de skill `.md` dans le dossier de votre projet si vous l'y avez enregistré). Quand Claude a fini, cherchez le bouton **Enregistrer le skill** : le skill atterrit dans vos **Skills personnels**. Désormais, tapez `/nom-du-skill` pour l'appeler, ou décrivez simplement ce que vous voulez — quand votre demande correspond à ce que le skill annonce, Claude le déclenche automatiquement.

> [!NOTE]
> **Skills personnels vs. skills de plugin.** Un skill que vous enregistrez ainsi est *le vôtre* — disponible sur vos tâches Cowork mais à vous seul. Les skills du plugin Marketing sont partagés. Si votre nouveau skill aiderait des collègues, suivez [CONTRIBUTING.md](../../CONTRIBUTING.md) pour configurer un environnement de développement et ouvrir une pull request.

**Deux autres façons de créer des skills :**

- **Transformer un chat en skill** — après avoir guidé Claude à travers un workflow en plusieurs étapes, ouvrez le menu déroulant **⌄** à côté du titre de la conversation et choisissez **Transformer en skill**.
- **Utiliser la voix** — expliquez à l'oral votre façon de faire, puis dites à Claude « Utilise le skill creator pour transformer cette conversation en skill ».

---

## D'autres labs à venir

| Lab | Ce que vous produirez |
| --- | --- |
| Lab 11 | Audit SEO de votre page produit ClimFeet (`/seo-audit`) avec correctifs priorisés |
| Lab 12 | Newsletter de marque saisonnière (`/newsletter`) — histoires clients et conseils froid/chaud |
| Lab 13 | Décision stratégique passée au `/llm-council` (mix retail / vente directe / médical, formulation des allégations) |
| Lab 14 | Banque d'accroches Instagram/TikTok (`/viral-hooks`) pour les démos « alimentées par vos pas » |
| Lab 15 | Post social informé par vos analytics — repérer ce qui marche, puis en rédiger un nouveau |
