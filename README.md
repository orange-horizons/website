# Orange Horizons Aerospace — website

Static, dependency-free single-page site. Private for now: `index.html` carries a `noindex, nofollow` meta tag.

## Run locally

```bash
cd website
python3 -m http.server 8080
# open http://localhost:8080
```

Or open `index.html` directly in a browser.

## Layout

```
website/
├── index.html          # hero, capabilities, open source, company, contact, footer
├── css/styles.css      # all styling; brand tokens at the top in :root
└── assets/
    ├── logo.png            # transparent background, navy text (header, favicon)
    ├── logo-white.png      # transparent background, white text (footer)
    ├── plane-white.png     # aircraft silhouette cropped from the logo (hero visual)
    └── logo-original.png   # the source file, untouched
```

## Brand

Sampled from the logo: navy `#0c1825`, orange `#fe5c04`.
Fonts: Michroma (display) and Inter (body) via Google Fonts, with system fallbacks.

## Placeholders to replace

- UEI and CAGE code: hidden until SAM.gov registration is active. Add them back to the Company stats in `index.html` (there's a comment marking the spot), and consider changing the heading back to "Registered and ready to work with government and industry."


If you change `styles.css`, bump the `?v=` number on the stylesheet link in `index.html` so browsers pick up the new file.
