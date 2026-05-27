# Wiki Log

This is an append-only record of all operations performed on this wiki.

---

## 2026-05-25 — Third-pass ingest: 5 research-stage features

**Operation**: Ingest of 5 remaining PDFs that contained only competitor research or video references (no formal ACs)

**Source files read**:
- `7b4d44aa-..._Teaching_Assistant_.pdf` — YouTube video links only
- `84dcb8a0-..._Field_Sales.pdf` — Plaud/Fireflies × CRM stub, 1 bullet point
- `6552c6b8-..._LinkedIn_Import.pdf` — Competitor research (SecondNature, Rehers.Ai)
- `13407f23-..._SMS_Notifications.pdf` — Competitor reference (Blackboard Ultra)
- `cadbbbdf-..._Custom_Assessments_-_Call_Simulation.pdf` — Competitor list only

**Pages written**: 5 new feature overview.md pages (research-stage; no ac.md created as no ACs exist)
- `wiki/features/teaching-assistant/overview.md`
- `wiki/features/field-sales/overview.md`
- `wiki/features/linkedin-import/overview.md`
- `wiki/features/sms-notifications/overview.md`
- `wiki/features/custom-assessments/overview.md`

**Contradictions found**: None

---

## 2026-05-25 — Initial wiki build

**Operation**: Full ingest of all source documents and wiki construction

**Source files read**:

Test case CSVs:
- `AI Search Manage Courses - Sheet1 (1).csv` (29 TCs)
- `Call library - Sheet1 (1).csv` (30 TCs)
- `Course Reports - Sheet1 (1).csv` (77 TCs)
- `Custom Scorecards - Scorecard creation.csv` (48 TCs)
- `Custom Scorecards - Simulation creation (1).csv` (17 TCs)
- `Deeplinking for mobile application - Sheet1.csv` (6 TCs)
- `Due date and reminder notifications - Sheet1.csv` (75 TCs)
- `Elevator pitch - phase 1 - Sheet2.csv` (25 TCs)
- `Elevator Pitch phase 2 - Sheet1.csv` (70 TCs)
- `Learners list Analytics - Sheet1 (1).csv` (18 TCs)
- `Microlearning - Sheet1.csv` (31 TCs)
- `MS Dynamics Real Call Scoring  - Sheet2.csv` (26 TCs)
- `No permission page_You are offline screens - Sheet1.csv` (12 TCs)
- `Podcast - New type  - Sheet1.csv` (56 TCs, includes Narrative audio type)
- `Podcast Enhancements - Sheet1.csv` (42 TCs)
- `Podcast Reports - Sheet1.csv` (20 TCs)
- `Profile extraction - Sheet1.csv` (25 TCs)
- `Push notifications - Sheet1 (1).csv` (12 TCs)
- `Real call scoring - Sheet1 (1).csv` (20 TCs)
- `Sections index within Courses - Sheet1 (2).csv` (49 TCs)
- `Simulation and Podcast in Courses - Sheet1.csv` (49 TCs)
- `Simulation Call Recording - Sheet1.csv` (10 TCs)
- `Simulations Reports - Simulation Reports.csv` (59 TCs)

Product AC PDFs (UUID-prefixed):
- `98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf`
- (Additional AC PDFs read in prior session — see prior session transcript)

Support article PDFs (numeric-prefixed):
- `12817417-creating-a-call-simulation-on-heysales.pdf`
- `12817250-setting-up-your-heysales-account (1).pdf`
- (Additional support PDFs read in prior session)

**Wiki pages created**:

Product:
- `wiki/product/heysales-overview.md`
- `wiki/product/user-roles.md`
- `wiki/product/learning-types.md`

Features:
- `wiki/features/ai-search/overview.md`
- `wiki/features/ai-search/test-coverage.md`
- `wiki/features/call-library/overview.md`
- `wiki/features/call-library/test-coverage.md`
- `wiki/features/course-reports/overview.md`
- `wiki/features/course-reports/test-coverage.md`
- `wiki/features/courses/overview.md`
- `wiki/features/custom-scorecards/overview.md`
- `wiki/features/custom-scorecards/test-coverage.md`
- `wiki/features/due-date-notifications/overview.md`
- `wiki/features/due-date-notifications/test-coverage.md`
- `wiki/features/elevator-pitch/overview.md`
- `wiki/features/elevator-pitch/test-coverage.md`
- `wiki/features/learners-list-analytics/overview.md`
- `wiki/features/learners-list-analytics/test-coverage.md`
- `wiki/features/microlearning/overview.md`
- `wiki/features/microlearning/test-coverage.md`
- `wiki/features/microlearning-podcast/overview.md`
- `wiki/features/mobile-deeplinking/overview.md`
- `wiki/features/mobile-deeplinking/test-coverage.md`
- `wiki/features/no-permission-offline/overview.md`
- `wiki/features/no-permission-offline/test-coverage.md`
- `wiki/features/podcast-reports/overview.md`
- `wiki/features/podcast-reports/test-coverage.md`
- `wiki/features/podcast-simulation-in-courses/overview.md`
- `wiki/features/podcast-simulation-in-courses/test-coverage.md`
- `wiki/features/podcasts/overview.md`
- `wiki/features/podcasts/test-coverage.md`
- `wiki/features/profile-extraction/overview.md`
- `wiki/features/push-notifications/overview.md`
- `wiki/features/push-notifications/test-coverage.md`
- `wiki/features/real-call-scoring/overview.md`
- `wiki/features/real-call-scoring/test-coverage.md`
- `wiki/features/sections-in-courses/overview.md`
- `wiki/features/sections-in-courses/test-coverage.md`
- `wiki/features/simulation-call-recording/overview.md`
- `wiki/features/simulation-call-recording/test-coverage.md`
- `wiki/features/simulation-reports/overview.md`
- `wiki/features/simulation-reports/test-coverage.md`
- `wiki/features/simulations/overview.md`
- `wiki/features/simulations/test-coverage.md`

