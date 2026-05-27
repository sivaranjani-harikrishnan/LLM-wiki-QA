# Acceptance Criteria: Simulation Reports

**Summary**: Defines the analytics overview, learner detailed report, ranking, and attempt filtering for simulation reports.

**Sources**: `raw/60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf`, `raw/4790856c-45aa-4425-8a3a-54da656889c7_Simulation_-_Analytics.pdf`

**Last updated**: 2026-05-25

---

## Analytics Overview ACs

## AC-SR-01: Three overview cards

GIVEN a manager or coach views simulation analytics
WHEN the overview is shown
THEN three title cards are displayed: Completion %, Average Score, and Avg. Time Spent

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-02: Completion % card logic

GIVEN the Completion % card is displayed
WHEN the value is calculated
THEN it shows "X completed of Y assigned/enrolled" where X = unique learners who completed at least once, Y = unique learners assigned or enrolled

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-03: Average Score card logic

GIVEN the Average Score card is displayed
WHEN the value is calculated
THEN it shows the arithmetic mean of all completed attempts by all learners, rounded to the nearest whole number; subtext shows the number of completed attempts used in the calculation; when no completions exist, shows "N/A" with subtext "no learners have taken the learning yet"

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-04: Time Spent card logic

GIVEN the Time Spent card is displayed
WHEN the value is calculated
THEN it shows the average time spent by completed learners across all their attempts

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-05: Learner list — completed users are clickable

GIVEN the learner list in simulation analytics is displayed
WHEN a learner has completed the simulation
THEN their row is clickable and opens their detailed report

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-06: Learner list — not-started users are disabled

GIVEN the learner list in simulation analytics is displayed
WHEN a learner has not started the simulation
THEN their row is non-clickable and visually disabled

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

---

## Learner Detailed Report ACs

## AC-SR-07: Three top-level metrics

GIVEN a manager views a learner's detailed simulation report
WHEN the report is shown
THEN three top-level metrics are displayed: Latest Score, Attempts Taken (last 3 scores shown), and Time Spent

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-08: Latest Score subtext — team comparison

GIVEN the Latest Score is displayed in the detailed report
WHEN there are more than 5 learners
THEN subtext shows "Average best score across the team: Y"; if the learner's latest score is a new personal best, subtext also shows "New best score"

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-09: Latest Score subtext — fewer than 5 learners

GIVEN the Latest Score is displayed in the detailed report
WHEN there are fewer than 5 learners
THEN the team average best score subtext is NOT shown

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-10: Attempts Taken — single attempt edge case

GIVEN the Attempts Taken metric is displayed
WHEN the learner has only 1 attempt
THEN the score % UI for attempts is not shown

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-11: Time Spent — cumulative across attempts

GIVEN the Time Spent metric is displayed
WHEN the value is calculated
THEN it shows the cumulative time the learner spent on this simulation across all their attempts

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-12: Time to Complete (Ramp-up Rate)

GIVEN a learner has completed a simulation
WHEN the detailed report is displayed
THEN Time to Complete (ramp-up rate) is shown: number of days from enrollment/assignment to first completion; shown in hours if < 24 hours, days rounded to nearest day if > 24 hours; assignment/enrollment date is shown below this card

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-13: Latest attempt metadata

GIVEN the detailed report is displayed
WHEN the latest attempt section is shown
THEN it includes: call logged on date and call duration

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-14: Learner sidebar — sorted by last call logged date

GIVEN multiple learners are shown in the sidebar
WHEN the list is displayed
THEN learners are sorted by their last call logged date; the currently selected learner is highlighted and auto-scrolled to

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-15: Assessment report per attempt

GIVEN a manager views a learner's detailed report
WHEN the assessment section is shown
THEN the full assessment report for the selected attempt is listed, varying by call type (discovery call, cold call, etc.)

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-16: Attempt filter for multiple attempts

GIVEN a learner has completed more than one attempt
WHEN a manager views their detailed report
THEN a dropdown allows filtering by attempt; all completed attempts are listed; if an attempt has insufficient time logged for a report, the UI shows "report not available" for that attempt

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

## AC-SR-17: Ranking display

GIVEN a manager views a learner's detailed simulation report
WHEN the page is shown
THEN the learner's rank (top right corner) and the best score that earned that rank are displayed; ranking is based on each learner's best score across all their attempts

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

---

## Simulation Analytics within Courses ACs

## AC-SRA-01: Course-context simulation updates simulation manage cards

GIVEN a course containing a simulation is assigned to a learner
WHEN the learner is added to the simulation's learner list
THEN the simulation manage analytics cards are updated to reflect course-context completions

(source: 4790856c-45aa-4425-8a3a-54da656889c7_Simulation_-_Analytics.pdf)

## AC-SRA-02: Only last attempt at course-end counts

GIVEN a learner completes a course with a simulation
WHEN the simulation's data is used for course scoring
THEN only the last simulation attempt at the time the course ended is considered

(source: 4790856c-45aa-4425-8a3a-54da656889c7_Simulation_-_Analytics.pdf)

## AC-SRA-03: Simulation score contributes to course score

GIVEN a course contains a simulation
WHEN the course is scored
THEN the simulation score is included alongside assessment scores; if the course contains only a simulation, the simulation score becomes the course score

(source: 4790856c-45aa-4425-8a3a-54da656889c7_Simulation_-_Analytics.pdf)

---

## Out of Scope

- Aspect score visualisations (charts) are not in scope
- Call recording playback button is not in scope
- Search within the learner list is not in scope

(source: 60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[simulations]]
- [[course-reports]]
- [[podcast-simulation-in-courses]]
