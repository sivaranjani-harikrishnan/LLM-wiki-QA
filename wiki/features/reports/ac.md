# Acceptance Criteria: Reports

**Summary**: Defines the data shown in role-based analytics dashboards, learning-level reports, and the analytics revamp calculations for time spent, learner insights, and course insights.

**Sources**: `raw/4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf`, `raw/98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf`, `raw/2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf`

**Last updated**: 2026-05-25

---

## Role-based Dashboard ACs

## AC-RPT-01: Role-specific default view on entry

GIVEN a user navigates to the Reports tab
WHEN the page loads
THEN the user lands on a role-specific default view: Admin → Org overview, Sales Manager → My Team view, Course Creator → My Content view, Learner → My Progress, Leadership → Business Outcomes

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-02: Global filters always visible

GIVEN a user is on any Reports page
WHEN viewing the top bar
THEN the following filters are always visible and functional: date range picker (Last 7 days / 30 days / Quarter / Custom), org selector (Org → Region → Team → Rep), segment switch (Myself / My Team / Other Teams / Entire Org), learning type filter (Course / Simulation / Podcast / All), skill filter, status filter (Not Started / In Progress / Completed), compare toggle (User vs Team / Team vs Org)

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-03: Admin dashboard layout

GIVEN a user with Admin role views the Reports dashboard
WHEN the dashboard renders
THEN they see: KPI strip (Active learners, Active creators, number of Learnings Completed, number of Learnings Published), charts (Funnel: Assign→Start→Complete→Pass; Completion rate by team; Ramp-up time; Time spent learning stacked by type), and team-level tables with drilldown to learners

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-04: Sales Manager dashboard layout

GIVEN a user with Sales Manager role views the Reports dashboard
WHEN the dashboard renders
THEN they see: KPI strip (Team completion %, Avg score, Skills gained, number of Active learners), charts (Team completion vs target, Skill breadth and depth, Simulation performance tiles for Discovery/Cold/Follow-up, Call aspect radar, Improvement trends in call aspects), and a leaderboard table of top learners and learners needing attention

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-05: Course Creator dashboard layout

GIVEN a user with Course Creator role views the Reports dashboard
WHEN the dashboard renders
THEN they see: KPI strip (Completion %, Avg ramp-up, Avg score, Attempts-to-pass), charts (course completion funnel, Attempts vs Pass % scatter, Drop-off chart at lesson level, Peer comparison of their portfolio vs org averages), and tables for course-level performance and top vs at-risk courses

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-06: Learner dashboard layout

GIVEN a user with Learner role views the Reports dashboard
WHEN the dashboard renders
THEN they see: KPI strip (My completion %, Avg score, Skills earned, Call scores), charts (learning points trend, skills breadth and depth radar, call simulation improvement from first to latest), and tables of current learnings in progress or not started and peer comparison

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-07: Leadership dashboard layout

GIVEN a user with Leadership role views the Reports dashboard
WHEN the dashboard renders
THEN they see: KPI strip (Org LRS, SLA % achieved, Skills coverage, New skills), charts (Region/team readiness leaderboard, Learning points vs Opportunity closure correlation tile, Org-wide completion % and Avg scores trend), and tables of top regions/teams with readiness vs deal outcomes

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-08: Drilldown from chart elements

GIVEN a user clicks any chart element (bar, line, or tile)
WHEN the click is registered
THEN a drilldown view opens following the role's hierarchy: Admin (Team → Learners), Sales Manager (Learner → Attempts/Sim runs), Course Creator (Course → Lesson/Question stats), Learner (Asset → Feedback/Recommendations); breadcrumbs (Org → Team → User) are shown to navigate back

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-09: AI insight cards (Seek layer)

GIVEN a user views any role-specific Reports dashboard
WHEN the page loads
THEN 3-5 auto-generated natural-language insight cards with a CTA are shown at the top of the dashboard

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## AC-RPT-10: Export options

GIVEN a user is on any Reports page
WHEN they want to export data
THEN export options are available: CSV, PDF, and scheduled email delivery

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

---

## Analytics Revamp ACs

## AC-RPT-11: Time spent on courses calculation

GIVEN a user views the time spent metric for a course
WHEN the value is calculated
THEN it equals the sum of duration of content sessions across all lessons within the course

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-12: Time spent card scope

