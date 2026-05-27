# HeySales Wiki — Index

**Summary**: Complete table of contents for the HeySales knowledge base.

**Last updated**: 2026-05-25 (third-pass ingest: 5 research-stage features added)

---

## Product context

| Page | Description |
|---|---|
| [[heysales-overview]] | What HeySales is, core modules, key architectural facts |
| [[user-roles]] | Admin, Content Publisher, Learner, BI Analyst — access levels |
| [[learning-types]] | Courses, Podcasts, Simulations, Microlearning — comparison and definitions |

---

## Features

### Simulations

| Page | Description |
|---|---|
| [[simulations/overview]] | How simulations are created, configured, and played by learners |
| [[simulations/ac]] | ACs for knowledge assessment (Fact Check) and video mode in simulations |
| [[simulations/test-coverage]] | Test cases for simulation creation, profile extraction |
| [[elevator-pitch/overview]] | Timed monologue simulation variant (no AI prospect); Video/Audio modes |
| [[elevator-pitch/ac]] | ACs for scorecard filtering by call type; elevator pitch exempt from call-type filter |
| [[elevator-pitch/test-coverage]] | Phase 1 (creation, 25 TCs) + Phase 2 (learner experience, 70 TCs) |
| [[knowledge-assessment/overview]] | Fact Check parameter: claims vs knowledge base, no score impact, hidden when clean |
| [[knowledge-assessment/ac]] | 5 ACs for Fact Check in simulation reports |
| [[video-in-simulations/overview]] | Camera-on simulations: creator chooses mode, recording in report, manager review |
| [[video-in-simulations/ac]] | 5 ACs for video mode |
| [[simulation-foreign-languages/overview]] | Language selection per simulation; AI prospect communicates entirely in chosen language |
| [[simulation-foreign-languages/ac]] | 8 ACs for foreign language simulations |
| [[profile-extraction/overview]] | Upload MP4/MP3 to auto-fill simulation scenario from real call transcript |
| [[profile-extraction/ac]] | Points to simulation-call-recording/ac for extraction ACs (AC-SCR-08 to AC-SCR-14) |
| [[simulation-reports/overview]] | Aggregate metrics: completion rate, avg score, time spent, ranking |
| [[simulation-reports/ac]] | 20 ACs for simulation analytics and reporting |
| [[simulation-reports/test-coverage]] | 59 TCs for simulation reporting |
| [[simulation-call-recording/overview]] | Call recording slider: audio playback + transcript in detailed report |
| [[simulation-call-recording/ac]] | 14 ACs for recording playback and profile extraction upload flow |
| [[simulation-call-recording/test-coverage]] | 10 TCs for call recording slider |

### Scorecards

| Page | Description |
|---|---|
| [[custom-scorecards/overview]] | Create/manage scorecards; default scorecard protection; call type filtering |
| [[custom-scorecards/ac]] | 10 ACs: Scorecards tab, non-deletable default, create/clone, map to call types, specificity logic |
| [[custom-scorecards/test-coverage]] | 48 + 17 TCs for scorecard creation and simulation selection |

### Podcasts

| Page | Description |
|---|---|
| [[podcasts/overview]] | AI-generated audio: Conversational, Monologue, Narrative; 5-asset max; SEEK editing |
| [[podcasts/ac]] | 18 ACs: creation flow, audio types, error handling, notifications, source asset viewer |
| [[podcasts/test-coverage]] | 42 + 56 TCs covering creation, audio types, Narrative quality, editing, learner views |
| [[podcast-enhancements/overview]] | Enhancement details: audio type, asset management, errors, notifications, source viewer |
| [[podcast-enhancements/ac]] | Points to podcasts/ac (enhancements ingested as part of core podcasts feature) |
| [[podcast-enhancements/test-coverage]] | 42 TCs for podcast enhancements |
| [[podcast-reports/overview]] | Completion rate, total listen time, avg listen time (replay does not increment metrics) |
| [[podcast-reports/ac]] | 4 ACs: Completion Rate, Total Time Spent, Avg Time Spent, listen time graph |
| [[podcast-reports/test-coverage]] | 20 TCs for podcast reporting |

### Courses

