# Supernal releases

One JSON file per product in `releases/<slug>.json`, newest release first. Anyone can read them over HTTPS without an account.

Each record has these fields: key, slug, kind, version, releasedAt (ISO date), summary (one plain sentence), source, link, recordedAt (ISO date) and backfilled.
Records are only added, never edited. They are written by the release step of each product, not by hand.
A file with `backfilled: true` records was created from the product's existing npm publish times or production deploys.

Read the latest release of a product:

    curl -s https://raw.githubusercontent.com/supernalintelligence/releases/main/releases/repotype.json
