# Feature: Podcast Reports

**Summary**: Podcast reporting provides admins with completion rates, total listen time, and average listen time metrics for each podcast.

**Sources**: `Podcast Reports - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Podcast reports give admins visibility into how learners engage with assigned podcasts: who has completed it, how much time has been spent listening, and the average engagement per learner.

## Who uses it

- **Admins / Content Publishers**: View all learner engagement metrics

## Metric cards

### Completion Rate
- Formula: Completed / Assigned learners
- Replaying a completed podcast does NOT increment the completed count (completion recorded once)

### Total Listen Time
- Formula: Cumulative listen time across all learners, including in-progress and completed
- Replaying does NOT change the total listen time
- In-progress time is included

### Avg Listen Time
- Formula: Total listen time / (learners who started + learners who completed)
- Does NOT include learners who have not started
- Replaying does NOT change the average
- In-progress learners ARE included in the denominator

## Key behaviours

- Replay does not change any metric (completion, total time, or avg time)
- In-progress time counts toward total and avg listen time
- Not-started learners are excluded from avg listen time denominator

## Pass rate

For podcasts, pass rate is counted as "passed by default" (all completions are considered passes). (source: Analytics Revamp ACs)

## Related pages

- [[overview]]
- [[test-coverage]]
- [[podcasts]]
- [[learners-list-analytics]]
