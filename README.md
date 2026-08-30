# Bay Area Relocation Planner

A tool for figuring out where to move based on the criteria that actually
matter to you. It shows an interactive map comparing 68 Peninsula
neighborhoods — commute time, walkability, rent, and family/fitness
amenities — and lets you tune how much each criterion counts, filter by
budget and commute, and pin a handful of neighborhoods side by side to
compare directly.

Single static page (`index.html`), no build step, deployed to GitHub Pages.

## Using it

- **Chips** at the top toggle a criterion on/off; double-tap a chip to
  score on that one criterion alone.
- **Tune weights** opens a form with a slider per criterion, so you can
  set exactly how much each one matters (not just on/off) — the map and
  ranked list recompute live as you drag. **Reset to defaults** restores
  the original weighting.
- **Rent ceiling / drive-time sliders** filter out neighborhoods that
  don't fit your budget or commute tolerance.
- Click any neighborhood on the map or in the ranked list to see its full
  breakdown; click **Add to compare** to pin up to 5 side by side in a
  table at the bottom.

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
