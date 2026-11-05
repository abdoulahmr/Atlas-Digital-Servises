# Atlas Digital Services — website

Static site (no build step), English / French / Arabic (RTL).

## Deploy on Vercel
1. Push this folder to GitHub (or run `npx vercel` inside it).
2. Import the repo in Vercel. Framework preset: **Other**. No build command. Output directory: `public` (already set in `vercel.json`).

## Before going live
- Replace `contact@example.com` with your real email (search all files in `public/`).
- Replace `YOUR-DOMAIN.vercel.app` in `public/sitemap.xml` and `public/robots.txt`.
- The footer "Privacy policy" and "Social media" links point to the contact section; add real pages/URLs.

## Structure
- `public/index.html` — landing page
- `public/atlas-*.html` — six product pages (own title and description for SEO)
- `public/invoice-maker.html` — free invoice generator at `/invoice-maker` (`invoice.js`, `invoice.css`; PDF export via self-hosted `vendor/html2pdf.bundle.min.js`). Runs fully in the browser; data in localStorage only.
- `public/styles.css`, `public/i18n.js` — shared styles and FR/AR translation + RTL switching
- Translations live in the `D` dictionary at the top of `i18n.js`, keyed by the English text.

Preview locally: `npm run dev`
