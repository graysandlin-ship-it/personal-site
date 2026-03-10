# Grayson Sandlin Personal Site

Personal website built with Astro and prepared for static deployment on Cloudflare Pages.

## Local development

Run from the project root:

```sh
npm install
npm run dev
```

Local build:

```sh
ASTRO_TELEMETRY_DISABLED=1 npm run build
```

## Content to update

- Site-wide identity, links, and domain live in `src/consts.ts`
- Homepage copy lives in `src/pages/index.astro`
- About page copy lives in `src/pages/about.astro`
- Future blog posts go in `src/content/blog/`

## Cloudflare Pages

This project is set up for Cloudflare Pages static hosting.

- Framework: `Astro`
- Build command: `npm run build`
- Build output directory: `dist`
- Root directory: `personal-site` if you connect the whole `Personal` repo

If you create the Pages project with the name `grayson-sandlin`, Cloudflare will usually assign `https://grayson-sandlin.pages.dev`. If that exact subdomain is unavailable, update `SITE_URL` in `src/consts.ts` after deployment to match the real assigned URL.

The repo also includes `wrangler.jsonc` with `pages_build_output_dir` set to `./dist`.
