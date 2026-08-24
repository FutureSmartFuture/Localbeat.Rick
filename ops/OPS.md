# Ops — the connective tissue and live view

## What this area is
The day-to-day glue and the data behind the "live view of everything": calendar,
inbox, weekly digests, and the metrics the command centre shows.

## Sources of truth
- **Calendar and email:** [[FILL: which provider — connect the connector]]
- **File storage:** Google Drive (connected).

## Key files
- `weekly-digest/` — the Friday digest outputs. [[empty]]
- `metrics.md` — the numbers the command centre reads (pipeline, pulls sent, content shipped). [[FILL]]
- `command-centre/` — the front-door page and its data feed. [[built in a later step]]

## The one rule
This area is a window, not a source of truth. It summarizes the other three
areas; it does not duplicate them.
