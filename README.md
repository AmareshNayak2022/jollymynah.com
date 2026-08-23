# Amaresh Nayak — Personal Website

A single-page static site. No build step, no dependencies — just HTML, CSS (inline in `index.html`) and two images.

## Project structure

```
amaresh-nayak-site/
├── index.html          → the entire site (markup + styles)
└── assets/
    ├── portrait.jpg     → cropped black-and-white portrait
    └── painting.jpg     → original artwork: the site's logo, favicon and hero emblem
```

## Opening in IntelliJ IDEA

1. Unzip this project to a folder on disk.
2. In IntelliJ: **File → Open...** and select the unzipped folder.
3. Choose **"Open as Project"** (IntelliJ will detect it as a static web project — no SDK or framework needed).
4. Right-click `index.html` in the Project panel → **Open in Browser** to preview, or use the built-in live preview if you have the browser plugin enabled.

## Hosting

Because everything is self-contained (no external build), you can deploy the folder as-is to any static host: GitHub Pages, Netlify, Vercel, an S3 bucket, or a plain web server. Just make sure the `assets/` folder is uploaded alongside `index.html` — the image paths are relative.

## Editing

- All content lives in `index.html` — text, layout, and styling are in one file for simplicity.
- Colors, fonts, and spacing are defined as CSS custom properties (`:root { --deep: ...; --violet: ...; --pink: ...; }`) near the top of the `<style>` block, so palette or type changes only need to happen in one place.
- To swap the portrait or painting, replace the files in `assets/` and keep the same filenames, or update the `src` paths in `index.html`.
