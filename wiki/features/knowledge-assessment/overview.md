# Feature: Knowledge Assessment

**Summary**: Evaluates whether a rep's claims during a simulation contradict the product knowledge base (Paperflite stream), surfacing factual errors without affecting the simulation score.

**Sources**: `raw/21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf`, `raw/e1de3de8-d101-45f5-afed-3f4e70fb89e3_Knowledge_Assessment_-_Call_Simulation.pdf`

**Last updated**: 2026-05-25

---

## What it does
Knowledge Assessment adds a Fact Check layer to simulation reports. It checks whether anything the learner said during the simulation contradicts the linked Paperflite knowledge base, then surfaces those contradictions in the report with the claim, its timestamp, and an explanation.

## Who uses it
Learners reviewing their own simulation reports, and managers reviewing rep performance to identify knowledge gaps.

## How it works
1. The simulation creator links a Paperflite stream as the knowledge base when setting up the simulation.
2. After the learner completes the simulation run and the report is generated, the system checks all of the learner's claims against the knowledge base.
3. Any claims that contradict the knowledge base appear in a "Fact Check" section of the report.
4. Each entry shows: the claim, the timestamp of when it was said, and a rationale explaining the contradiction.
5. If no contradicting claims were made, the Fact Check section is hidden entirely.

## Things to know
- Fact Check findings do NOT affect the simulation score — they are informational only. (source: 21e566c7-09c2-49a5-805f-8dfa58ead1dd_Knowledge_Assessment_-_Simulation.pdf)
- The `e1de3de8` source (Knowledge Assessment - Call Simulation) references Yoodli as a research reference only and contains no HeySales-specific ACs. (source: e1de3de8-d101-45f5-afed-3f4e70fb89e3_Knowledge_Assessment_-_Call_Simulation.pdf)

## Related pages
- [[ac]]
- [[simulations]]
- [[simulation-reports]]
