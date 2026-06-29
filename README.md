# Mohammed “Momo” Alsouri — personal site

A clean, static personal website. No build step, no framework, no backend —
just `index.html`, `styles.css`, and `script.js`. Built to host on GitHub Pages.

```
omgbroops/
├── index.html              # all page content
├── styles.css              # all styling (warm-minimal theme, light + dark)
├── script.js               # theme toggle, mobile menu, scroll reveals
├── .nojekyll               # tells GitHub Pages to serve files as-is
├── assets/
│   ├── favicon.svg         # the little "M" tab icon
│   └── placeholders/       # notes on swapping in real images
└── README.md               # you are here
```

## Preview locally

It’s plain static files, so any of these work:

```bash
# Option A — just open it
#   double-click index.html

# Option B — a tiny local server (nicer; smooth scrolling + correct paths)
python -m http.server 8000      # then open http://localhost:8000
# or
npx serve .
```

## Deploy to GitHub Pages

This repo is named `omgbroops`, so it publishes as a **project site** at
`https://omgbroops.github.io/omgbroops/`.

1. Commit and push to the `main` branch.
2. On GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: `main`, folder: `/ (root)`. Save.
5. Wait ~1 minute, then visit the URL shown on that Pages settings screen.

> Want the cleaner URL `https://omgbroops.github.io/` (no `/omgbroops`)?
> Rename the repo to `omgbroops.github.io`. All links here are relative, so
> nothing in the code needs to change.

## What to customize

All edits are in **`index.html`** — search for the `EDIT ME` comments. The main ones:

| What                | Where (search in `index.html`)        | Currently set to                         |
|---------------------|----------------------------------------|------------------------------------------|
| GitHub link         | `EDIT ME: your GitHub profile`         | `https://github.com/omgbroops`           |
| Email               | `mailto:`                              | `adam.zahaan@gmail.com`                  |
| Instagram (calculus)| `idislikelhopital`                     | `https://instagram.com/idislikelhopital` |
| Polyshield link     | `EDIT ME: live Polyshield link`        | `https://polyshield.vercel.app/`         |
| JSwingX repo        | `EDIT ME: GitHub repo for JSwingX`     | `https://github.com/omgbroops/JSwingX`   |
| LinkedIn / X        | commented-out block in Contact section | *(add when ready)*                       |
| Page title / meta   | top of `<head>`                        | name + short description                 |

## Adding images

Every grey dashed box is a placeholder. To replace one, find it in `index.html`
(they look like `<div class="ph" data-label="…">`) and swap it for an `<img>`.
Full instructions and a section-by-section image list are in
[`assets/placeholders/README.md`](assets/placeholders/README.md).

## Editing content

- **Projects** live in the `#work` section, one `<article>` each. Copy an
  existing block to add a new project, or delete one you don’t want.
- **Timeline** entries are `<li class="timeline__item">` blocks.
- **Notes** are placeholder cards. To turn one into a real post, create e.g.
  `notes/my-post.html` and link the card’s title to it.
- **Colors / spacing / fonts** are all CSS variables at the top of `styles.css`
  (`:root { … }`). Change `--accent` to retheme the whole site in one place.

## Notes

- **Dark mode** is automatic (follows your OS) with a manual toggle in the nav;
  the choice is remembered. Remove the `#themeToggle` button in `index.html` to
  drop it.
- **Fonts** load from Google Fonts (Fraunces + Inter). Delete the three font
  `<link>` tags in `<head>` to go fully offline — the CSS falls back to a clean
  system stack.
- Everything works without JavaScript; `script.js` only adds polish.
