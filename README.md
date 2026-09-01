# e-vishnu-gh.github.io

Personal portfolio site — Vishnu Ellusamy, Senior DevOps / Site Reliability
Engineer. Plain HTML/CSS/JS, no build step, no framework. Deployed with
GitHub Pages.

**Live:** https://e-vishnu-gh.github.io/

## Stack

- Static HTML + hand-written CSS (custom properties, no utility framework)
- Vanilla JS (~80 lines): theme toggle, mobile nav, scroll-reveal
- Fonts: [Fraunces](https://fonts.google.com/specimen/Fraunces) (display),
  [Inter](https://fonts.google.com/specimen/Inter) (body),
  [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (labels)
  via Google Fonts
- No build tooling, no dependencies to install — deploys straight from the
  repository root

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Structure

```
index.html            single-page site
css/styles.css         design system + layout
js/script.js            theme toggle, mobile nav, scroll-reveal
assets/
  favicon.svg
  og-image.png          social share preview
  Vishnu-Ellusamy-Resume.pdf
robots.txt
sitemap.xml
.nojekyll               tells GitHub Pages to skip Jekyll processing
```

## Updating content

All copy lives directly in `index.html` — experience, selected work, and
skills are plain markup, no CMS or data file. To update the résumé PDF,
replace `assets/Vishnu-Ellusamy-Resume.pdf` with the new file, keeping the
same filename so the download links keep working.

## Deployment

Pages is configured to deploy from the `main` branch, root folder — no
GitHub Actions workflow required. Any push to `main` updates the live site
within a minute or two.
