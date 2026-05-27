# Feature: Elevator Pitch

**Summary**: Elevator Pitch is a simulation variant where the learner delivers a timed solo monologue to the camera or microphone — no AI prospect responds — and is scored against a scorecard.

**Sources**: `Elevator pitch - phase 1 - Sheet2.csv`, `Elevator Pitch phase 2 - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Unlike standard simulations (where an AI prospect responds), Elevator Pitch is a one-way timed delivery. The learner practises pitching with a countdown timer. The system records the video or audio and scores the performance against the account's default scorecard (or a selected scorecard).

## Who uses it

- **Admins / Content Publishers**: Create, configure, publish, and assign Elevator Pitch simulations
- **Learners**: Start the pitch, deliver within the time limit, view their scored report, retake

## How it works

### Creation flow
1. Navigate to Studio → Create Simulation → Select "Elevator Pitch" (appears alongside Discovery, Cold Call, Follow-on call)
2. Landing screen shows: "Untitled Simulation" title, Pitch Scenario section, Company and Audience section, Format section, Time Bound section, Skills in Focus, All Learners, Assessment Framework, Save/Publish/Back/Delete/Review Error buttons
3. Fill mandatory fields:
   - **Pitch Scenario** (required, no character limit)
   - **Company and Audience** description (required)
4. Choose format:
   - **Video** (default) — camera-based recording
   - **Audio** — microphone-only, shows avatar instead of live camera
5. Choose duration: 30 sec / 1 min / 1 min 30 sec / 2 min (time-bound slider)
6. Assessment Framework defaults to account's current default scorecard; can be changed via the Review option
7. Add Skills and Learners
8. Save → Publish → Congratulations screen

### Editing published simulations
- All fields editable (scenario, audience, time, format, scorecard)
- Changes saved on click Save
- Discard returns to last published version
- Default scorecard changes in Settings do NOT retroactively update published simulations

### Learner experience (Phase 2)
1. Assigned learner sees simulation in My Courses → "Start Call"
2. Unassigned but published → visible in Explore → "Enrol Call"
3. Browser prompts for camera/microphone permission
4. Countdown starts after permission granted
5. Video mode: black screen + live camera, timer, info/restart/end icons
6. Audio mode: avatar + blank screen
7. Info icon shows call info slider
8. Restart requires confirmation
9. Learner can manually end before duration expires → confirmation slider
10. Processing screen shown while report generates
11. Report shows scorecard breakdown (out of 10 per parameter)
12. View call recording slider available (video player for video mode, audio + single avatar for audio mode)
13. Retake available

### UI display
- Simulation card shows "Elevator Pitch" pill/tag, selected duration, creator name and avatar
- Visible in: Studio (Draft + Published sections), Manage Course, learner My Courses, learner Explore

## Things to know

- Duration options: 30 sec, 1 min, 1 min 30 sec, 2 min (source: `Elevator pitch - phase 1 - Sheet2.csv` TC0006)
- Video is selected by default, not Audio (source: TC0007)
- No AI prospect — the learner speaks without any AI response (source: overview)
- Assessment Framework section in creation screen shows framework name + parameters + sub-parameters count (source: TC0008)
- Changing default scorecard in Settings DOES reflect in new Elevator Pitch creations but NOT in already-published ones (source: TC0010, TC0011)
- Clicking Back without saving shows a Save Changes prompt (source: TC0012)
- Clicking Cancel in Save Changes toast retains all entered data (auto-save) (source: TC0013)
- Clicking Discard Changes removes all unsaved edits (source: TC0021)

## Reports
Elevator Pitch uses the same reporting structure as regular simulations:
- Completion Rate card
- Avg Score card
- Avg Time Spent card
- Ranking (by best score)
- Ramp-up rate
- Time Spent (cumulative)
- Attempts Taken card
- Breakdown + attempts dropdown
- Call recording in breakdown

(source: `Elevator Pitch phase 2 - Sheet1.csv`)

## Related pages

- [[simulations]]
- [[simulation-reports]]
- [[simulation-call-recording]]
- [[custom-scorecards]]
