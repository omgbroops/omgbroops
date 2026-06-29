# Image placeholders

Drop your real images anywhere under `assets/` (this folder is just a convenient home).
The site ships with styled placeholder boxes so it looks finished before you add anything.

## How to swap a placeholder for a real image

In `index.html`, find a placeholder like this:

```html
<div class="ph ph--wide" data-label="Website / app screenshot" aria-hidden="true"></div>
```

Replace the whole `<div>` with an `<img>`:

```html
<img src="assets/carecompass-app.png" alt="CareCompass event sign-up screen" />
```

Always write a short, descriptive `alt` text (it’s read aloud by screen readers and
shown if the image fails to load).

## Suggested images to add (by section)

| Section            | Placeholder labels                                         |
|--------------------|------------------------------------------------------------|
| Hero               | Portrait / workspace photo / project collage               |
| Polyshield         | Dashboard screenshot · Approval / demo GIF                 |
| CareCompass        | Website/app screenshot · Care package photo · Outreach photo |
| JSwingX            | Example interface · UI component · Code snippet            |
| Indie Games        | Game screenshot · In-game UI · 3D asset / render           |
| Pumps & Pipes      | Team/car photo · Circuit photo · Reaction→sensor→motor diagram |
| Other Builds       | Small 16:9 thumbnail per card                              |

## Recommended formats / sizes

- Screenshots & photos: `.webp` or `.jpg`, ~1600px on the long edge.
- Wide media (`.ph--wide`): aim for a 16:9 crop.
- Social preview (`assets/og-image.png`): 1200×630, then uncomment the
  `og:image` line in `index.html`.
