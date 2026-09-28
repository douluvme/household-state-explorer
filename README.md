# Housing State Explorer

A single-page prototype of an interactive US housing dashboard, modelled on the
state view of the Anthropic Economic Index.

- **US overview**: a tile map of all 50 states plus DC, coloured by year-over-year
  median home-price growth (quartile tiers), with a ranked list.
- **State detail**: select any state to see its growth rank, growth compared with the
  US average, market and affordability indicators, and a treemap of typical monthly
  housing spending. Switch between homeowners and renters, and select a tile with a
  corner mark to drill into its parts.

All data is **mock data** generated inside `index.html` with a seeded random generator,
so it stays the same on every load.

## Run it

Open `index.html` in a browser. No build step or server is needed. D3 loads from cdnjs,
and fonts load from Google Fonts.

## Hosting on GitHub Pages

The repo is ready to be served as-is: `index.html` is at the root, and `.nojekyll`
tells Pages to skip its Jekyll build. In **Settings → Pages**, set **Source** to
*Deploy from a branch*, then pick **main** and **/ (root)**. The site appears at
`https://douluvme.github.io/household-state-explorer/`.

Deep links work with a state code in the URL fragment, for example `index.html#WA`.

## Tech stack

- **Plain HTML, CSS and JavaScript in one file**: easy to share, open and edit.
- **D3.js v7**: `d3.treemap` for the spending breakdown, scales for the rank strip
  and growth bar, and data joins to build the tile map and lists.
- **CSS grid** for the tile map, so it resizes to any screen width.
