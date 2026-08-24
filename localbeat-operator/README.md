# LocalBeat 24/7 Operator Workspace

This is LocalBeat's business brain for Claude, built for the **API-licensing sales motion** and aimed at one job: **re-opening and closing deals that stall.**

It follows the "AI employee" model. Claude reads this workspace before it works, so it operates the sales motion from context instead of guessing.

## How to use it

1. Point Claude (Cowork or Claude Code) at this folder.
2. Tell it to read `LOCALBEAT.md` first. That file routes it to everything else.
3. Give it a small, clear ticket (see the prompt pack in the plan doc).
4. It drafts. You review against `REVIEW.md`. Ian owns pricing and contracts.

## Layout

```
LOCALBEAT.md      how Claude works for LocalBeat (read this first)
ROADMAP.md        what matters right now (updated weekly)
REVIEW.md         the bar every outbound must pass before it ships
/context          the business brain: product, API, taxonomy, ICP, positioning, pricing, proof
/customers        one file per deal: stage, blocker, notes, language + the objection library
/products         what we sell: API tiers, data packages, sample deliverables
/sales            the asset library: email sequences, recipes, demo script, deck + one-pager templates
/routines         the recurring prompts that run the 24/7 layer
/data             scratch space for generated sample pulls before they are cleaned and filed
```

## Status of this build

Everything structural and every reusable process is built. Anything that needs live LocalBeat data is marked `[[FILL: ...]]` and is safe to search for. Fill those, connect the CRM and the API key, and the system runs.

**Fill-me-first list:** `context/pricing.md`, `context/product-and-api.md` (tier specifics), and the real deals in `/customers`.
