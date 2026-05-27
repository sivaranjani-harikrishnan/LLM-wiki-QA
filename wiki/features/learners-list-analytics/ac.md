# Acceptance Criteria: Learners List Analytics

**Summary**: Defines what additional progress and performance data is shown per learner in the Manage Courses learner list, varying by learning type and learner status.

**Sources**: `raw/6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf`

**Last updated**: 2026-05-25

---

## AC-LLA-01: Additional data in learner list

GIVEN an admin or course creator views the learner list for a learning in Manage Courses
WHEN additional progress/performance data is displayed
THEN the data shown varies based on learning type (simulation / course / podcast) and learner status (completed / in progress / not started); the UI layout is uniform across types

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

---

## Podcast — Learner Status Data

## AC-LLA-02: Podcast — completed learner data

GIVEN a learner has completed a podcast
WHEN their row is shown in the learner list
THEN a flag icon is shown, their total time spent listening to the podcast is shown, and the last engagement date is shown ("last engaged on 'date'")

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-03: Podcast — in-progress learner data

GIVEN a learner is in progress on a podcast
WHEN their row is shown in the learner list
THEN a progress bar is shown based on percentage completion, and the last engagement date is shown

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-04: Podcast — not-started learner data

GIVEN a learner has not started a podcast
WHEN their row is shown in the learner list
THEN their assigned/enrolled date is shown; on hover, an email icon appears to allow sending a nudge email (nudge is not in current build scope)

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

---

## Call Simulation — Learner Status Data

## AC-LLA-05: Simulation — completed learner data

GIVEN a learner has completed a call simulation
WHEN their row is shown in the learner list
THEN a flag icon is shown, their latest attempt's score % is shown, and the latest call logged date is shown ("last call logged on 'date'")

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-06: Simulation — in-progress learner data

GIVEN a learner is in progress on a call simulation
WHEN their row is shown in the learner list
THEN no additional data is shown (N/A for in-progress simulation learners)

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-07: Simulation — not-started learner data

GIVEN a learner has not started a call simulation
WHEN their row is shown in the learner list
THEN their assigned/enrolled date is shown; on hover, a nudge email option appears (not in current build scope)

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

---

## Course with Assessment — Learner Status Data

## AC-LLA-08: Course (with assessment) — completed learner pass/fail indicator

GIVEN a course has a pass percentage set
WHEN a learner has completed the course
THEN a flag icon (pass) or cross icon (fail) is shown; score % is shown in green if passed, red if failed

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-09: Course (with assessment) — completed learner data

GIVEN a learner has completed a course with assessment
WHEN their row is shown
THEN their latest attempt's score % and the last attempt completed date ("completed on 'date'") are shown

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-10: Course (with assessment) — in-progress learner data

GIVEN a learner is in progress on a course with assessment
WHEN their row is shown
THEN if an attempt is in progress: a progress bar by completion % and the latest attempt's started date are shown; if a previous attempt failed and no new attempt started: a cross icon, latest failed attempt date, and latest attempt copy are shown

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-11: Course (with assessment) — not-started learner data

GIVEN a learner has not started a course with assessment
WHEN their row is shown
THEN their assigned/enrolled date is shown; on hover, a nudge email option appears (not in current build scope)

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

---

## Course without Assessment — Learner Status Data

## AC-LLA-12: Course (without assessment) — completed learner data

GIVEN a learner has completed a course without assessment
WHEN their row is shown
THEN a flag icon and the completed date ("Completed on 'date'") are shown

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-13: Course (without assessment) — in-progress learner data

GIVEN a learner is in progress on a course without assessment
WHEN their row is shown
THEN a progress bar (elements completed / total elements) and the latest attempt's started date are shown

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

## AC-LLA-14: Course (without assessment) — not-started learner data

GIVEN a learner has not started a course without assessment
WHEN their row is shown
THEN their assigned/enrolled date is shown; on hover, a nudge email option appears (not in current build scope)

(source: 6d24bedd-6d3b-47bc-9309-a73fdad5c0ec_Learners_list_Analytics.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[courses]]
- [[course-reports]]
- [[simulation-reports]]
