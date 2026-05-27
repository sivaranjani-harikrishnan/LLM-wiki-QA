# Test Coverage: Elevator Pitch

**Summary**: Phase 1 covers creation and configuration (25 TCs); Phase 2 covers learner experience and reporting (70 TCs).

**Sources**: `Elevator pitch - phase 1 - Sheet2.csv`, `Elevator Pitch phase 2 - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Phase 1: Creation TCs

### TC0001: Navigation to Create Simulation screen
**What this tests**: Validate that user can navigate from HeySales to Studio and click on Create Simulation to view Scenario Selection popup; Elevator pitch type visible next to Discovery call, Cold call, Follow-on call

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0002: Selecting Elevator Pitch opens creation screen
**What this tests**: Validate that selecting "Elevator Pitch" navigates user to the Elevator Pitch type creation screen

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0003: UI elements of creation screen
**What this tests**: Validate UI elements — "Untitled Simulation" title, Pitch Scenario section with warning, Company and Audience section with warning, Format section (Video/Audio), Time Bound slider (30s/1m/1m30s/2m), Skills in Focus, All Learners, Save/Publish/Back/Delete/Review Error buttons, Assessment Framework section

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0004–TC0005: Scenario and Audience Description fields
**What this tests**: User can enter text in Scenario Description and Audience Description; warning message removed on input; no character limit

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0006: Time Duration slider
**What this tests**: Validate that user is able to select pitch duration using the Time Duration slider (30 seconds, 1 minute, 1 minute 30 seconds, 2 minutes); only one option selectable at a time

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0007: Video/Audio format selection and default
**What this tests**: Validate that user can select Video or Audio format; Video is selected by default

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0008: Default Assessment Framework displayed
**What this tests**: Validate that the Assessment Framework set as default in Settings is displayed in Elevator Pitch screen; shows framework name, parameters, and sub-parameters count

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0009: Change Assessment Framework
**What this tests**: Validate that user can modify/change the Assessment Framework by clicking Review option

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0010: Updated default framework reflects in new simulations
**What this tests**: Validate that when default Assessment Framework is changed in Settings, the updated framework reflects in Elevator Pitch screen for new simulations

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0011: Updated default framework does NOT reflect in published simulations
**What this tests**: Validate that when default Assessment Framework is changed in Settings, the updated framework is not reflected in published simulations

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0012: Save Changes slider on Back button
**What this tests**: Validate that a Save Changes slider/prompt appears when user clicks Back button after making changes without saving; options: Save / Cancel

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0013: Cancel in Save Changes toast retains data
**What this tests**: Validate that all entered details are auto-saved when user clicks Back button without explicitly clicking Save; clicking Cancel retains data

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0014–TC0016: Save, Publish, Congratulations
**What this tests**: User can save after adding Skills and Learners; Publish button enabled after save; Congratulations message shown after publishing

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0017–TC0020: Post-creation UI
**What this tests**: Created Elevator Pitch simulation shows "Elevator Pitch" pill/tag, duration, creator name, avatar; analytics cards visible (Completion Rate, Avg Score, Avg Time Spent); pill and duration visible in Studio sections and Manage Course

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0021: Discard Changes removes unsaved edits
**What this tests**: Validate that all unsaved changes are removed when user clicks on Discard Changes option from the Save Changes slider/prompt

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0022–TC0023: Delete simulation
**What this tests**: Clicking Delete removes simulation after confirmation; clicking Cancel in delete confirmation closes slider and simulation remains

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

### TC0024–TC0025: Edit simulation
**What this tests**: User can edit all fields (scenario, audience, time, format, scorecard); changes saved and reflected; duration shows correctly in Studio and Manage Course pills for all four duration values

(source: `Elevator pitch - phase 1 - Sheet2.csv`)

---

## Phase 2: Learner experience and reporting TCs

Phase 2 (`Elevator Pitch phase 2 - Sheet1.csv`) covers 70 TCs including:

- Assigned vs unassigned learner flows (My Courses vs Explore)
- Detail page UI (duration in seconds/minutes, simulation type, creator, pitch scenario, company audience, skills)
- Browser permission prompt (camera/microphone)
- Countdown after permission granted
- Video recording screen (black screen + camera, timer, info/restart/end icons)
- Audio recording screen (avatar + blank screen)
- Info icon shows call info slider
- Restart requires confirmation; manual end requires confirmation
- Processing screen after call ends
- Report with scorecard breakdown (out of 10 per parameter)
- View call recording slider (video player for video mode; audio + single avatar for audio mode)
- Retake flow
- Reporting: completion rate, avg score, avg time spent, ranking, ramp-up rate, time spent, attempts taken, breakdown, call recording in breakdown
- Due dates (specific date or time-from-assignment), overdue states
- Green/red hourglass icons in learner list
- Reminder email schedule
- Elevator pitch inside courses
- Elevator pitch in main reports section

(source: `Elevator Pitch phase 2 - Sheet1.csv`)

---

## Related pages

- [[overview]]
- [[simulations]]
- [[simulation-reports]]
