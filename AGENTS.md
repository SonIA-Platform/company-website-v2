# AGENTS.md - Web Corporativa SonIA

This is the authoritative instruction for coding agents working in this repository.

## Development

When starting the dev server, use background mode:

```sh
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

## Mission

Build and maintain SonIA's corporate website: an AI platform for high-volume recruiting processes, from receiving or publishing a job offer to ranking, contacting, and advancing candidates.

The site must clearly communicate:

1. SonIA reduces manual CV review work.
2. SonIA prioritizes the best-fit candidates and explains the ranking.
3. SonIA helps recruiting teams move from detection to contact and follow-up.

Reference brand promise: **de centenares de candidatos a una shortlist accionable en minutos**. Do not turn this into a contractual guarantee or invent exact figures.

## Product Context

Conceptual flow:

`Oferta de trabajo -> carga/importacion de CVs -> analisis semantico -> ranking justificado -> shortlist -> contacto -> recogida de datos -> seguimiento`

Known internal modules:

- Subida de Ofertas de Trabajo
- Subida de CVs
- Ranking de Candidatos
- Contacto / outreach
- Informe de uso
- Usuarios
- Prompts
- OCR

The public website may explain these modules, but it must not copy the internal app interface literally or expose admin functions without a commercial reason.

## Audience And Goals

Primary audience:

- HR leaders
- recruiters and recruiting consultancies
- companies with massive or repetitive hiring processes
- decision makers who need to understand outcome, process, trust, and return

Website goals:

1. Make the problem and solution understandable in seconds.
2. Build trust, not a sense of AI magic.
3. Show the product tangibly.
4. Drive a clear action: request information, contact, or request a demo.

## Stack And Working Rules

This project is an **Astro** website. Preserve the existing architecture and inspect `package.json`, `astro.config.*`, `src/`, `public/`, and available scripts before changing code.

- Prefer `.astro` components and server-rendered HTML.
- Add client JavaScript only when an interaction requires it.
- Do not introduce React, Vue, Tailwind, or a component library just because a prototype uses it.
- If the repo already uses a library, integrate with it without duplicating systems.
- Keep strict TypeScript when the project uses it.
- Reuse components and tokens; avoid repeated ad hoc CSS.
- Do not rewrite unrelated files.
- Do not break `ClientRouter`, transitions, routes, or metadata if they exist.
- Do not add dependencies unless they are justified and necessary.

## Design System Truth Sources

Order of precedence:

1. Current owner request and current repository code.
2. `design-reference/colors_and_type.css` and real SVG assets.
3. `docs/DESIGN_SYSTEM.md` and the Design System README.
4. Real product screenshots provided by the owner.
5. UI kit and previews as pattern inspiration.
6. Generated manifests or metadata.

Ignore old or inconsistent names such as “Indigo”, “Hanken Grotesk”, or “Schibsted Grotesk”. The current brand uses **SonIA Purple** and **Montserrat**.

## Required Visual Brand

- Name: `SonIA` in the wordmark; `SonIA` is acceptable in running text.
- Do not write `Sonia`, `SONIA`, or `Son-IA`.
- Primary: `#695E9C`.
- Accent: `#FBC33C`, used moderately.
- Main background: light off-white; surfaces white.
- Text: ink scale, not pure black by default.
- Typography: Montserrat for display, body, and UI when font assets are available.
- JetBrains Mono only for data, scores, identifiers, or tabular numbers.
- Icons: Lucide-style outline, consistent stroke, 16/20/24 px.
- No emojis as product iconography or formal UI.
- No decorative gradients, glow, neon, excessive glassmorphism, or generic AI template effects.

## Copy Rules

Primary site language: **Spanish**, unless a task states otherwise.

Tone:

- calm expert
- direct
- close, using “tu”
- outcome first, mechanism second
- no hype or empty jargon

Preferred narrative structure:

`Problema -> Solucion -> Como funciona -> Evidencia/beneficio -> CTA`

Avoid invented clients, testimonials, exact savings, ROI, pricing, contract volumes, certifications, precision guarantees, security claims, and unconfirmed integrations. Mark missing commercial data with `TODO: confirmar`.

## Accessibility, Performance, SEO

- Use semantic HTML and correct landmarks.
- Use a single main `h1` per page and coherent heading order.
- Keep keyboard focus visible.
- Use real labels in forms.
- Respect `prefers-reduced-motion`.
- Avoid accidental horizontal scroll.
- Minimize hydrated JavaScript.
- Define page title, description, canonical when applicable, and `lang="es"`.
- Do not add schema.org data with invented fields.

## Quality Gate

Before considering a task complete:

1. Inspect the repo and conventions.
2. Read this file and related docs.
3. Implement the smallest correct change.
4. Run available build, type-check, lint, and test scripts.
5. Review relevant responsive breakpoints when possible.
6. Check basic accessibility and console errors when possible.
7. Report changed files, relevant decisions, and real limitations.

Do not claim a check passed if it was not run.

## Documentation

Full Astro documentation: https://docs.astro.build

Consult these guides before related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)
