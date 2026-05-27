# Acceptance Criteria: Call Redaction

**Summary**: Defines when and how call redaction happens before LLM assessment, and what transcript is shown in reports.

**Sources**: `raw/bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf`

**Last updated**: 2026-05-25

---

## AC-CR-01: Redaction happens before LLM assessment

GIVEN a call transcript is ready for assessment
WHEN it is sent to the LLM for scoring
THEN the call redaction process must have completed first; the LLM only ever receives the redacted transcript

(source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)

## AC-CR-02: Original transcript shown in reports UI

GIVEN a call has been assessed
WHEN the evaluation report is shown in the UI
THEN the original (unredacted) transcript is displayed, not the redacted version

(source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)

## AC-CR-03: Redaction applies to integration-sourced calls

GIVEN a call arrives via Zoom, Fireflies, or Teams integration
WHEN real call scoring is triggered
THEN the redaction process runs on that call's transcript before assessment

(source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)

## AC-CR-04: Redaction applies to manually uploaded calls

GIVEN a user manually uploads a call recording to the Call Library
WHEN the transcript is processed for assessment
THEN the redaction process runs before the transcript is sent to the LLM

(source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)

## AC-CR-05: Redaction applies to simulation extraction uploads

GIVEN a call is uploaded for simulation extraction
WHEN the transcript is processed
THEN the redaction process runs before the transcript is used for simulation extraction

(source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)

---

## Related pages
- [[overview]]
- [[real-call-scoring]]
- [[call-library]]
- [[simulations]]
