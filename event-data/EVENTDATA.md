# Event-Data — data operations

## What this area is
Pulling from the LocalBeat corpus and turning it into clean, branded proof:
market pulls, saved datasets, coverage checks. Distinct from Sales, which uses
these pulls in outbound — this module is about the data itself.

## Sources of truth
- **How to query:** the `localbeat-api` skill (structured filters, facet counts
  for true totals, dedupe by programId, hygiene).
- **The proof recipe:** `../localbeat-operator/sales/market-pull-recipe.md`.

## Key files
- `pulls/` — saved, cleaned datasets, one folder per market or prospect. [[empty until the first pull is filed]]
- `coverage-notes.md` — known coverage gaps by region and category, stated honestly in outbound. [[FILL as gaps are found]]

## Prerequisites
- `LOCALBEAT_API_KEY` available to the session. [[set as a scheduled-task secret for the always-on layer]]

## The one rule
Every number traces to a real pull. Canonical figures only: 85M+ events,
300K+ venues, 180+ categories, US-wide.
