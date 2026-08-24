# REVIEW.md: the bar every outbound must pass

Run this on any email, deck, one-pager, proposal, or data sample before it ships. Sort findings into **must-fix**, **should-fix**, **okay-to-ship**. When in doubt, it does not ship.

## Must-fix (block the send)

- **Proof is real.** Every number traces to an actual data pull or to the canonical figures (85M+ events, 300K+ venues, 180+ categories, US-wide). No invented stats. No rounded-up guesses.
- **Pricing and terms.** No price, discount, SLA, data-volume guarantee, or contract language unless Ian approved it. If present and unapproved, stop and route to Ian.
- **Right prospect, right facts.** Names, company, city, vertical, and their stated blocker are correct and match the `/customers` file.
- **One ask.** The email asks for exactly one thing.
- **Data hygiene.** Any attached sample is cleaned per the `localbeat-api` skill: `Event |` prefixes stripped, coded class names removed, deduped by programId, counts verified with a facet call, coverage gaps stated honestly.

## Should-fix (fix unless there is a reason not to)

- **Brand voice.** Title-case LocalBeat in prose. Short declarative sentences. No em-dashes. Softeners cut. Ends on conviction.
- **Visual brand.** Indigo is identity, red is action used sparingly, category colors label content only, white foundation. Bricolage for headlines, Inter for body.
- **Momentum.** The message moves the deal forward, not just "checking in." It gives the champion something to forward internally.
- **Length.** As short as it can be and still land.

## Okay-to-ship (note, do not block)

- Minor phrasing preferences, optional extra proof, formatting polish.

## Always human-owned

Signing, final pricing, legal and data-license terms. These never ship from Claude, no matter how clean the draft.
