# FS AI Templates

The source of truth for the FunnelStreams AI template library. The template
directory (the theme-filter portal) reads `templates.json` from this repo.

## What is here

| Path | What it holds |
| --- | --- |
| `templates.json` | One record per template: name, niche, category, palette, colors, fonts and file paths |
| `thumbnails/<id>.jpg` | 800 x 500 screenshot of the top of each template, rendered at 1440 px wide |
| `templates/<id>.html` | The template as one standalone HTML page |

Files are named by template name. `Crowned by Kenya` is `crowned-by-kenya`.
A redesigned version of a template keeps the name and adds `-redesign`.

## A record in templates.json

```json
{
  "id": "renee-calloway",
  "name": "Renee Calloway",
  "niche": "Career Coaches & Consultants",
  "category": "coaching",
  "categoryName": "Coaching & Experts",
  "palette": "Ink & Apricot",
  "colors": { "background": "#FAF7F4", "primary": "#1F2F46", "accent": "#F6CDA8" },
  "style": "Light",
  "headlineType": "Serif",
  "headlineFont": "Fraunces",
  "colorFamily": "Blue",
  "hue": 215,
  "edition": "library",
  "thumbnail": "thumbnails/renee-calloway.jpg",
  "html": "templates/renee-calloway.html",
  "canvasUrl": "https://claude.ai/artifact/..."
}
```

`edition` is `original` (the first eleven coaching designs), `library` (the
generated set) or `redesign` (hand-built replacements).

`thumbnail` and `html` are paths inside this repo. `canvasUrl` opens the design
on its private canvas and only works for the canvas owner.

## Adding a template

1. Put the page in `templates/<id>.html`.
2. Put its screenshot in `thumbnails/<id>.jpg` (800 x 500).
3. Add a record to `templates.json` and raise `count`.

## Placeholders

Brand names are stand-ins. Photos are labeled shapes. Prices, credentials and
testimonials are in [BRACKETS] for the business owner to fill in.
