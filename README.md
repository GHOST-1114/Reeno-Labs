# Reeno Labs

Reeno Labs is a static Astro website for a digital studio. The frontend has no backend, database, server API, or runtime environment variables; the production output is generated as static files in `dist/`.

## Local development

Requirements: Node.js 18.17 or newer and npm.

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Validate and build

```bash
npm run check
npm run build
```

`npm run build` creates a clean static production site in `dist/`. To inspect that production build locally:

```bash
npm run preview
```

Then open [http://localhost:3000](http://localhost:3000).

## Cloudflare Pages

Use these project settings:

- **Build command:** `npm run build`
- **Build output directory:** `dist`
- **Root directory:** `/`
- **Environment variables:** none required

The `public/_redirects` file is copied into `dist/` during the build and provides the Cloudflare Pages fallback route.

## Project structure

- `src/` — Astro components, page composition, data, browser interactions, and styles
- `public/` — local images, icons, PDF assets, social preview, and Cloudflare redirects
- `dist/` — generated production output; ignored by Git
- `package.json` / `package-lock.json` — npm scripts and locked dependencies
