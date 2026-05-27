# Audience Guide: Testing & QA

**Summary**: How QA engineers should navigate and use the HeySales wiki to find test cases, preconditions, and coverage gaps.

**Last updated**: 2026-05-25

---

## How to use this wiki for testing

### Finding test cases for a feature

Every feature folder under `wiki/features/<feature-name>/` contains a `test-coverage.md` file with:
- All test case IDs and titles
- Preconditions
- Steps
- Expected results
- Source CSV file reference

Example: for real call scoring tests, read `wiki/features/real-call-scoring/test-coverage.md`.

### Understanding what is NOT tested

Read the `ac.md` file (if it exists) alongside `test-coverage.md`. Anything in the AC with no corresponding test case is a coverage gap.

### Feature-to-source-file mapping

| Feature | Source CSV |
|---|---|
| Custom Scorecards | `Custom Scorecards - Scorecard creation.csv`, `Custom Scorecards - Simulation creation (1).csv` |
| Simulations | `Custom Scorecards - Simulation creation (1).csv`, `Profile extraction - Sheet1.csv` |
| Simulation Reports | `Simulations Reports - Simulation Reports.csv` |
| Simulation Call Recording | `Simulation Call Recording - Sheet1.csv` |
| Elevator Pitch | `Elevator pitch - phase 1 - Sheet2.csv`, `Elevator Pitch phase 2 - Sheet1.csv` |
| Podcasts | `Podcast Enhancements - Sheet1.csv`, `Podcast - New type  - Sheet1.csv` |
| Podcast Reports | `Podcast Reports - Sheet1.csv` |
| Real Call Scoring (HubSpot) | `Real call scoring - Sheet1 (1).csv` |
| Real Call Scoring (MS Dynamics) | `MS Dynamics Real Call Scoring  - Sheet2.csv` |
| Call Library | `Call library - Sheet1 (1).csv` |
| Microlearning | `Microlearning - Sheet1.csv` |
| AI Search | `AI Search Manage Courses - Sheet1 (1).csv` |
| Learners List Analytics | `Learners list Analytics - Sheet1 (1).csv` |
| Due Date Notifications | `Due date and reminder notifications - Sheet1.csv` |
| Push Notifications | `Push notifications - Sheet1 (1).csv` |
| Course Reports | `Course Reports - Sheet1 (1).csv` |
| Sections in Courses | `Sections index within Courses - Sheet1 (2).csv` |
| Podcast & Simulation in Courses | `Simulation and Podcast in Courses - Sheet1.csv` |
| Mobile Deeplinking | `Deeplinking for mobile application - Sheet1.csv` |
| No Permission / Offline | `No permission page_You are offline screens - Sheet1.csv` |

### Key preconditions to know

- Most HeySales tests require HeySales to be **enabled** on the account
- Scorecard settings tests require **Admin** or **Content Publisher** role
- Real call scoring requires **both** Zoom AND CRM integrations active + call recording toggle ON
- Elevator Pitch Phase 2 requires simulation to be **published** before learner testing
- Profile extraction accepts only **MP4 and MP3** files

### Gotchas and edge cases

- Calls under 2 minutes: marked as NA in simulation reports; still score in real call scoring (different behaviour)
- Default scorecard changes in Settings do NOT affect already-published simulations
- In-Progress column exists for courses and podcasts but NOT simulations
- Sections are NOT shown in mobile app
- Microlearning/Let's Learn articles and podcasts are PRIVATE — never visible to admins (even for testing)
- Narrative podcast audio should be verified for fillers and random voices (specific quality tests in TC0020, TC0047)

### Contradictions to be aware of

See `wiki/contradictions.md` for known discrepancies between source documents, especially around Call Library time grouping labels.

## Related pages

- [[for-support]]
- [[for-engineering]]
- [[for-pm]]