GIVEN a user views the Time Spent card with a date range filter applied
WHEN the value is calculated
THEN it equals the sum of duration of learning records whose started date falls within the selected time duration

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-13: Learner Insights table sorting and scope

GIVEN a user views the Learner Insights table with a date range filter
WHEN the table renders
THEN all learners are listed sorted in descending order of learnings started in the given duration; learners with 0 learnings started are included and appear at the end; all data points in the table are scoped to that time range only

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-14: Pass % calculation

GIVEN a user views the Pass % metric for a time period
WHEN the value is calculated
THEN it equals: out of the learnings completed in that duration, the percentage that were passed; podcasts and simulations are counted as passed by default

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-15: Avg score % calculation

GIVEN a user views the Avg Score % metric for a time period
WHEN the value is calculated
THEN it equals the average score across learnings completed in that duration

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-16: Course Insights table

GIVEN a user views the Course Insights table with a date range filter
WHEN the table renders
THEN all published courses are listed sorted in descending order of learnings started for that course in the given duration; each course shows: pass % (out of completed records in the duration), number of unique learners assigned/enrolled in the duration, number of learning completions in the duration, average score across completed records in the duration

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-17: Course Insights Learnings Tab

GIVEN a user views the Learnings Tab within Course Insights
WHEN the tab renders
THEN all published courses the user is enrolled in are listed; each shows: enrolled date, status (not started / in progress / completed — if completed even once it is marked as completed), completed date, number of attempts, time spent, average score

(source: 98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf)

## AC-RPT-18: Learning Points definition

GIVEN a learner completes a learning
WHEN learning points are calculated
THEN every completion adds the learner's score out of 100 as points (e.g. completing two learnings with 76% and 82% scores gives 158 learning points total)

(source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

---

## Learning-level Analytics ACs

## AC-RPT-19: Overall analytics per learning type

GIVEN an admin/manager/creator views the overall analytics panel for a specific learning
WHEN the panel renders
THEN it shows: Number of learners + Completion rate (all types); additionally for Call Simulation: Average score across latest takes by completed learners, Average call aspect scores; additionally for Course (with assessment): Average score by assessment, Average days to complete (ramp-up rate); additionally for Course (without assessment): Average days to complete; additionally for Podcast: Average time spent, Highest drop-off point/topic, Topic with most/least time spent, timeline graph of engagement

(source: 2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf)

## AC-RPT-20: Learner summary view — data per status and learning type

GIVEN an admin/manager views the learner list for a specific learning
WHEN a learner row is displayed
THEN the two data values shown depend on learning type and learner status:
- Completed simulation: latest call's overall score (with date), latest call date, number of takes, link to breakdown view
- In-progress simulation: N/A (no data shown)
- Completed course (with assessment): latest completion score %, number of attempts to pass/complete, latest completion date
- In-progress course (with assessment): latest attempt's progress %, started on date, last active date (and failure attempts count if previously failed)
- Not started (any type): assigned/enrolled date and nudge icon to send reminder email
- Completed podcast: total time spent listening, number of sessions, completed date, completion %
- In-progress podcast: percentage of completion, time spent listening so far, last engagement date

(source: 2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf)

## AC-RPT-21: Learner breakdown view — all attempts sorted by recency

GIVEN a user clicks to expand a learner's breakdown view within a specific learning
WHEN the breakdown renders
THEN all takes/attempts/sessions are listed sorted by most recent first; for Call Simulation each take shows: call logged date, duration of call, overall score, link to view call recording, link to view report; for Course (with assessment) each attempt shows: overall score %, assessment-wise breakdown %, links to assessment reports, started on date, completed date

(source: 2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf)

## AC-RPT-22: Inactive learners — nudge across all learning types

GIVEN a learner has not started a learning (across all types: simulation, podcast, course with or without assessment)
WHEN their row is displayed in the learner list
THEN the assigned/enrolled date is shown and a nudge icon is available to send a reminder email with a single click

(source: 2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf)

---

## Related pages
- [[overview]]
- [[course-reports]]
- [[simulation-reports]]
- [[podcast-reports]]
- [[learner-reports]]
- [[learners-list-analytics]]
- [[courses]]
- [[simulations]]
- [[podcasts]]
