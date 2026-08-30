# Bay Area Relocation Planner

Interactive chart comparing 68 Peninsula neighborhoods against commute to
Waymo HQ, walkability, budget, and family/fitness criteria. Single static
page (`index.html`), no build step, deployed to GitHub Pages.

## Access

The page is gated behind an access code (client-side only — this is a
soft gate to keep casual visitors out, not real security; don't put
anything more sensitive than what's already here behind it).

## Deploying

Pushing to `main` triggers `.github/workflows/pages.yml`, which publishes
`index.html` via GitHub Pages. One-time setup: in this repo's
**Settings → Pages**, set **Source** to **GitHub Actions** (only needs
doing once — the workflow handles every deploy after that).

## Editing the data

All neighborhood scores, weights, and criteria live in the `CRITERIA` and
`PLACES` arrays near the top of the `<script type="text/babel-source">`
block in `index.html`. Edit the numbers there and push — no rebuild
needed.
