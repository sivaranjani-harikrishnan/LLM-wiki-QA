# Acceptance Criteria: Course Reports

**Summary**: Defines the metrics and views available in course reports for managers and admins.

**Sources**: `raw/aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf`

**Last updated**: 2026-05-25

---

## AC-CR-01: Course overview cards

GIVEN a manager views the course reports page
WHEN they look at the course summary
THEN they see overview cards showing: Completion %, Pass %, Average Score, Total Time Spent, and Average Time Spent

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-02: Learner list — completed entries are clickable

GIVEN a manager is viewing the learner list in a course report
WHEN they look at a learner who has completed the course
THEN that learner's row is clickable and links to their detailed report

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-03: Learner list — not-started entries are disabled

GIVEN a manager is viewing the learner list in a course report
WHEN they look at a learner who has not started the course
THEN that learner's row is non-clickable (disabled), since there is no report to show

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-04: Detailed report — Latest Score vs peer best

GIVEN a manager views a learner's detailed course report
WHEN they view the scores section
THEN the learner's latest score is shown alongside the peer best score for comparison

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-05: Detailed report — Last 3 attempts

GIVEN a manager views a learner's detailed course report
WHEN they view the attempts section
THEN the last 3 attempts are shown with their scores

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-06: Detailed report — Time Spent and Time to Complete

GIVEN a manager views a learner's detailed course report
WHEN they view the time metrics
THEN both Time Spent (total active time) and Time to Complete (ramp-up rate, elapsed from first access to completion) are shown

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-07: Ranking by best score

GIVEN the learner list in a course report has a ranking column
WHEN learners are ranked
THEN ranking is based on each learner's best score (not most recent score)

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

## AC-CR-08: Assessment slider breakdown

GIVEN a course contains assessments
WHEN a manager views the detailed report for a learner
THEN an assessment slider breakdown is shown, displaying the learner's performance across individual assessment components

(source: aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[courses]]
- [[podcast-simulation-in-courses]]
- [[simulation-reports]]
