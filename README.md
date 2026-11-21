# Oday Seyam — Personal Website

Single-page personal site (Arabic / English / French, dark & light themes).
No build step, no framework: plain HTML, CSS and JavaScript in `index.html`.

## Structure
- `index.html` — all markup, styles (`<style>`) and scripts (`<script>`).
- `img/` — portrait (`oday.webp`, `oday-cut.webp` transparent cutout) and project screenshots
  (`h*-*.webp` AlHaibaPhone, `y*-*.webp` Yafa Cosmetics). Customer data in screenshots is already blurred.
- `Oday-Seyam-CV.pdf` — ATS-friendly CV (English, 2 pages), linked from the nav and hero "Download CV" buttons.
- `og.jpg` — 1200×630 link-preview image (WhatsApp, LinkedIn, X).

## Where to edit
- **All texts (3 languages):** the `T` object in the script (`ar` / `en` / `fr` for every key).
- **Jobs:** `JOBS` · **Certificates:** `CERTS` · **Skills:** `SKILLS`, `LANGS`, `SOFT` · **Services:** `SERVICES`.
- **App Store link (Yafa):** `const APP_STORE_URL = ""` near the top of the script.
- **Colors / fonts:** CSS variables in `:root` (light) and `:root[data-theme="dark"]`.
  Fonts: Alexandria (headings) + IBM Plex Sans Arabic (body) from Google Fonts.
- **Site address:** the `og:url`, `og:image` and `twitter:image` meta tags use `https://odayseyam.github.io`.
  Change them if the site is hosted on another domain (e.g. Cloudflare Pages or a custom domain).

## Behaviour
- **Language:** opens in `#ar`, `#en` or `#fr` if the link has that hash; otherwise the visitor's last choice;
  otherwise the browser language (Arabic → ar, French → fr, anything else → en).
  Share language-specific links like `https://odayseyam.github.io/#en`.
- **Lite mode:** on slow connections (2G/3G, Data Saver), low-memory or low-core devices, or reduced-motion,
  the `lite` class is added to `<html>`: background animation is drawn once, orbit/sweep effects and blur are off.

## Run locally
Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000

## Deploy
- **GitHub Pages:** push this folder to a public repo named `odayseyam.github.io` → https://odayseyam.github.io
- **Cloudflare Pages (recommended for a future login portal):** connect the GitHub repo; no build command; output directory `/`.
