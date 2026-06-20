# armactl — Website handoff

Design reference + source for the **marketing website** (the public site, `website/index.html` in the `armactl` repo — live at https://dturovskiy.github.io/armactl/). This package is for improving the **website only**. It is a separate surface from the web dashboard and uses a deliberately different visual language.

## What's inside

| Path | What it is |
|---|---|
| `reference/website-index.html` | **The real, live production site** — fully self-contained (open it in a browser for the exact target look; needs internet for Google Fonts + Font Awesome). This is the source of truth for markup, copy and values, and what you are improving. |
| `source/ui-kit/index.html` | A clean-room recreation's site-level layout CSS (header, hero, sections, footer) + mount point — handy as a structured reference. |
| `source/ui-kit/website-app.jsx` | The recreation's React components: `SiteHeader`, `Hero`, `Overview`, `Features`, `Philosophy`, `SiteFooter`. (Composes the DS web primitives via a bundle, so it won't render on its own — read it for structure.) |
| `source/components/web/` | Reusable site primitives: `Button`, `SectionHeader`, `FeatureCard`, `ValueItem`, `TerminalWindow` (each with `.d.ts` types + `.prompt.md` notes). |
| `source/tokens/` | The website design tokens — `colors.css` (near-black neutrals + neon green/blue/orange triad, + `.theme-light` scope), `typography.css` (Nico Moji + Roboto Mono), `spacing.css`, `effects.css` (sharp corners, glows, motion), `base.css`. |
| `source/fonts/fonts.css` | Google Fonts import (Nico Moji, Roboto Mono). |
| `reference/website-index.html` | Verbatim copy of the real live-site source — the source of truth for exact values/copy. |
| `assets/` | `logo.png` (gradient AC roundel), `social_perview.png`, and the two full-bleed image-break JPGs. |

## Brand rules (do NOT break)

- **Terminal-native aesthetic:** monospace everywhere (`Roboto Mono`), `Nico Moji` only for headings/wordmark. Sharp corners — `border-radius: 0` on every box (dots & the logo roundel excepted).
- **Color roles:** green `#00FF94` = act/success, blue `#00B2FF` = navigate/inform, orange `#F6AD55` = warn. Don't swap. Dark is the brand; `.theme-light` exists but dark is default. Never more than two background colors per view.
- **Type:** body is Roboto Mono weight 300; emphasis 600 (not bold sans). Interactive labels are UPPERCASE + 1px tracking.
- **Motion:** one speed `0.3s ease`. Card lift `translateY(-5px)` + blue border + 2px accent top bar on hover; nav-link animated underline; block-cursor blink is the only infinite loop.
- **Icons:** Font Awesome 6.4.0 only. No hand-drawn SVG icons. **No emoji, ever.**
- **Copy:** plain, technical, operator-to-operator — write like a man page, not a landing page. Product name always lowercase `armactl` (wordmark renders ARMActl). Trilingual EN / UA / FR, EN default.
- **Do NOT** bring the web dashboard's light/forest-green/rounded/sans look into the website. They are separate surfaces.

## Known gaps on the recreation (present on the live site, not yet rebuilt)

- EN / UA / FR language switcher.
- Mobile hamburger menu / responsive nav.

These are good candidates for improvement.

## ⚠️ File suffixes

Source files under `source/` carry an extra **`.txt`** suffix (`Button.jsx.txt`, `index.html.txt`, `Button.d.ts.txt`, …) so this archive isn't picked up by build tooling. **Strip the trailing `.txt`** when you use them (`Button.jsx.txt` → `Button.jsx`). The production reference `reference/website-index.html` keeps its real extension and opens directly.

## How to use this package

Open **`reference/website-index.html`** in a browser — that is the actual site you're improving (self-contained; pulls Google Fonts + Font Awesome from CDN). Use the `source/` recreation and `source/tokens/` for structured component/token references, and follow the brand rules below. Work against the repo's real `website/index.html`; this package is the design reference, not a build target.
