# Market-pull recipe

The repeatable way to turn a prospect's city + category into clean, branded proof. This is the operational core of the flagship play. The `market-pull` skill automates it; this is the human-readable spec.

## Inputs

- City or zip, category/categories (map to taxonomy codes), date window, and view (series vs occurrence, usually series).

## Steps

1. **Geocode.** `geocode(zip)` preferred (bare city names are ambiguous: "Brooklyn" resolves to Alabama). Take the first result's lat/lng. Sanity-check it.
2. **True count first.** `POST /program/search/facets` with location + radius + dates (+ taxonomyCodes) to get `totalElements` (exact) and topic buckets. This is the headline number. Never use the 10,000-result pagination cap as a total.
3. **Pull records.** `POST /program/search`, `size: 100`, paginate until short, **dedupe by programId** (raw pulls inflate 20 to 30% from overlap).
4. **Hygiene.** Strip `Event |` prefixes, collapse whitespace, title-case ALL-CAPS names, drop coded studio class names (parenthetical durations, code prefixes). Flag `showDate` ending `T00:00:00` as all-day/unscheduled, not midnight. Note venues with `statusCode: REVIEW` as unverified.
5. **Series vs occurrence.** For a human-facing sample, group by (cleaned name, venue `locationId`) into series with cadence ("every Tuesday"). Offer occurrence view only if they asked.
6. **Headline stat.** One honest line: "[N] events across [C] categories at [V] venues in [City], [window]."
7. **Brand it.** Apply `localbeat-brand`: white foundation, indigo identity, category colors for tags, Bricolage headline, Inter body. Keep it clean.

## Honesty rules

State coverage gaps. If a category is thin in that market, say it and show where the corpus is strong instead. Do not pad the number.

## Output

A short branded sample (table or one-slide) plus the one-line headline stat, ready to attach to an email or drop on the deck's "Events in [Region]" slide.

## Auth

Read the key from `LOCALBEAT_API_KEY`. Never hardcode it, never write it into a saved file.