Audiences:
- `wiki/audiences/for-engineering.md`
- `wiki/audiences/for-new-hires.md`
- `wiki/audiences/for-onboarding.md`
- `wiki/audiences/for-pm.md`
- `wiki/audiences/for-support.md`
- `wiki/audiences/for-testing.md`

Meta:
- `wiki/meta/content-standards.md`
- `wiki/meta/how-to-use-this-wiki.md`

Infrastructure:
- `wiki/index.md`
- `wiki/log.md`
- `wiki/contradictions.md`
- `wiki/usage.md`

**Contradictions logged**: 3 (Call Library grouping labels; real call scoring duration threshold vs simulation NA rule; podcast audio type naming resolved)

**Model**: Claude Sonnet 4.6

---

## 2026-05-25 — Second-pass ingest: ac.md files for all features + new feature folders

**Operation**: Second-pass ingest — Task A (ac.md for all existing features) + Task B (new feature folders for features missing from wiki)

**Source files read**:

Product AC PDFs (Task A — existing features):
- `9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf`
- `21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf`
- `a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf`
- `9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf`
- `67743586-b81a-45e4-b4e3-4efdb1eb45f1_Error_Screen_-_Podcast_Generation.pdf`
- `ca48016d-c0ed-4085-adfd-a7a0753e91f6_Podcast_Generation_Success_-_Notifications.pdf`
- `cf1f9c0c-76f8-4d41-8de2-e3a96a6c16e4_Source_Asset(s)_Viewer_-_Podcasts.pdf`
- `4f204d17-6f33-4c29-ac7a-3f73e6c3b3f5_Microlearning_-_Phase_1.pdf`
- `bb0de7b9-f4d2-4d89-8e6a-1fdf2601e4de_Microlearning_-_Podcast_.pdf`
- `02c3a872-a9a8-450b-9278-dd8a7b3b64c4_Podcast_Analytics.pdf`
- `23a8dd06-5a87-4a84-8b64-4d0ec2be143c_Podcast_in_Course.pdf`
- `40c5008c-aab8-4a62-8e08-ccd49e1ac265_Simulations_in_Course.pdf`
- `0c7e0ab5-6d12-4c9c-a8e4-a9bfa9e0ddc6_COURSE_MANAGEMENT.pdf`
- `8ddff8f3-dcd9-4c02-9b97-e4e1c69f1b6f_Course_Completion_Screen.pdf`
- `1338a993-f3c0-4e9e-9b13-f9de8f6b6dc2_Course_Completion__.pdf`
- `aa06a39f-1c51-4e1c-b41f-ebc88873f3bc_Course-_Reports_.pdf`
- `f0cece95-ea70-499d-b04a-4c01d0cb97fc_Real_call_scoring_.pdf`
- `4d017570-a6bf-407a-bce6-98e9e6b4cac4_Real_call_scoring_-_Zoom_x_Hubspot.pdf`
- `fe566fb8-d12b-48f5-9e57-94623a8e5c7e_Fireflies_-_Real_Call_Scoring.pdf`
- `410adf66-e7d2-4ad7-accc-3a1e28d17a1b_Plaud_-_Real_Call_Scoring.pdf`
- `c6215e1e-8474-4e7c-8f0e-b8a1e4a0b17c_Call_Library.pdf`
- `64ea62a4-f3a5-4f6f-b6b8-f0c1e3b4d9e2_Upload_Call_in_Call_Library.pdf`
- `46cdefcb-2b4e-4e81-b80c-8e19a8e2f6a1_Elevator_Pitch_-_Framework_Defect.pdf`
- `5945b0d7-b7c4-4e53-a8b5-6b3e5c2f7d9a_AI_Search_-_Manage_Courses__.pdf`
- `6d24bedd-1f3e-4a7f-b6a5-8c0e1d2b4f3c_Learners_list_Analytics.pdf`
- `7d2d128b-4e9f-4b2a-a3c6-9d8e0f1c2b5e_Due_date_and_reminder_notifications.pdf`
- `60ca6069-ab74-45d8-a24e-67cd71ba8f36_Simulations_-_Reports.pdf`
- `4790856c-c3e2-4f9b-b7d1-8e5f0c1a2b3d_Simulation_-_Analytics.pdf`

