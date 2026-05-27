# Feature: Simulation Reports

**Summary**: Simulation reports provide admins with completion rates, average scores, time spent, rankings, and per-learner call breakdowns for every simulation.

**Sources**: `Simulations Reports - Simulation Reports.csv`

**Last updated**: 2026-05-25

---

## What it does

After learners complete simulations, admins can view a rich reporting dashboard showing aggregate metrics and per-learner detailed breakdowns, including a call recording slider for individual attempts.

## Who uses it

- **Admins / Content Publishers**: View all learner reports
- **Learners**: View their own individual report after each attempt

## Metric cards (aggregate view)

| Metric Card | Calculation |
|---|---|
| Completion Rate | Completed learners / Assigned learners |
| Avg Score | Total score across all attempts (all completed learners including retakes) / Total attempts |
| Avg Time Spent | Cumulative time per learner / Number of completed learners — does NOT include retakes separately |
| Latest Score | Last attempt's score (individual report) |
| Team Avg | Sum of best scores / Number of completed learners |
| Attempts Taken | Count shown; bar graph shows last 3 attempts if >3 total |
| Ramp-up Rate | Assigned vs Enrolled; hours if <24h elapsed, days otherwise |
| Time Spent | Cumulative across all attempts |
| Ranking | Based on best score; dynamic (updates as learners complete) |

## Learner list

- Completed learners: clickable (opens detailed report)
- Not started learners: disabled (not clickable)

## Detailed report screen

Accessible by clicking a completed learner. Shows:
- Back button
- Completed learners count
- Search bar
- Learner list with score and call date on left side
- Full report on right side

### Latest Score card
- Score from last attempt
- Team avg = sum of best scores / completed learner count

### Attempts dropdown
- Lists all attempts chronologically
- Calls under 2 minutes are labelled "NA"
- Attempt selector updates all breakdown content

### Breakdown section
- Last call date
- Call duration
- Parameter-by-parameter scoring

### Call properties scored
- Conversation Quality
- Prospect Engagement
- Brand Positioning
- Understanding Buyer Needs
- Buying Intent Qualification
- Next Steps & Call Progression

## Related pages

- [[overview]]
- [[test-coverage]]
- [[simulation-call-recording]]
- [[custom-scorecards]]
