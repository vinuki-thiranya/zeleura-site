# ZELEURA — Art Lives Here

Static website for the ZELEURA art studio. Everything lives in `index.html` (markup, styles and scripts) with images and the intro video in `assets/`. Pages are hash routes (`#/shop`, `#/gallery`, …) so it runs on any static host, including GitHub Pages, with no server or build step.

## Run locally
Open `index.html` in a browser, or serve the folder (`npx serve .` or `python3 -m http.server`).

## Deploy on GitHub Pages
1. Create a repository (for example `zeleura-site`) and upload these files to the root of the `main` branch.
2. Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` → Save.
3. The site is live at `https://<your-username>.github.io/zeleura-site/` within a minute or two.

## Editing
- Artworks, collections, sizes and frames: the `BASE_ARTWORKS`, `COLLECTIONS`, `ORDER_SIZES` and `FRAMES` arrays near the top of the script in `index.html`. Put new artwork photos in `assets/` and point `img`/`room` at them.
- Prices: set `PRICES_ENABLED = true` and fill the `price` fields.
- Contact links: search for `wa.me` in `index.html`.
- Themes: the three `:root[data-theme=…]` blocks at the top of the stylesheet.

## What is demo-only
Cart, wishlist, orders, commission requests and the Admin dashboard (passcode `zeleura`) save to the visitor's own browser (localStorage). GitHub Pages cannot run a backend, so to receive real orders and commission enquiries connect a form/database service (e.g. Formspree, Netlify Forms, Supabase) or move to the Next.js build.
