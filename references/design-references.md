# Design references

A running catalog of sites we're drawing from. Each entry records what the site
actually *is*, its extracted design tokens, and what's worth borrowing (or not)
for nicholasmileham.com.

---

## 1. Watermelon UI

- **URL**: <https://ui.watermelon.sh/> (part of the Watermelon ecosystem at <https://watermelon.sh/>)
- **What it is**: A premium/open-source React component library — dashboards, blocks,
  and application UI you copy-paste. Not a website design to imitate; a *component kit*.
- **Stack**: React + Tailwind CSS v4 + the shadcn/ui token contract, shipped as a Vite SPA
  (4 KB HTML shell, ~1 MB compiled CSS, client-rendered).

### Extracted tokens

| Token | Light | Dark |
| --- | --- | --- |
| `--background` | `#ffffff` | `#121212` / `oklch(.145 0 0)` |
| `--primary` | `#0ab1ba` (teal) | same |
| `--accent` | `#edf3fc` (blue-tinted) | `oklch(.269 0 0)` |
| `--accent-foreground` | `#0a1b39` (navy) | `oklch(.985 0 0)` |
| `--border` | `#e4e7ec` | `oklch(1 0 0 / 10%)` |
| `--radius` | `.5rem`–`.625rem`, scaled to `sm/md/lg/xl` | same |

- **Type**: Inter Variable as the single sans family; system mono for code; serif optional.
- **Neutrals**: pure grayscale — `oklch(… 0 0)`, zero chroma, no hue bias.
- **Theming**: light/dark by swapping the same token names. Clean architecture.

### Assessment

**Borrow:** the token architecture. Naming a semantic layer (`--background`,
`--foreground`, `--border`, `--card`, `--radius`) rather than literal color names is
genuinely better than what we have now, and makes theming and future components trivial.
The radius scale (`sm/md/lg/xl` derived from one base) is worth copying too.

**Don't borrow:** the surface aesthetic. Inter + pure-neutral grays + rounded cards +
hairline borders is the default SaaS/dashboard look — it's everywhere, and it reads as
generic on a personal site. Our current direction (Cormorant Garamond display, brass
accent on near-black, monospace telemetry) has a specific point of view that this would
flatten.

**Compatibility note:** using Watermelon's actual components means adopting React +
Tailwind + a build step. The site today is one self-contained HTML file with no
dependencies. That's a real architecture decision, not a drop-in.

---

## 2. _(next site — add here)_