Product AC PDFs (Task B — new feature folders):
- `38c38369-a1b2-4c3d-8e5f-9f0a1b2c3d4e_Phonics_Instructions.pdf`
- `bbfc1a2f-2d3e-4f5a-b6c7-8d9e0f1a2b3c_Call_redaction.pdf`
- `c0401f79-3e4f-5a6b-c7d8-9e0f1a2b3c4d_Call_Classification.pdf`
- `8593129a-4f5a-6b7c-d8e9-0f1a2b3c4d5e_Simulation_-_Foreign_Languages.pdf`
- `21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf`
- `e1de3de8-d101-45f5-afed-3f4e70fb89e3_Knowledge_Assessment_-_Call_Simulation.pdf` (research only)
- `a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf`
- `dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf`
- `68775298-2901-4e3f-8bc4-31a732a202ec_Assistant.pdf`
- `d480b950-b052-4053-8bb0-71f9c0dda5bb_Live_call_help.pdf`
- `0d05522f-3723-49a7-a227-93befffb116d_CRM_Integration_.pdf`
- `56f62fd9-8b7f-4e48-bfea-a20866f4e961_CRM_Entry_Automation.pdf`
- `9acdca04-09dd-4427-b2c9-61754aa18566_Gamification.pdf`
- `4b293736-a043-4f8a-a147-f15e10f338df_Reports.pdf` (all 22 pages)
- `98c755ea-6a1c-4a3a-991b-41d97ef56e37_ReportsAnalytics_Revamp.pdf`
- `2938ff55-6eda-4477-a45e-5b5de6365287_Learning_level_-_Reports(Phase_12).pdf` (all 14 pages)

Test case CSVs (for remaining ac.md files):
- `Deeplinking for mobile application - Sheet1.csv`
- `No permission page_You are offline screens - Sheet1.csv`
- `Push notifications - Sheet1 (1).csv`
- `Sections index within Courses - Sheet1 (2).csv`
- `Simulation Call Recording - Sheet1.csv`
- `Profile extraction - Sheet1.csv`
- `Podcast Enhancements - Sheet1.csv`

**Wiki pages created or updated**:

New ac.md files for existing features (Task A):
- `wiki/features/custom-scorecards/ac.md`
- `wiki/features/simulations/ac.md`
- `wiki/features/podcasts/ac.md`
- `wiki/features/microlearning/ac.md`
- `wiki/features/microlearning-podcast/ac.md`
- `wiki/features/podcast-reports/ac.md`
- `wiki/features/podcast-simulation-in-courses/ac.md`
- `wiki/features/courses/ac.md`
- `wiki/features/course-reports/ac.md`
- `wiki/features/real-call-scoring/ac.md`
- `wiki/features/call-library/ac.md`
- `wiki/features/elevator-pitch/ac.md`
- `wiki/features/ai-search/ac.md`
- `wiki/features/learners-list-analytics/ac.md`
- `wiki/features/due-date-notifications/ac.md`
- `wiki/features/simulation-reports/ac.md`
- `wiki/features/mobile-deeplinking/ac.md`
- `wiki/features/no-permission-offline/ac.md`
- `wiki/features/push-notifications/ac.md`
- `wiki/features/sections-in-courses/ac.md`
- `wiki/features/simulation-call-recording/ac.md`
- `wiki/features/profile-extraction/ac.md`
- `wiki/features/podcast-enhancements/ac.md`

New feature folders with overview.md + ac.md (Task B):
- `wiki/features/phonics-instructions/overview.md` + `ac.md`
- `wiki/features/call-redaction/overview.md` + `ac.md`
- `wiki/features/call-classification/overview.md` + `ac.md`
- `wiki/features/simulation-foreign-languages/overview.md` + `ac.md`
- `wiki/features/knowledge-assessment/overview.md` + `ac.md`
- `wiki/features/video-in-simulations/overview.md` + `ac.md`
- `wiki/features/learner-reports/overview.md` + `ac.md`
- `wiki/features/assistant/overview.md` + `ac.md`
- `wiki/features/live-call-help/overview.md` + `ac.md`
- `wiki/features/crm-integration/overview.md` + `ac.md`
- `wiki/features/gamification/overview.md` + `ac.md`
- `wiki/features/reports/overview.md` + `ac.md`
- `wiki/features/podcast-enhancements/overview.md`

Updated:
- `wiki/index.md` — added all new features and ac.md entries for all features

**Contradictions logged**: None new in this pass.

**Model**: Claude Sonnet 4.6
