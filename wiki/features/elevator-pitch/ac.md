# Acceptance Criteria: Elevator Pitch

**Summary**: No formal acceptance criteria were found in the available source documents. The source PDFs are research and design references only.

**Sources**: `raw/4035463b-497d-4455-aa61-7d76ab9424f2_Elevator_Pitch.pdf`, `raw/1659a9bf-dd66-4e7c-8e4f-3e19375ce573_Elevator_Pitch_-_Assessment_Framework.pdf`

**Last updated**: 2026-05-25

---

## Note on core Elevator Pitch ACs

Neither core source PDF contains formal acceptance criteria.

- `4035463b_Elevator_Pitch.pdf` — References a YouTube video; contains no ACs
- `1659a9bf_Elevator_Pitch_-_Assessment_Framework.pdf` — Contains a scoring rubric research reference only; no formal product ACs

---

## Framework Defect Fix ACs

## AC-EPF-01: Scorecard filtering by call type during simulation setup

GIVEN a creator is setting up a simulation and selecting an assessment framework
WHEN they view the available scorecards
THEN only scorecards that are marked with a call type matching the simulation's call type are shown; untagged scorecards do not appear

(source: 46cdefcb-eec2-46b6-b59b-08d920037e5f_Elevator_Pitch_-_Framework_Defect.pdf)

## AC-EPF-02: Filtering rules do not apply to Elevator Pitch

GIVEN a creator is setting up an Elevator Pitch simulation
WHEN they view the available scorecards
THEN the call-type filtering rules described in AC-EPF-01 do NOT apply; elevator pitch uses its own rule

(source: 46cdefcb-eec2-46b6-b59b-08d920037e5f_Elevator_Pitch_-_Framework_Defect.pdf)

## AC-EPF-03: Scorecards marked "all" appear for all standard call types

GIVEN a scorecard is marked as applicable to "all" call types
WHEN a creator sets up any standard simulation (discovery, cold call, etc.)
THEN that scorecard appears in the framework options for all such call types

(source: 46cdefcb-eec2-46b6-b59b-08d920037e5f_Elevator_Pitch_-_Framework_Defect.pdf)

## AC-EPF-04: Default scorecard is automatically "all"

GIVEN a scorecard is marked as the default
WHEN call type filtering is applied
THEN the default scorecard is automatically treated as "all" and appears as the default for every call type

(source: 46cdefcb-eec2-46b6-b59b-08d920037e5f_Elevator_Pitch_-_Framework_Defect.pdf)

## AC-EPF-05: Elevator Pitch only shows explicitly labelled frameworks

GIVEN a creator is setting up an Elevator Pitch simulation
WHEN they select an assessment framework
THEN only scorecards explicitly labelled as "elevator pitch" are shown; all others are hidden

(source: 46cdefcb-eec2-46b6-b59b-08d920037e5f_Elevator_Pitch_-_Framework_Defect.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[custom-scorecards]]
- [[simulations]]
