# High Pace

Personal home page with the bio of a software consultant and architect.

Keep personal details off the page and out of the repository: no name, location, photo, personal email, university, employer names, client names, other people's names, recommendations or credential IDs. Publish professional details only, and describe clients by sector as the owner's LinkedIn profile does.

## Stack

- Astro, static output only, with plain CSS and no client-side JavaScript by default.
- No backend. Contact is a `mailto:` link and social links. If a contact form is ever needed, use a hosted form service before writing server code.
- All editable text lives in `src/content.ts`.

## Hosting

GitHub Pages at https://highpace.dev, deployed by `.github/workflows/deploy.yml` on pushes to `main`. The custom domain is set in the repository's Pages settings, so no `CNAME` file is needed. DNS is managed at Porkbun. The repository is public, so keep anything private out of it.

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
