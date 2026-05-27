# Acceptance Criteria: Simulations

**Summary**: Defines how simulations are conducted, what is assessed (including knowledge accuracy), and how video recording works.

**Sources**: `raw/21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf`, `raw/a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf`

**Last updated**: 2026-05-25

---

## Knowledge Assessment ACs

## AC-KA-01: Fact Check parameter

GIVEN a simulation has a knowledge base linked (via Paperflite stream)
WHEN the learner completes a simulation run
THEN the post-completion report includes a Fact Check parameter that lists all claims the learner made that contradict the knowledge base

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-02: Claim details in Fact Check

GIVEN the Fact Check parameter is shown
WHEN a contradicting claim is displayed
THEN each entry shows the claim text, the timestamp in the recording when it was made, and a rationale explaining why it contradicts the knowledge base

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-03: No score impact from Fact Check

GIVEN the Fact Check parameter identifies wrong claims
WHEN the simulation score is calculated
THEN the Fact Check findings do NOT affect the overall simulation score

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-04: Fact Check hidden when no wrong claims

GIVEN the learner made no claims contradicting the knowledge base
WHEN the post-completion report is displayed
THEN the Fact Check section is hidden (not shown as empty)

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-05: Paperflite stream as knowledge base

GIVEN a simulation creator wants to link a knowledge base
WHEN they configure the simulation
THEN they select a Paperflite stream to serve as the knowledge base for Fact Check

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

---

## Video in Simulations ACs

## AC-VS-01: Creator chooses video or audio mode

GIVEN a creator is setting up a simulation
WHEN they configure the simulation type
THEN they can choose between video mode (camera on) or audio-only mode

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-02: Learner grants camera permission

GIVEN a simulation is set to video mode
WHEN the learner begins the simulation
THEN the system requests camera permission from the learner before the simulation starts

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-03: Parallel video display during simulation

GIVEN a video-mode simulation is in progress
WHEN the learner is actively in the simulation
THEN they see the prospect's image (or video) and their own live video feed displayed in parallel on screen

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-04: Recording included in post-completion report

GIVEN the learner completes a video-mode simulation
WHEN the post-completion report is generated
THEN the report includes the session recording for review

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

## AC-VS-05: Manager can view recordings in reports

GIVEN a manager is reviewing a learner's simulation report
WHEN the report includes a video recording
THEN the manager can view the recording from within the report

(source: a5bf57bb-4b08-4874-bb07-a5d0b37cb20e_Video_in_Simulations.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[custom-scorecards]]
- [[podcast-simulation-in-courses]]
- [[simulation-reports]]
- [[simulation-call-recording]]
