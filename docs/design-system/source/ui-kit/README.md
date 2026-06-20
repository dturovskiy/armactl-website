# UI Kit — armactl marketing website

Faithful recreation of https://dturovskiy.github.io/armactl/ (source: `reference/website-index.html`, original at `website/index.html` in the repo).

- `index.html` — entry + site-level layout CSS (header, hero, sections, footer).
- `website-app.jsx` — SiteHeader, Hero, Overview, Features, Philosophy, SiteFooter.

Interactive: theme toggle (moon icon → `.theme-light` scope), anchor nav, all hover states. Composes DS primitives: `Button`, `SectionHeader`, `FeatureCard`, `ValueItem`, `TerminalWindow`.

Omitted from the recreation (present on the live site): EN/UA/FR language switcher, mobile hamburger menu.
