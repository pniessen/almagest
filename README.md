# ALMAGEST — Medicare Advantage star-rating forecast console

A self-contained, static console for exploring Medicare Advantage Star Ratings —
history, forecasts for the next publication, and each contract's position relative
to the 4.0 quality-bonus line.

**Live:** https://pniessen.github.io/almagest/

Built entirely from public CMS Star Ratings data tables. The page is a single
`index.html` (no framework, no build step) reading one generated `data.js` bundle.

## Views

1. **Board** — every contract: current overall rating, predicted next publication
   + P(≥4.0) at 1- and 2-year horizons, at-risk/upside flags.
2. **Contract** — rating trajectory, domain stars, and each measure's position
   inside its published cut-point band.
3. **Accuracy** — the roll-up replication gate and the walk-forward backtest vs
   a carry-forward baseline.
4. **Industry** — rating distribution by year, upgrade/downgrade counts, carrier
   trajectories vs the 4.0 line.

Forecasts are model output, not CMS publications. Generated from a private
modeling pipeline; `data.js` is refreshed when the forecast re-runs.
