# htmweb.com

Personal blog for Hassan Mamdani. Built with [Astro](https://astro.build), deployed to [Cloudflare Pages](https://pages.cloudflare.com).

## Local development

```bash
npm install
npm run dev
```

Opens at `http://localhost:4321`.

## Writing a new post

Create a Markdown file in `src/content/blog/`:

```md
---
title: "Your post title"
description: "One sentence for the listing and meta tags."
pubDate: 2026-04-01
---

Your post content here.
```

The filename becomes the URL slug — `my-post.md` → `/blog/my-post`.

Set `draft: true` to keep a post out of the built site while you work on it.

## Build

```bash
npm run build
```

Outputs to `dist/`. No server required — pure static HTML.

## Deploy to Cloudflare Pages

1. Push this repo to GitHub (or GitLab).
2. In the Cloudflare dashboard, go to **Workers & Pages → Create → Pages → Connect to Git**.
3. Select the repository.
4. Set build settings:
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
   - **Node.js version:** 22 (set in Environment Variables: `NODE_VERSION = 22`)
5. Click **Save and Deploy**.

After the first deploy, connect your custom domain (`htmweb.com`) under **Custom domains** in the Pages project settings.

Subsequent pushes to `main` deploy automatically.