| Page | Description |
|---|---|
| [[courses/overview]] | Course structure with lessons, assessments, sections, podcasts, simulations |
| [[courses/ac]] | 18 ACs: scheduling, archiving, due dates, progress bar, completion screen |
| [[course-reports/overview]] | Pass %, avg score, time spent, Q&A breakdowns, sections-based report structure |
| [[course-reports/ac]] | 8 ACs: overview cards, row clickability, Latest Score, last 3 attempts, ranking |
| [[course-reports/test-coverage]] | 77 TCs for course reporting |
| [[sections-in-courses/overview]] | Optional section grouping: creation, rearranging, learner view, progress bar, platform differences |
| [[sections-in-courses/ac]] | 19 ACs: section creation, content management, learner view, completion, mobile/demo URL differences |
| [[sections-in-courses/test-coverage]] | 49 TCs for sections |
| [[podcast-simulation-in-courses/overview]] | Pick from Studio: adding published podcasts and simulations to courses |
| [[podcast-simulation-in-courses/ac]] | 13 ACs: podcast global completion, simulation per-course completion, course-end scoring, reporting |
| [[podcast-simulation-in-courses/test-coverage]] | 49 TCs for podcast/simulation in courses |

### Real Call Scoring

| Page | Description |
|---|---|
| [[real-call-scoring/overview]] | Zoom + HubSpot or MS Dynamics integration; trigger conditions; multi-invitee rules |
| [[real-call-scoring/ac]] | 12 ACs: rejection criteria, Zoom/HubSpot flow, Fireflies, Plaud, account-level controls |
| [[real-call-scoring/test-coverage]] | 20 HubSpot TCs + 26 MS Dynamics TCs |
| [[call-library/overview]] | Browsable history of all scored real calls with metadata, score %, and recording |
| [[call-library/ac]] | 8 ACs: list view columns, recency ordering, detailed view, manual upload, bulk upload |
| [[call-library/test-coverage]] | 30 TCs for Call Library |
| [[call-classification/overview]] | AI layer classifying call type before assessment; Phase 1 discovery-only pass-through |
| [[call-classification/ac]] | 8 ACs: AI classification, Phase 1 scope, per-account configuration, UI tag |
| [[call-redaction/overview]] | PII redaction before LLM; original transcript visible in UI reports |
| [[call-redaction/ac]] | 5 ACs: redaction before LLM, original shown in UI, applies to integration and manual uploads |

### Microlearning

| Page | Description |
|---|---|
| [[microlearning/overview]] | Private AI articles for every user; prompt + assets required; history pane; strictly private |
| [[microlearning/ac]] | 6 ACs: text+query inputs, 1-pager output, irrelevant query fails, no strict word count |
| [[microlearning/test-coverage]] | 31 TCs for Let's Learn module |
| [[microlearning-podcast/overview]] | Private audio generated from Microlearning article; not visible to admins |
| [[microlearning-podcast/ac]] | 7 ACs: right panel option, type+duration choice, private, icon only when generated |

### Analytics and Reporting

| Page | Description |
|---|---|
| [[reports/overview]] | Role-aware analytics dashboard: Admin, Sales Manager, Course Creator, Learner, Leadership |
| [[reports/ac]] | 22 ACs: role dashboards, global filters, drilldown, AI insight cards, time-spent calc, learning-level analytics |
| [[learner-reports/overview]] | Stage-based rep scorecard: Readiness (Stage 1), Call Excellence (Stage 2), Win Rate (Stage 3) |
| [[learner-reports/ac]] | 13 ACs: north star metric per stage, pillar rules, floor rule, transfer gap, win rate, rep self-view |
| [[learners-list-analytics/overview]] | In-Progress column (courses + podcasts only); completion data per learning type |
| [[learners-list-analytics/ac]] | 14 ACs: per learning type and learner status data, flag icons, score colours, floor rule indicators |
| [[learners-list-analytics/test-coverage]] | 18 TCs for learner list analytics |

### Notifications

