# Scapegoat LLC

Marketing site for **Scapegoat LLC**, a landscaping company in Greenville, South Carolina,
run by Jason Brown (25 years on residential and commercial properties across the Southeast).

Live: https://jimmyardis.github.io/scapegoat-llc/

## Structure

A single self-contained `index.html`: inlined CSS, SVG favicon, and all art as data URIs.
No external assets, no build step, no dependencies.

The file is authored outside this repo and delivered as a finished artifact, so treat the
repo copy as the artifact rather than the source — re-deliveries overwrite it wholesale
instead of being hand-edited.

## Deploy

GitHub Pages, `main` branch, `/ (root)`. Pushing to `main` publishes.
