# Acceptance Criteria: Video in Simulations

**Summary**: Defines how video mode works in simulations, including camera permission, parallel video display, and recording in reports.

**Sources**: `raw/a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf`

**Last updated**: 2026-05-25

---

## AC-VS-01: Creator chooses video or audio mode

GIVEN a creator is configuring a simulation
WHEN they set up the simulation type
THEN they can choose between video mode (camera on) and audio-only mode

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-02: Learner grants camera permission

GIVEN a simulation is configured in video mode
WHEN the learner starts the simulation
THEN the system requests camera permission before the simulation begins

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-03: Parallel video display during simulation

GIVEN a video-mode simulation is active
WHEN the learner is in the simulation
THEN they see the prospect's image and their own live video feed displayed in parallel on screen

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-04: Recording included in post-completion report

GIVEN the learner completes a video-mode simulation
WHEN the post-completion report is generated
THEN the session recording is included in the report

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-05: Manager can view recordings in reports

GIVEN a manager is reviewing a learner's simulation report
WHEN the report contains a session recording
THEN the manager can view the recording from within the report

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

---

## Related pages
- [[overview]]
- [[simulations]]
- [[simulation-reports]]
- [[simulation-call-recording]]