| Page | Description |
|---|---|
| [[due-date-notifications/overview]] | Due date picker (specific/relative); cascading reminder schedule (50%/7d/3d/1d); no-clash rule |
| [[due-date-notifications/ac]] | 20 ACs: assignment-only scope, specific/relative dates, 5 notification triggers, overdue tracking |
| [[due-date-notifications/test-coverage]] | 75 TCs for due dates and reminders |
| [[push-notifications/overview]] | Browser permission prompt; deeplink to learning; offline delivery; device settings |
| [[push-notifications/ac]] | 12 ACs: permission prompt, allow/deny, assignment trigger, deeplink, offline, deleted learning |
| [[push-notifications/test-coverage]] | 12 TCs for push notifications |

### Search

| Page | Description |
|---|---|
| [[ai-search/overview]] | AI search in Manage Courses: name > skill > description ranking; Atlas Search; NLP queries |
| [[ai-search/ac]] | 8 ACs: Phase 1 scope, keyword extraction, fields searched, ranking order, partial match |
| [[ai-search/test-coverage]] | 29 TCs for AI search |

### Mobile

| Page | Description |
|---|---|
| [[mobile-deeplinking/overview]] | Notification email deeplinks to app; app-not-installed redirects to stores |
| [[mobile-deeplinking/ac]] | 6 ACs: logged-in navigation, logged-out, app not installed, expired session, wrong user, cross-platform |
| [[mobile-deeplinking/test-coverage]] | 6 TCs for deeplinking |
| [[no-permission-offline/overview]] | No Permission page (no HeySales access) and Offline screen behaviour |
| [[no-permission-offline/ac]] | 9 ACs: no-permission login blocking, offline on main screens vs content consumption |
| [[no-permission-offline/test-coverage]] | 12 TCs for error screens |

### Platform / Studio Features

| Page | Description |
|---|---|
| [[phonics-instructions/overview]] | Add phonetic spellings for names/terms; global application across all TTS audio |
| [[phonics-instructions/ac]] | 7 ACs: add phonetics, global application, preview, instance count, immediate effect |
| [[assistant/overview]] | AI assistant with 5 modes: Knowledge (Seek), Creation, Search, Recommendation, Shortcuts |
| [[assistant/ac]] | No formal ACs yet; source document is prompt pattern examples |

### Planned / Early-Stage Features

| Page | Description |
|---|---|
| [[live-call-help/overview]] | Real-time AI assist during live calls: knowledge answers, objection handling, buying signals |
| [[live-call-help/ac]] | No formal ACs yet; source document is a design brief and competitor research |
| [[crm-integration/overview]] | CRM integration (Sandler/HubSpot context) and CRM Entry Automation from real calls |
| [[crm-integration/ac]] | No formal ACs yet; source documents are a screenshot and a one-line intent statement |
| [[gamification/overview]] | Planned gamification of learning platform to boost adoption (initial use case: Evolus) |
| [[gamification/ac]] | No formal ACs yet; requirements field in source document is empty |
| [[teaching-assistant/overview]] | Research stub — two YouTube video references; no requirements documented yet |
| [[field-sales/overview]] | Planned Plaud/Fireflies × CRM extension for non-Zoom field sales calls; research stage |
| [[linkedin-import/overview]] | Competitor research (SecondNature, Rehers.Ai) — no HeySales ACs yet |
| [[sms-notifications/overview]] | Competitor research (Blackboard Ultra) — no HeySales ACs yet |
| [[custom-assessments/overview]] | Competitor research (Eduviva, Speakology AI, TestPortal) — no HeySales ACs yet |

---

## Audience guides

| Page | Description |
|---|---|
| [[for-testing]] | QA engineers: how to find test cases, preconditions, coverage gaps |
| [[for-support]] | Support agents: quick-reference for common customer issues |
| [[for-engineering]] | Engineers: formulas, state machines, integration architecture |
| [[for-pm]] | Product managers: feature inventory, decisions, contradictions |
| [[for-onboarding]] | Sales and onboarding: how to explain and demo HeySales |
| [[for-new-hires]] | Start here if you're new to HeySales |

---

## Meta

| Page | Description |
|---|---|
| [[content-standards]] | Page formats, citation rules, writing style, source trust hierarchy |
| [[how-to-use-this-wiki]] | Prompt patterns and navigation guide by role |

---

## Infrastructure

| Page | Description |
|---|---|
| [[log]] | Append-only record of all wiki operations |
| [[contradictions]] | Known conflicts between source documents |
| [[usage]] | Token usage and cost per operation |
