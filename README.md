# SonIA Company Website

Astro corporate website for SonIA, an AI platform for high-volume recruiting workflows.

## Development

```sh
npm install
npm run dev
npm run build
```

When an agent starts the dev server, use the background Astro workflow documented in `AGENTS.md`.

## Project Context

- `AGENTS.md` is the authoritative instruction for coding agents.
- `docs/PROJECT_CONTEXT.md` explains the product, audience, and commercial constraints.
- `docs/DESIGN_SYSTEM.md` defines the SonIA purple/gold design direction.
- `docs/ASTRO_IMPLEMENTATION.md` captures Astro implementation rules.
- `docs/QUALITY_GATE.md` lists validation checks before considering work complete.

## Current Skeleton

- Astro pages and sections are server-rendered `.astro` components.
- Global brand tokens live in `src/styles/tokens.css` and are imported by `src/styles/global.css`.
- The home page is a Spanish corporate skeleton with placeholder contact/legal items marked as `TODO: confirmar`.
- Set `PUBLIC_SITE_URL` in production to enable canonical/sitemap configuration with the confirmed domain.
