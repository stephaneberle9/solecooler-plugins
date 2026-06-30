# Connecteurs

## Comment fonctionnent les références aux outils

Les fichiers du plugin utilisent `~~catégorie` comme espace réservé pour l'outil que l'utilisateur connecte dans cette catégorie. Par exemple, `~~crm` peut désigner HubSpot, Salesforce ou tout autre CRM doté d'un serveur MCP.

Les plugins sont **agnostiques aux outils** — ils décrivent des workflows en termes de catégories (CRM, chat, etc.) plutôt que de produits spécifiques. Le `.mcp.json` préconfigure des serveurs MCP précis, mais n'importe quel serveur MCP de cette catégorie fonctionne.

## Connecteurs de ce plugin

| Catégorie | Espace réservé | Serveurs inclus | Autres options |
|----------|-------------|-----------------|---------------|
| Messagerie | `~~email` | `gmail` ([MCP HTTP officiel Google](https://gmailmcp.googleapis.com/mcp/v1)) | Microsoft 365 |
| Agenda | `~~calendar` | `google-calendar` ([MCP HTTP officiel Google](https://calendarmcp.googleapis.com/mcp/v1)) | Microsoft 365 (Outlook Calendar) |
| Stockage cloud | `~~cloud-storage` | `google-drive` ([MCP HTTP officiel Google](https://drivemcp.googleapis.com/mcp/v1)) | Microsoft 365 (OneDrive), Notion, Confluence |
| CRM | `~~crm` | `hubspot` ([MCP HTTP officiel HubSpot](https://mcp.hubspot.com/anthropic)) | Salesforce, Pipedrive |
| Chat | `~~chat` | `slack` ([MCP HTTP officiel Slack](https://mcp.slack.com/mcp)) | Microsoft Teams |
| Recherche | `~~search` | Outil `WebSearch` intégré (aucune configuration requise) | Brave Search, Exa, Perplexity (MCP HTTP quand disponibles) |

## Comment connecter

Les connecteurs nécessitent deux étapes distinctes dans Cowork : **Installer** et **Connecter** (authentifier). Aucune ne se fait automatiquement.

1. Cliquez sur **Personnaliser** dans la barre latérale gauche
2. Sous **Plugins personnels**, sélectionnez **Marketing** → **Connecteurs**
3. Pour chaque connecteur, vérifiez son état et agissez :
   - Bouton **Installer** → cliquez pour installer (ajoute le connecteur à votre environnement Cowork)
   - Bouton **Connecter** → cliquez pour authentifier (relie votre compte via OAuth ou clé API)
   - Aucun bouton → déjà connecté, rien à faire
4. Répétez pour chaque connecteur que vous voulez utiliser (Gmail, Google Drive, Google Calendar, HubSpot, Slack)

> [!NOTE]
> Certains connecteurs peuvent déjà être présents — apportés par un autre plugin ou configurés à l'échelle de l'organisation par votre administrateur Claude AI. Si un connecteur n'affiche aucun bouton, c'est qu'il est déjà connecté ; il vous suffit peut-être de le connecter, sans l'installer.
>
> **Dégradation gracieuse :** les skills fonctionnent avec ou sans connecteurs. Quand un connecteur n'est pas connecté, le skill se termine normalement et l'offre de connecteur est simplement ignorée. Connectez-le plus tard et il devient disponible la fois suivante.
