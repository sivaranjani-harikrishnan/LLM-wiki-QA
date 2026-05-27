# Acceptance Criteria: Simulation Call Recording

**Summary**: No formal AC document exists for simulation call recording. Acceptance criteria below are inferred from test cases. See [[test-coverage]] for the full test case list.

**Sources**: `raw/Simulation Call Recording - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Simulation Report — Recording Playback ACs

## AC-SCR-01: Call recording button shown in detailed report

GIVEN an admin or content publisher views the detailed report screen for a simulation
WHEN the report renders
THEN a "Call recording" button with an audio icon is displayed in line with the breakdown and attempts dropdown

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-02: Call recording button shown without retakes dropdown when no retakes

GIVEN a learner has no retakes on a simulation
WHEN the report renders
THEN the attempts dropdown is not displayed; only the call recording button is shown

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-03: Clicking call recording opens slider with call log

GIVEN the call recording button is visible
WHEN the admin clicks it
THEN a slider opens showing the call log for the respective attempt; the list of completed learners slides out of the UI

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-04: Call recording slider UI elements

GIVEN the call recording slider is open
WHEN the slider renders
THEN it displays: heading "Call recording" (top left), close button (top right), call type (e.g. Follow up, Cold call), challenge level, transcript of learner and AI with profile pictures and timestamps, audio slider, volume button, play/pause, forward/reverse 15s buttons, and playback speed button

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-05: Recording updates per attempt selected

GIVEN a learner has multiple attempts
WHEN the admin selects a different attempt
THEN the call log in the recording screen updates to reflect the selected attempt

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-06: NA call shows error in recording slider

GIVEN a learner ended a call within 2 minutes (insufficient data — NA call)
WHEN the call recording slider is opened for that call
THEN an error message is displayed instead of a recording

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-07: Full audio playback controls functional

GIVEN the call recording slider is open with a valid recording
WHEN the admin uses the playback controls
THEN they can play/pause, skip forward/reverse 15 seconds, increase/decrease playback speed, and jump to any point in the audio; the transcript syncs to the current playback position

(source: Simulation Call Recording - Sheet1.csv)

---

## Profile Extraction (Source Upload) ACs

## AC-SCR-08: Admin can upload a call recording as a simulation source

GIVEN an admin is creating or editing a simulation in the scenario screen
WHEN they click "Add source"
THEN a call recording slider opens allowing them to upload an MP3 or MP4 file from their local device

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-09: Only MP3 and MP4 files are accepted for extraction

GIVEN an admin is uploading a file for profile extraction
WHEN they upload a file
THEN only MP3 and MP4 formats are accepted; image files and paged files (e.g. PDF) are rejected

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-10: Successful extraction populates company, buyer, and need fields

GIVEN an admin uploads a valid call recording
WHEN extraction succeeds
THEN the Company profile, Buyer profile, and Buyer need fields in the scenario screen are populated from the extracted call data; the admin can edit the extracted details

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-11: Extraction failure shows error with retry option

GIVEN an admin uploads a file that cannot be processed (e.g. random MP4/MP3 with no usable content)
WHEN extraction fails
THEN "Profile generation failed" is shown with Retry and "Upload new asset" buttons; clicking Retry re-triggers extraction; clicking Upload new asset opens the file picker

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-12: Previously extracted calls are reusable

GIVEN calls have been previously extracted
WHEN an admin creates a new simulation
THEN they can select a previously extracted call from the list; the respective details are applied to the new simulation

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-13: Deleting an extracted call does not affect existing simulations

GIVEN an admin deletes a previously extracted call
WHEN the deletion is confirmed
THEN all simulations generated from that call are not disturbed

(source: Simulation Call Recording - Sheet1.csv)

## AC-SCR-14: Extracted calls are account-scoped

GIVEN Account A has uploaded extracted calls
WHEN a user in Account B views the call recording slider
THEN calls extracted under Account A are not visible in Account B

(source: Simulation Call Recording - Sheet1.csv)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[simulations]]
- [[simulation-reports]]
- [[video-in-simulations]]
