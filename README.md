# armactl website

Public marketing website for [armactl](https://github.com/dturovskiy/armactl).

This repository contains the static public site only. It is separate from the authenticated armactl web management panel, which lives in the main `armactl` repository under `src/armactl/web/`.

## Structure

```text
index.html              # static marketing page
assets/                 # website images and favicon source
docs/design-system/     # design handoff, tokens, UI references, and source notes
```

## Local preview

Open `index.html` directly in a browser, or serve the directory with any static file server.

```bash
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.

## Design rules

Use `docs/design-system/HANDOFF.md` as the source of truth for the marketing site visual language.

Keep these surfaces separate:

- this repository: public marketing website;
- `dturovskiy/armactl`: CLI, TUI, backend, authenticated web panel, tests, releases.

Do not copy authenticated dashboard controls, dangerous actions, user management, billing, terminal, host controls, or file-management actions into this public site as if they were public website features.

## Deployment

GitHub Pages deploys the repository root through `.github/workflows/static.yml`.
