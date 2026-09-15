# Arunima Shankar's Portfolio

A static, framework-free portfolio site. No build step, just HTML, CSS and a
few lines of JS.

```
site/
├── index.html            # homepage
├── work/nira.html         # NiRA case study
├── assets/
│   ├── css/style.css
│   ├── js/main.js
│   ├── favicon.svg
│   └── img/               # all project imagery, organised by section
└── README.md
```

## Preview locally

Any static server works. From this folder:

```bash
ruby -run -e httpd . -p 8000
# then open http://localhost:8000
```

or, if you have Node:

```bash
npx serve .
```

## Hosting it

The easiest options: all free, all take under five minutes.

**Netlify (drag and drop)**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the whole `site` folder onto the page
3. Done: you get a live URL immediately, and can add a custom domain in Site settings

**Vercel**
```bash
npx vercel --cwd "site"
```
Follow the prompts, no config needed.

**GitHub Pages**
1. Push the contents of `site/` to a GitHub repo (as the repo root, or a `/docs` folder)
2. Repo → Settings → Pages → set the source branch/folder
3. Your site publishes at `https://<username>.github.io/<repo>`

## Adding a new project

Duplicate `work/nira.html`, swap the images and copy, and add a card for it
in the "Selected Work" section of `index.html`. Keep new images inside
`assets/img/<project-name>/` so everything stays organised.

## Notes

- Fonts load from Google Fonts (Inter) over a CDN link, no local font files to manage.
- All imagery currently in `assets/img/` was sourced from the NiRA project
  documents (presentation boards + ideation booklet) and optimised for web
  (resized + compressed) from the originals.
