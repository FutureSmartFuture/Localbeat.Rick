# Product and API

What we license and how a buyer uses it. Keep this factual. Full query mechanics live in the `localbeat-api` skill.

## What LocalBeat sells (Product line)

Access to a national, forward-looking corpus of local events (called "programs"), the venues that host them, and a 181-code taxonomy. Delivered via a REST API at `https://localbeat.com/api`, authenticated with a Bearer key scoped at creation.

## What is in a record

Each program includes: `programId` (the dedupe key), `name`, `showDate` / `showEndDate` (local time), `duration`, `description` (~75% filled), `ticketUrl` (~7% filled, absence is a decent proxy for free/unticketed), `calendarUrl`, `taxonomy` (code objects, ~20% of events arrive untagged), `acts`, and `stage.location` (venue: name, address, city, state, zip, coordinates, timezone, `typeCode` like BREWERY or PUBLIC_LIBRARY, Google Places id).

## What a buyer can do with it

- **Search by place and time:** location (lat/lng + radius, or national) plus a date window.
- **Filter by taxonomy:** 181 codes across categories and topics.
- **Count truthfully:** facet endpoint returns exact totals and topic buckets.
- **Pull at scale:** paginate at 100/page, dedupe by programId.

## Coverage honesty (say this to prospects)

- ~75% of events have descriptions; ~20% arrive untagged; ~7% have ticket URLs.
- Most of the corpus is recurring: grouping by (cleaned name, venue) yields series, and in tested markets 65 to 90% of events belong to a series meeting 3+ days per month. We can deliver a **series view** (one row per recurring thing, with cadence) or an **occurrence view** (every date). Humans usually want series.
- We do not oversell coverage. When a prospect's market or category is thin, we say so. Honesty is a closing tool, not a liability.

## Tiers and packaging

See `products/api-tiers-and-packages.md`. Specifics are `[[FILL]]` until confirmed with Ian.

## What a buyer needs from us to start

A scoped API key, the base URL, and (usually) a sample pull for their market so they can see the data before they commit. The sample is the wedge (see the plays in the plan).
