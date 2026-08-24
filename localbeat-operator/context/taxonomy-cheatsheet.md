# Taxonomy cheat-sheet

The corpus is organized by a 181-code taxonomy (categories + topics). Match a prospect's language to codes case-insensitively when building a pull. Codes are passed as `taxonomyCodes` in a search.

## How to get the real, complete list

This starter is not the full 181. Pull the authoritative vocabulary once and cache it:

- `GET /taxonomy/getAll` returns all 181 codes (name + description), or use the `taxonomy()` helper in the `localbeat-api` skill's client.
- Do this on Day 1 and drop the result into this file so Claude matches buyer language to real codes, not guesses.

`[[FILL: paste the taxonomy()/getAll output here on Day 1]]`

## Common codes seen in the wild (from the API skill, not exhaustive)

`TRIVIA`, `BLUEGRASS`, `KIDS_AND_FAMILY`, `FOOD_TRUCKS`, plus categories like live music, comedy, markets, classes, festivals.

## Mapping buyer language to codes (examples)

- "family stuff" / "things to do with kids" -> `KIDS_AND_FAMILY`
- "bar trivia" / "pub quiz" -> `TRIVIA`
- "food trucks" / "street food" -> `FOOD_TRUCKS`
- "live music" -> the relevant music category/topic codes (confirm against the full list)

When a prospect names a vertical need ("we care about nightlife" or "outdoor events"), find the closest codes from the full list before pulling.
