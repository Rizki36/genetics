# AGENTS.md

## Build & dev

```bash
npm run dev      # starts Astro dev server
npm run build    # production build to dist/
npm run preview  # preview production build locally
```

## Stack

- **Astro v6** — static site, no SSR. All `.astro` files in `src/pages/`, `src/components/`, `src/layouts/`.
- **Tailwind CSS v4** — loaded via `@tailwindcss/vite` (not via an Astro integration). Custom theme tokens (`coal`, `ember`, `ash`, `fog`, `slatex`, `soft`) and utility classes are defined in `src/styles/global.css`.
- **TypeScript** — `astro/tsconfigs/strict`, but the project currently contains no `.ts` files.

## Conventions

- The site is a single-page Indonesian landing page for "Genetics Run Club" (https://genetics-club.vercel.app).
- Use the `.display-font` CSS class for headings — it applies the Teko font with italic, uppercase, tight tracking.
- Google Fonts (Inter + Teko) are loaded in `src/layouts/Layout.astro` — do not change the font setup without updating Layout.
- Global CSS custom utilities (`.soft-card`, `.grid-fade`, `.hero-overlay`, `.motion-blur`, `.bg-noise`, etc.) are in `global.css` and used across components.
- The site uses Indonesian (`lang="id"` in Layout.astro). All user-facing text should be in Indonesian.
- No CI/CD, linting, testing, or formatting config exists. Keep it simple.
