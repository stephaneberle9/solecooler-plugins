# CLAUDE.md

## Project

Claude plugin marketplace for Solecooler (all teams).

## Language

- Commit messages in English (Conventional Commits: `feat:`, `fix:`, `docs:` etc.)
- User-facing docs (README, CONTRIBUTING, CONNECTORS, TUTORIAL) in French
- Skill content stays in English but triggers on French prompts; product/voice context (`company-context`, `company-instructions`) is Solecooler-specific
- Code comments in English where present

## Structure

- Plugins live under `plugins/<plugin-name>/`
- Each plugin has `.claude-plugin/plugin.json` and `README.md`
- Skills live under `plugins/<plugin-name>/skills/<skill-name>/SKILL.md`
- Marketplace config: `.claude-plugin/marketplace.json`

## Git

- Commits GPG-signed (`git commit -S`)
- Default branch: `main`
