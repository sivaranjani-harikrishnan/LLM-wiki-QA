# Feature: Simulations

**Summary**: Simulations are AI-powered role-play sales calls where learners practise against an AI prospect; their performance is scored against a configurable scorecard.

**Sources**: `Custom Scorecards - Scorecard creation.csv`, `Custom Scorecards - Simulation creation (1).csv`, `Simulations Reports - Simulation Reports.csv`, `Simulation Call Recording - Sheet1.csv`, `Profile extraction - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Simulations allow sales reps to practice call types (Discovery, Cold Call, Follow-up, Elevator Pitch) in a safe environment. The AI acts as a prospect. After the call, an AI-generated report scores the learner against the selected scorecard.

## Who uses it

- **Admins / Content Publishers**: Create, configure, publish, and assign simulations; view all learner reports
- **Learners**: Take the simulation, view their own report, retake if needed

## How it works

### Creation (two-step flow)
**Step 1**: Time, Difficulty Level, Scorecard selection
- Default scorecard pre-populated from account's current default
- Admin can preview (navigates to scorecard detail) or change (shows filtered scorecard list by call type)

**Step 2**: Profile creation
- Company profile, Buyer profile, Buyer needs
- Optional: Upload an MP4 or MP3 recording ("Add Source" / Profile Extraction) to auto-populate the profile from a real call transcript
- Supported upload types for profile extraction: MP4, MP3 only (not images or paged files)

### Profile Extraction
When admin uploads a call recording:
1. Click "Add Source" in scenario screen → Call recording slider opens
2. Click "Upload new call" → local file picker (MP4/MP3 only)
3. After upload, "Add Source" button changes to "Generate"
4. Click Generate → "transcribing the call recording" placeholder shown
5. On success: Company profile, Buyer profile, Buyer needs auto-filled from transcript
6. Previously uploaded calls are listed and reusable across simulations
7. Call library is account-scoped (Account A's calls not visible to Account B)
8. Deleting an extracted call does not affect simulations already generated from it

### Publishing
- Save → draft state
- Publish → active; Congratulations screen shown
- Discard reverts to last published version
- Delete removes simulation from Studio and Manage Course; learners can no longer access it

### Learner experience
- Learner starts call via browser (camera + mic, or audio-only)
- Timer runs during call
- Call under 2 minutes → report marked as NA (not scored)
- Call of 2+ minutes → AI generates report using tagged scorecard

### Call types
- Discovery
- Cold Call (additional Brand Positioning metric in report beyond discovery call metrics)
- Follow-up
- Elevator Pitch (monologue; see [[elevator-pitch]])

## Things to know

- Edits to a published simulation (name, banner, skill, duration, etc.) made in Studio do NOT retroactively affect the simulation when embedded in a course (source: `Simulation and Podcast in Courses - Sheet1.csv` TC0032)
- A simulation can be added to multiple courses simultaneously (source: TC0034)
- If a simulation is deleted from Studio, it is removed from all courses it was embedded in (source: TC0033)
- Brand Positioning is an additional metric shown in Cold Call simulation reports (source: `12817417-creating-a-call-simulation-on-heysales.pdf`)
- Default scorecard changes in Settings do NOT affect already-published simulations (source: `Elevator pitch - phase 1 - Sheet2.csv` TC0011)

## Scorecard parameters tested in Simulation Reports

- Conversation Quality
- Prospect Engagement
- Brand Positioning
- Understanding Buyer Needs
- Buying Intent Qualification
- Next Steps & Call Progression

(source: `Simulations Reports - Simulation Reports.csv`)

## Related pages

- [[elevator-pitch]]
- [[simulation-reports]]
- [[simulation-call-recording]]
- [[custom-scorecards]]
- [[profile-extraction]]
- [[podcast-simulation-in-courses]]
