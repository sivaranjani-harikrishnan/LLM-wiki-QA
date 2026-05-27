# Feature: Course Reports

**Summary**: Course reports provide admins with aggregate completion, pass rate, score, and time metrics plus per-learner breakdowns including Q&A performance and attempt history.

**Sources**: `Course Reports - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## What it does

Course reports give admins a full view of how learners are progressing through a course: who completed, what they scored, and how long it took them.

## Who uses it

- **Admins / Content Publishers**: View all learner reports across the course
- **Learners**: View their own individual report

## Metric cards (aggregate view)

| Metric Card | Calculation |
|---|---|
| Completion Rate | Completed learners / Assigned learners |
| Pass % | Passed learners / Completed learners (only completed learners in denominator); retakes can change pass status; threshold changes only apply to new completions; ALL completed (including failed) count |
| Avg Score | Total score across all attempts (including retakes) / Total attempts |
| Avg Time Spent | Cumulative time per learner / Learner count; retakes count cumulatively per learner then divided |
| Total Time Spent | Cumulative across ALL completed learners across all attempts |

## Learner list

- Completed learners: clickable → opens detailed report
- Not-started learners: disabled (not clickable)

## Detailed report screen

Accessible by clicking a completed learner. Shows:
- Latest Score card: last attempt's score + Team avg (sum of best scores / learners)
- Ranking: based on best score; dynamic
- Ramp-up rate
- Time spent: cumulative
- Breakdown: lessons + assessments listed with completion status
- Q&A slider: shows each question with correct/incorrect marking
- Attempts dropdown: last 3 displayed if >3 attempts

### Sections-based courses
When a course uses Sections, the breakdown shows the section structure with lessons and assessments nested within each section.

## Key behaviours

- Pass % applies only to completions (retakes can flip failed → passed or vice versa)
- All completed (even those who failed) are included in avg score
- Avg time spent retakes: each retake's time added cumulatively per learner before dividing
- Ranking is dynamic (recalculates as more learners complete)
- Team avg = sum of best scores / completed learner count

## Related pages

- [[test-coverage]]
- [[courses]]
- [[learners-list-analytics]]
