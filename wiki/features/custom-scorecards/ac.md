# Acceptance Criteria: Custom Scorecards

**Summary**: Defines how scorecards are created, mapped to call types, and used to evaluate simulations and real calls.

**Sources**: `raw/9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf`

**Last updated**: 2026-05-25

---

## AC-01: Scorecards tab visibility

GIVEN a user is in the platform settings or admin area
WHEN they navigate to the Scorecards section
THEN a dedicated Scorecards tab is displayed listing all scorecards

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-02: Default scorecard always exists

GIVEN the platform is set up
WHEN a user views the scorecard list
THEN at least one scorecard always exists (the default) and cannot be deleted

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-03: Create a new scorecard

GIVEN a user has scorecard management permissions
WHEN they choose to create a scorecard
THEN they can define a new scorecard with a name and set of parameters

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-04: Clone an existing scorecard

GIVEN a user has scorecard management permissions
WHEN they clone an existing scorecard
THEN a copy of that scorecard is created with all its parameters, which they can then edit independently

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-05: Map scorecard to call types

GIVEN a scorecard exists
WHEN a user maps it to one or more call types
THEN that scorecard is used when scoring calls of those types

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-06: Mark scorecard as default

GIVEN multiple scorecards exist
WHEN a user marks a scorecard as the default
THEN it is applied to any call type that does not have a more specific scorecard mapped to it

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-07: Specificity-based default logic

GIVEN a call type has both a specific scorecard mapped and the default scorecard
WHEN a call of that type is scored
THEN the most specific scorecard (the one directly mapped to that call type) takes precedence over the default

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-08: Generate scoring criteria with Seek button

GIVEN a user is editing a scorecard parameter
WHEN they click the "Seek" button
THEN the system generates AI-suggested scoring criteria for that parameter on a 1–5 scale

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-09: Parameters and sub-parameters

GIVEN a user is creating or editing a scorecard
WHEN they define the scorecard structure
THEN they can add top-level parameters and nest sub-parameters beneath them

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

## AC-10: Scoring scale

GIVEN a scorecard parameter is evaluated
WHEN a score is assigned to that parameter
THEN the score is on a 1–5 scale as defined by the scoring criteria

(source: 9b4406b6-010f-483b-8783-eefa6ea2fa86_Custom_Scorecards_.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[simulations]]
- [[real-call-scoring]]
