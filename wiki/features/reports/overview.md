# Feature: Reports

**Summary**: A role-aware analytics dashboard that surfaces different metrics and views for Admins, Sales Managers, Course Creators, Learners, and Leadership, enabling each role to track the data that matters to their goals.

**Sources**: `raw/4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf`, `raw/98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf`, `raw/2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf`

**Last updated**: 2026-05-25

---

## What it does
Reports provides a centralised analytics view for the HeySales platform, tailored to the viewer's role. Each role lands on a different default view and sees different KPIs, charts, and tables. Data can be filtered by time period, team/org segment, learning type, skill, and status, and compared against benchmarks.

## Who uses it
- **Admins**: Ensure the organisation is engaging with learning, content is being created, and adoption targets are met.
- **Sales Managers**: Track team learning progress and skill development; identify areas for improvement and targeted coaching.
- **Course Creators**: Monitor how their content is used, completed, and its impact on learner performance.
- **Learners**: Track personal progress, identify strengths and gaps, and benchmark against peers.
- **Leadership**: Measure how learnings are driving business (sales) outcomes.

## How it works

### Entry point
Users access Reports via the Reports tab in the main navbar. On click, they land on a role-specific default view:
- Admin → Org overview
- Sales Manager → My Team view
- Course Creator → My Content view
- Learner → My Progress
- Leadership → Business Outcomes

### Global filters (always visible, top bar)
- Date range picker (Last 7 days, 30 days, Quarter, Custom)
- Org selector (Org → Region → Team → Rep)
- Segment switch (Myself / My Team / Other Teams / Entire Org)
- Learning type filter (Course, Simulation, Podcast, All)
- Skill filter (dropdown/multi-select)
- Status filter (Not Started, In Progress, Completed)
- Compare toggle (User vs Team / Team vs Org)

### Role-specific dashboard layouts

**Admins**
- KPI strip: Active learners, Active creators, number of Learnings Completed, number of Learnings Published
- Charts: Funnel (Assign → Start → Complete → Pass), Completion rate by team, Ramp-up time, Time spent learning (stacked bar by type)
- Tables: Team-level rollups with drilldown to learners

**Sales Managers**
- KPI strip: Team completion %, Avg score, Skills gained, number of Active learners
- Charts: Team completion vs target, Skill breadth and depth (bar or radar), Simulation performance tiles (Discovery, Cold, Follow-up), Call aspect radar, Improvement trends in call aspects
- Leaderboard table: Top learners, learners needing attention

**Course Creators**
- KPI strip: Completion %, Avg ramp-up, Avg score, Attempts-to-pass
- Charts: My course completion funnel, Attempts vs Pass % (scatter for outliers), Drop-off chart (lesson-level), Peer comparison (my portfolio vs org averages)
- Tables: Course-level performance, Top vs At-risk courses

**Learners**
- KPI strip: My completion %, Avg score, Skills earned, Call scores
- Charts: My learning points trend, My skills breadth and depth (radar), My call simulation improvement (first vs latest)
- Tables: Current learnings (In progress / Not started), Peer comparison

**Leadership**
- KPI strip: Org LRS, SLA % achieved, Skills coverage, New skills
- Charts: Region/team readiness leaderboard, Learning points vs Opportunity closure (correlation tile), Trend: Org-wide completion % and Avg scores
- Tables: Top regions/teams with readiness vs deal outcomes

### Drilldown flow
Clicking any chart element (bar, line, tile) opens a drilldown view:
- Admins: Team → Learners
- Sales Managers: Learner → Attempts/Sim runs
- Course Creators: Course → Lesson/Question stats
- Learners: Asset → Feedback/Recommendations

Breadcrumbs (Org → Team → User) allow navigation back up.

### Seek layer (AI insight cards)
At the top of each role's dashboard, 3-5 auto-generated insight cards in natural language with a CTA are displayed. Examples: "Completion rate in East SDRs dropped 18% this week — Send nudge to 12 reps." / "Cold Call simulations improved by +9 pts vs last month — Share best practice clip."

### Export
Reports can be exported as CSV or PDF, or scheduled as email delivery.

### Learning-level reports (per-learning analytics)
Within a specific learning's manage view, admins/managers/course creators see:

**Overall analytics** (per learning type):
- All types: Number of learners, Completion rate
- Call Simulation: Average score (across latest takes by completed learners), Average call aspect scores
- Course (with assessment): Average score, Average score by assessment, Average days to complete (ramp-up rate)
- Course (without assessment): Average days to complete
- Podcast: Average time spent, Highest drop-off point/topic, Topic with highest/least time spent listening, Timeline graph

**Learner-level analytics (summary view)**:
Each learner row shows 2 data values depending on learning type and status:
- Completed simulation: Latest call's overall score, latest call date, number of takes, link to breakdown
- In-progress simulation: No data (N/A)
- Not-started (any type): Assigned/enrolled date, nudge icon to send reminder email
- Completed course (with assessment): Latest completion score %, number of attempts to pass, latest completion date
- Completed course (without assessment): Latest attempt completed on date, number of attempts
- Completed podcast: Total time spent listening, number of sessions, completed date, completion %
- In-progress podcast: Percentage of completion, time spent listening yet, last engagement date

**Breakdown view (per learner)**:
Expands to show all attempts/takes/sessions sorted by most recent first. Call simulations show: call logged date, duration, overall score, link to recording, link to report. Podcast breakdown: start date, completed date, time spent, drop-off minute/topic, most/least time spent on topic. Note: unique session breakdown is not available for podcasts (technical limitation).

**Across all learnings, inactive (not-started) users**: show assigned/enrolled date and a nudge button to send a reminder email.

### Analytics Revamp specifications
- Time spent on courses = sum of duration of content sessions across lessons within it.
- Time spent card = sum of duration of learning records with started date within the selected time window.
- Learner Insights table: all learners sorted descending by learnings started in the given duration (including learners with 0 at the end); all data points scoped to the selected time range.
- Pass % = out of completed learnings in the duration, how many were passed; podcasts and simulations counted as pass by default.
- Avg score % = out of completed learnings in the duration.
- Course Insights table: all published courses sorted descending by learnings started in the given duration; shows pass %, unique enrolled learners, completions count, average score — all scoped to the time range.
- Course Insights Learnings Tab: all published courses the user is enrolled in; status is not started / in progress / completed (if completed even once, marked as completed); shows enrolled date, completed date, number of attempts, time spent, average score.
- Learning Points definition: every time a learner completes a learning, their score out of 100 becomes points. A user who completes 2 learnings with scores 76% and 82% has 158 learning points total.

## Things to know
- The Reports source document (`4b293736`) pages 4-20 contain competitor research (Second Nature, Showpad, Mindtickle, BigtinCan, Nooks, Udemy, Lessonly/Seismic, Coursera for Business, Workramp, Hyperbound). These are reference UI designs, not HeySales specs. (source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)
- Active Learners definition is still under discussion in the source document (whether to count learners completed vs passed, whether failed completions count). (source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)
- Revenue impact and Learning Completion vs Opportunity Closure metrics are flagged as "to agree" in the source — linkage approach (learning completions vs learning points) is not yet decided. (source: 4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf)

## Related pages
- [[ac]]
- [[course-reports]]
- [[simulation-reports]]
- [[podcast-reports]]
- [[learner-reports]]
- [[learners-list-analytics]]
- [[courses]]
- [[simulations]]
- [[podcasts]]
