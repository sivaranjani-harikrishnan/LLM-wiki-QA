# Audience Guide: Product Management

**Summary**: Feature definitions, intended behaviour, and known gaps for PMs working on HeySales.

**Last updated**: 2026-05-25

---

## Feature inventory

| Feature | Status | Key source |
|---|---|---|
| Custom Scorecards | Active | `Custom Scorecards - Scorecard creation.csv` |
| Simulations | Active | Multiple CSVs |
| Simulation Reports | Active | `Simulations Reports - Simulation Reports.csv` |
| Simulation Call Recording | Active | `Simulation Call Recording - Sheet1.csv` |
| Elevator Pitch (Phase 1 + 2) | Active | `Elevator pitch - phase 1 - Sheet2.csv`, `Elevator Pitch phase 2 - Sheet1.csv` |
| Podcasts (Conversational, Monologue, Narrative) | Active | `Podcast Enhancements - Sheet1.csv`, `Podcast - New type  - Sheet1.csv` |
| Podcast Reports | Active | `Podcast Reports - Sheet1.csv` |
| Real Call Scoring (HubSpot) | Active | `Real call scoring - Sheet1 (1).csv` |
| Real Call Scoring (MS Dynamics) | Active | `MS Dynamics Real Call Scoring  - Sheet2.csv` |
| Call Library | Active | `Call library - Sheet1 (1).csv` |
| Microlearning (Let's Learn) | Active | `Microlearning - Sheet1.csv` |
| Microlearning Podcast | Active | `Microlearning - Sheet1.csv` |
| AI Search (Manage Courses) | Active | `AI Search Manage Courses - Sheet1 (1).csv` |
| Learners List Analytics (In-Progress column) | Active | `Learners list Analytics - Sheet1 (1).csv` |
| Due Date and Reminder Notifications | Active | `Due date and reminder notifications - Sheet1.csv` |
| Push Notifications (Mobile) | Active | `Push notifications - Sheet1 (1).csv` |
| Course Reports | Active | `Course Reports - Sheet1 (1).csv` |
| Sections in Courses | Active | `Sections index within Courses - Sheet1 (2).csv` |
| Podcast & Simulation in Courses | Active | `Simulation and Podcast in Courses - Sheet1.csv` |
| Profile Extraction | Active | `Profile extraction - Sheet1.csv` |
| Mobile Deeplinking | Active | `Deeplinking for mobile application - Sheet1.csv` |
| No Permission / Offline Screens | Active | `No permission page_You are offline screens - Sheet1.csv` |

## Key product decisions to understand

### Scorecard defaults
- Every account always has exactly ONE default scorecard
- The Paperflite (MEDDIC) scorecard is the permanent fallback — it cannot be deleted or renamed
- Custom scorecards can be set as default account-wide
- Changing default does NOT affect already-published simulations (by design)

### Real Call Scoring architecture
- HubSpot = user-level Zoom (each rep connects own Zoom)
- MS Dynamics = account-level Zoom (one integration for entire account)
- This is intentional — different CRM architectures require different integration models

### Microlearning privacy
- Let's Learn is strictly private — not a team or admin feature
- Even admin accounts cannot see another user's articles or podcasts
- This is a deliberate trust/privacy decision

### Podcast audio types
- Three types: Conversational, Monologue, Narrative
- Narrative is the newest; specific quality requirements (no fillers, no random voices)
- Default for new and existing podcasts: Conversational

### Sections in courses
- Sections NOT shown in mobile app (web and Demo URL only)
- Sections are optional — courses work without them
- Empty sections block publishing

### Call duration rules (inconsistency between features)
- Simulations: calls under 2 min → NA (not scored)
- Real call scoring (Zoom): calls under 2 min → report IS generated
- This is a known inconsistency between features — see [[contradictions]]

## Unresolved contradictions

See `wiki/contradictions.md` for a complete list of conflicts between source documents.

## Related pages

- [[for-engineering]]
- [[for-testing]]
- [[heysales-overview]]
