# Contribuer <!-- omit in toc -->

Merci de votre intérêt pour contribuer à `solecooler-plugins` ! Ce document fournit les directives pour mettre en place un environnement de développement, apporter des modifications et les tester en local avant de pousser sur GitHub.

- [Configuration de développement vs. installation normale](#configuration-de-développement-vs-installation-normale)
- [Prérequis](#prérequis)
- [Cloner le dépôt](#cloner-le-dépôt)
- [Enregistrer la marketplace en local](#enregistrer-la-marketplace-en-local)
- [Installer le plugin](#installer-le-plugin)
- [Tester les skills](#tester-les-skills)
- [Contribuer des modifications](#contribuer-des-modifications)
- [Incrémenter la version du plugin](#incrémenter-la-version-du-plugin)
- [Ajouter un nouveau plugin](#ajouter-un-nouveau-plugin)
- [Revenir à l'installation normale](#revenir-à-linstallation-normale)

## Configuration de développement vs. installation normale

L'installation normale (décrite dans le [README](README.md)) récupère la marketplace directement depuis GitHub. Claude Code clone le dépôt dans un répertoire de cache interne (`~/.claude/plugins/marketplaces/`) et ne met à jour les plugins que lorsque la `version` dans `plugin.json` change.

> [!WARNING]
> Avec l'installation normale, les modifications locales n'ont aucun effet tant
> qu'elles ne sont pas poussées et que la version n'est pas incrémentée.

La configuration de développement crée un clone local dédié du dépôt et configure Claude Code pour lire la marketplace directement depuis ce clone, au lieu de son cache interne. Chaque modification des skills, des fichiers de configuration ou des prompts prend effet immédiatement — sans commit, push ni incrément de version.

## Prérequis

- [Git](https://git-scm.com/)
- [VS Code](https://code.visualstudio.com/) avec l'[extension Claude Code pour VS Code](https://marketplace.visualstudio.com/items?itemName=anthropic.claude-code)
- ou bien [Claude Desktop](https://claude.ai/download) (inclut Claude Code en tant que CLI)

## Cloner le dépôt

Choisissez un dossier de votre choix pour le clone — par ex. `W:\GitHub`. Ouvrez un terminal et exécutez :

```bash
cd W:\GitHub
git clone git@github.com:solecooler/solecooler-plugins.git
cd solecooler-plugins
```

> [!TIP]
> La commande ci-dessus utilise SSH, l'option recommandée par défaut — elle évite les demandes répétées d'identifiants une fois votre clé SSH configurée ([guide SSH GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)). Si vous préférez HTTPS, clonez plutôt avec `git clone https://github.com/solecooler/solecooler-plugins.git`.

## Enregistrer la marketplace en local

L'étape suivante se passe dans Claude Code — que ce soit l'extension VS Code, le CLI Claude Code ou l'onglet Code de Claude Desktop.

Si la marketplace est déjà installée depuis GitHub, retirez-la d'abord :

> [!WARNING]
> Retirer la marketplace désinstalle aussi tous les plugins installés depuis celle-ci.

```
/plugin marketplace remove solecooler-plugins
```

Enregistrez ensuite votre clone local comme source de la marketplace — ajustez le chemin si vous avez cloné ailleurs :

```
/plugin marketplace add W:\GitHub\solecooler-plugins
```

## Installer le plugin

```
/plugin install marketing@solecooler-plugins
```

## Tester les skills

Les skills s'appellent dans Claude Code via `/nom-du-skill`, par ex. `/personal-interview`.

Comme Claude Code lit la marketplace directement depuis votre clone local, les modifications des skills et de la configuration prennent effet immédiatement. Après avoir édité un skill, il suffit de réinvoquer la commande slash — aucun redémarrage ni réinstallation nécessaire.

> [!TIP]
> Après avoir édité un skill, il suffit de réinvoquer la commande slash — aucun
> redémarrage ni réinstallation nécessaire.

## Contribuer des modifications

**Avec accès en écriture à ce dépôt :**

1. Créez une branche de fonctionnalité (par ex. `feat/ma-modification`) directement dans le dépôt
2. Faites des commits sur cette branche
3. Ouvrez une Pull Request vers `main`
4. Faites relire, approuver et fusionner la PR

**Sans accès en écriture :**

Forkez le dépôt et suivez la même procédure que ci-dessus.

## Incrémenter la version du plugin

Les modifications quotidiennes des skills n'ont pas besoin d'incrément de version — poussez librement. Un incrément de version n'est nécessaire que lorsque vous voulez **publier une release** que Cowork présente aux utilisateurs comme une mise à jour disponible.

Pour que Cowork présente une nouvelle version aux utilisateurs comme une mise à jour disponible, incrémentez aussi la version dans votre PR :

1. Incrémentez la version dans [`plugins/marketing/.claude-plugin/plugin.json`](plugins/marketing/.claude-plugin/plugin.json)
2. Validez la modification dans la même branche que vos autres changements
3. Une fois la PR fusionnée dans `main`, Cowork détecte automatiquement la nouvelle version

Une fois poussée, les utilisateurs ouvrent **Personnaliser** → **Plugins personnels** dans Cowork, sélectionnent le plugin et cliquent sur **Mettre à jour** pour récupérer la nouvelle version.

## Ajouter un nouveau plugin

Chaque plugin est un ensemble indépendant de skills et de contexte. Une fois validé et poussé, il apparaît dans la marketplace et les utilisateurs peuvent l'installer directement depuis Cowork.

1. Créez un nouveau répertoire sous `plugins/` avec `.claude-plugin/plugin.json` et `README.md`
2. Ajoutez une entrée dans [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json)
3. Validez et poussez
4. Les utilisateurs cliquent sur **+** → **Parcourir les plugins**, ouvrent l'onglet **Personnel**, sélectionnent la marketplace **solecooler-plugins** et cliquent sur **Installer** pour le plugin.

## Revenir à l'installation normale

Pour revenir à une installation depuis GitHub, retirez la marketplace locale et remplacez-la par la source GitHub :

```
/plugin marketplace remove solecooler-plugins
/plugin marketplace add https://github.com/solecooler/solecooler-plugins.git
/plugin install marketing@solecooler-plugins
```

> [!NOTE]
> Sur GitHub, `/plugin marketplace add solecooler/solecooler-plugins` (la forme
> abrégée `owner/repo`) est aussi acceptée. GitLab exige l'URL HTTPS de clone complète.
