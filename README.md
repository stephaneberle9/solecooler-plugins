# Plugins Solecooler

Marketplace de plugins Claude pour Solecooler. Les plugins sont avant tout conçus pour [Claude Cowork](https://claude.com/product/cowork), l'application de bureau agentique d'Anthropic, mais fonctionnent aussi dans [Claude Code](https://claude.com/product/claude-code).

Cette marketplace regroupe l'ensemble des plugins Solecooler, toutes équipes confondues. Ajoutez la marketplace une fois dans Cowork et installez les plugins directement depuis là. Lorsqu'une nouvelle version est publiée, Cowork vous le signale et vous pouvez mettre à jour en un clic.

## Installation

### Ajouter la marketplace

À faire une fois :

1. Ouvrez Claude Desktop et allez dans l'onglet **Cowork**
2. Cliquez sur **Personnaliser** dans la barre latérale gauche
3. Sous **Plugins personnels**, cliquez sur **+** → **Créer un plugin** → **Ajouter une marketplace**
4. Collez : `https://github.com/solecooler/solecooler-plugins.git`
5. Cliquez sur **Synchroniser** — suivez les instructions à l'écran pour autoriser l'accès à GitHub

### Installer un plugin

1. Cliquez sur **+** → **Parcourir les plugins**
2. Cliquez sur l'onglet **Personnel**
3. Sélectionnez la marketplace **solecooler-plugins**
4. Cliquez sur **Marketing** puis sur **Installer**

### Connectez vos outils (optionnel)

Les skills peuvent à la fois récupérer du contexte depuis des outils externes et y renvoyer des résultats — lire des contacts HubSpot pour personnaliser une séquence, récupérer un brief depuis Google Drive, ou livrer un résultat sous forme de brouillons Gmail, d'événements d'agenda et de messages Slack. Gmail, Google Drive, Google Calendar, HubSpot et Slack sont tous préconfigurés. Chaque connecteur doit être installé et authentifié séparément :

1. Cliquez sur **Personnaliser** dans la barre latérale gauche
2. Sous **Plugins personnels**, sélectionnez **Marketing** → **Connecteurs**
3. Pour chaque connecteur souhaité, cliquez sur **Installer** s'il ne l'est pas déjà
4. Après l'installation, cliquez sur **Connecter** et suivez les étapes d'authentification

> [!NOTE]
> Certains connecteurs peuvent déjà être présents — apportés par un autre plugin ou configurés à l'échelle de l'organisation par votre administrateur Claude AI. Si un connecteur n'affiche aucun bouton, c'est qu'il est déjà connecté ; il vous suffit peut-être de le connecter, sans l'installer.

## Mises à jour

Allez dans **Personnaliser** → **Plugins personnels** → cliquez sur le plugin dans la barre latérale.

- **Si le bouton Mettre à jour est actif** — cliquez sur **Mettre à jour**. Cela récupère les nouvelles versions officielles.
- **Si le bouton Mettre à jour est grisé** — le numéro de version n'a pas changé, mais les skills ont peut-être tout de même été mis à jour. Cliquez sur **Désinstaller**, puis réinstallez en suivant les étapes ci-dessus pour récupérer le contenu le plus récent.

## Plugins disponibles

| Plugin | Description | Documentation |
| --- | --- | --- |
| `marketing` | Le contexte business et les règles de voix de Solecooler, combinés à plus de 20 skills marketing pour la création de contenu, la recherche, la stratégie et l'édition. | [README](plugins/marketing/README.md) |

## Contribuer

Voir [CONTRIBUTING.md](CONTRIBUTING.md) pour la configuration de développement et les instructions d'ajout ou de mise à jour des plugins.

## Licence

Propriétaire. Tous droits réservés. Voir [LICENSE](LICENSE) pour les détails.
