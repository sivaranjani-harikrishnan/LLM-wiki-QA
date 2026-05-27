# Acceptance Criteria: Knowledge Assessment

**Summary**: Defines how the Fact Check parameter works in simulation reports, including what triggers it, what it shows, and its impact on scoring.

**Sources**: `raw/21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf`

**Last updated**: 2026-05-25

---

## AC-KA-01: Fact Check parameter in post-completion report

GIVEN a simulation has a knowledge base linked (Paperflite stream)
WHEN the learner completes a simulation run and the report is generated
THEN the report includes a Fact Check parameter listing claims the learner made that contradict the knowledge base

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-02: Claim details

GIVEN the Fact Check section is shown
WHEN a contradicting claim is listed
THEN each entry displays: the claim text, the timestamp of when it occurred in the recording, and a rationale explaining why it contradicts the knowledge base

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-03: No score impact

GIVEN the Fact Check parameter identifies wrong claims
WHEN the overall simulation score is calculated
THEN the Fact Check findings do NOT affect the simulation score

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-04: Fact Check hidden when no contradictions

GIVEN the learner made no claims that contradicted the knowledge base
WHEN the simulation report is shown
THEN the Fact Check section is hidden entirely (not shown as empty)

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

## AC-KA-05: Paperflite stream as knowledge base

GIVEN a simulation creator wants to enable Fact Check
WHEN they configure the simulation
THEN they select a Paperflite stream as the knowledge base for that simulation

(source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)

---

## Note on source documents

`raw/e1de3de8-d101-45f5-afed-3f4e70fb89e3_Knowledge_Assessment_-_Call_Simulation.pdf` is a research reference (Yoodli) and contains no HeySales-specific acceptance criteria.

---

## Related pages
- [[overview]]
- [[simulations]]
- [[simulation-reports]]
