# nicholasmileham.com

Personal website for Nicholas Mileham — aerospace, energy, film.

A single self-contained `index.html`: no build step, no framework, no dependencies beyond Google Fonts.

## Design

- **Concept** — "flight instrument, after dark": deep blue-black ground, machined hairlines, monospace telemetry, brass gauge accent.
- **Type** — Cormorant Garamond (display), Instrument Sans (body), IBM Plex Mono (telemetry).
- **Details** — canvas wireframe-terrain hero with mouse parallax, masked headline reveal, custom cursor, spotlight cards, live Wichita clock, scroll telemetry, film grain. All motion respects `prefers-reduced-motion`.

## Publishing

To serve this with GitHub Pages: repo **Settings → Pages → Deploy from a branch**, pick the branch and `/ (root)`. For a custom domain, add it under the same settings and point DNS at GitHub Pages.
