# baseline-lab.com

Static site for **Baseline Labs LLC**, an independent product studio.
No build step — plain HTML/CSS. Hosted on GitHub Pages at https://baseline-lab.com.

## Structure (product-studio IA)

```
index.html        Studio home (domain-agnostic) + products grid
styles.css        Shared styles. Parent brand is neutral; each product overrides
                  --accent via a theme class on <body> (e.g. .theme-halo).
CNAME             Custom domain for GitHub Pages
halo/
  index.html      Halo product page (App Store + Google OAuth landing)
  privacy.html    Halo privacy policy
  terms.html      Halo terms of service
```

## Adding a new product

1. Add a `.theme-<name>` block in `styles.css` with the product's accent color.
2. Create `/<name>/index.html`, `/<name>/privacy.html`, `/<name>/terms.html`
   (copy Halo's as a starting point; set `<body class="theme-<name>">`).
3. Add a `.product-card` for it in `index.html`'s products grid.

## Canonical URLs

- Studio home / Google OAuth homepage: `https://baseline-lab.com/`
- Halo product page: `https://baseline-lab.com/halo/`
- Halo privacy (App Store + Google OAuth): `https://baseline-lab.com/halo/privacy.html`
- Halo terms: `https://baseline-lab.com/halo/terms.html`
