# Routines

The 24/7 layer. Each file here is a prompt spec for a scheduled task. They **draft**, they do not send, and they never quote price or commit terms.

## How to activate

Create these as scheduled tasks (the `create_trigger` / scheduled-task tools), not local cron, so they survive and actually run. Times are America/Denver.

## Prerequisites before they add value

- `LOCALBEAT_API_KEY` set, so market pulls work.
- Real deals loaded in `/customers`.
- CRM connected (ideal), so "days since touch" and stage come from live data instead of only the folder.

Until those exist, a routine will run but produce thin output. Load the data first, then activate.

## The routines

- `morning-pipeline-brief.md` : weekdays 7:00 a.m.
- `pre-call-prep.md` : evening before any booked prospect call.
- `weekly-win-loss.md` : Friday afternoon.
