# High Pace

Personal home page with the bio of a software consultant and architect. The first version is deliberately generic: get it online, then add real details.

## Stack

- Astro, static output only, with plain CSS and no client-side JavaScript by default.
- No backend. Contact is a `mailto:` link and social links. If a contact form is ever needed, use a hosted form service before writing server code.
- All editable text lives in `src/content.ts`.

## Hosting

GitHub Pages at https://stompsu.github.io/high-pace/, deployed by `.github/workflows/deploy.yml` on pushes to `main`. The repository is public, so keep anything private out of it. If the site moves to a custom domain, update `site` and `base` in `astro.config.mjs`.

## Commands

- `npm run dev`: local dev server
- `npm run build`: build into `dist/`

## Agents

Defined in `.claude/agents/`:

- `content-writer`: the words on the page. Never invents facts about the owner.
- `site-builder`: layout, styling and configuration.
- `site-reviewer`: read-only checks before a deployment.
- `site-deployer`: the deployment workflow and hosting.

Usual order: `content-writer` and `site-builder`, then `site-reviewer`, then `site-deployer`.
