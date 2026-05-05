# habi-app

Marketing and support site for **Habi: Cultivar Hábitos** — a Kotlin Multiplatform habit tracker for iOS and Android.

Live: https://michelbueno.github.io/habi-app/

## Structure

- `index.html` — language detector that redirects visitors to their preferred locale (`en`, `pt`, `es`).
- `en/`, `pt/`, `es/` — localized landing (`index.html`) and support (`support.html`) pages.
- `assets/` — CSS, images, and screenshots.
- `.github/workflows/deploy.yml` — GitHub Actions workflow that publishes the site to GitHub Pages on every push to `main`.

## Local preview

The site is plain HTML/CSS — no build step. Open any page directly in a browser, or serve the directory:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080/
```

## Deployment

Pushes to `main` trigger `.github/workflows/deploy.yml`, which uses the official GitHub Pages actions (`configure-pages`, `upload-pages-artifact`, `deploy-pages`).

After the first deploy, enable Pages in **Settings → Pages → Source: GitHub Actions** (one-time setup).

## Updating content

- Marketing copy lives directly in each locale's `index.html`.
- FAQ and support copy lives in each locale's `support.html`.
- Privacy policy is hosted separately at https://michelbueno.github.io/habi-privacy/ and is linked from every page.
- Screenshots live under `assets/screenshots/{en,pt,es}/`. Replace files with the same names to update.

## Brand

- Primary color: `#2D6A4F` (Nature Green)
- Accent: `#FF9E00` (Sunrise Orange)
- Logo: 🌱

## License

MIT — see [LICENSE](LICENSE).
