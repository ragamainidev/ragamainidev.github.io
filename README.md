# Raghav Maini

Source for [raghavmaini.com](https://raghavmaini.com/): personal writing on applied AI, agent design, and software engineering.

This is a static site. HTML, CSS, fonts, and diagrams are served directly by GitHub Pages. There is no framework, build step, external font service, or account requirement for readers.

## Edit and preview

- Home and biography: `index.html`
- Essays: `writing/<article-slug>/index.html`
- Design: `assets/style.css`
- Diagrams: `assets/essays/`
- Search metadata: each page's head and JSON-LD, plus `sitemap.xml` and `robots.txt`

Run from the repository root:

```sh
python3 -m http.server 4178 --bind 127.0.0.1
```

Open http://127.0.0.1:4178/ . Push changes to `main` to publish. GitHub Pages is configured to deploy the repository root. `.nojekyll` preserves the static files without Jekyll processing.

## Domain and search

The canonical domain is `https://raghavmaini.com`. `CNAME` records that domain for GitHub Pages. Porkbun manages domain registration and DNS. Preserve the Google Search Console and GitHub domain-verification TXT records when changing DNS.

When adding an article, use its canonical URL in metadata and `sitemap.xml`, link it from the homepage, and keep descriptive alt text on diagrams. Content pages allow indexing; the 404 page deliberately does not. Search discovery does not guarantee indexing or ranking.

The site can move to any static host by copying these files and updating DNS. No hosted site-builder export is needed.

## Rights

Writing and site content copyright Raghav Maini. All rights reserved. Bundled fonts retain their respective OFL licenses in `assets/fonts/`.
