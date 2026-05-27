# Feature: Call Library

**Summary**: The Call Library in HeySales Studio aggregates all scored real call records, giving reps and admins a browsable history of past calls with metadata, scores, summaries, and recordings.

**Sources**: `Call library - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## What it does

The Call Library is a paginated list of all real calls that were successfully scored through the Zoom + CRM integration. Each record shows the call's metadata, the score (as a percentage), and links to the full report and recording.

## Who uses it

- **Admins**: View all reps' call records
- **Learners / Reps**: View their own call records

## How to access

Navigate to HeySales Studio → Call Library (tab or section in Studio navigation)

## Call card UI

Each call card shows:
- Meeting date
- Call title
- Prospect email
- Rep email
- Score (displayed as a percentage, converted from 5-point scorecard)

## Time grouping

Calls are grouped by time with pills:
- Today
- Yesterday
- This Week
- Last Week
- 2 Weeks Ago
- 3 Weeks Ago
- Month + Year (for older calls)

## Call record detail

Clicking a call card opens the detail view with:
- Metadata (meeting date, title, prospect, rep)
- Summary
- Scorecard (parameter-by-parameter breakdown)
- Recording

## Score conversion

Scorecard scores are on a 1–5 scale per parameter. The Call Library displays these as a percentage.

## Empty state

When no calls have been scored, the library shows: "No calls added yet!"

## No audio

When a call was scored but has no recording (e.g. recording toggle was off at time of call), a message is shown indicating no audio is available.

## Duplicate prevention

For any given deal, the system prevents duplicate call records being pushed. One unique record per call event.

## Integration sources

Calls can come from:
- Zoom + HubSpot integration
- Zoom + MS Dynamics integration

## Things to know

- Score shown in Call Library is the percentage equivalent of the 1–5 scorecard score (source: `Call library - Sheet1 (1).csv`)
- Time grouping uses "2 weeks ago" and "3 weeks ago" labels — this differs from some AC descriptions that only mention "previous month" as the oldest grouping (logged in contradictions.md)

## Related pages

- [[test-coverage]]
- [[real-call-scoring]]
- [[custom-scorecards]]
