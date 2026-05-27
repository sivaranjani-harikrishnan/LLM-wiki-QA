# Acceptance Criteria: Call Classification

**Summary**: Defines how calls are classified by type before assessment, which call types are routed to the Call Library, and how the system is extensible per account.

**Sources**: `raw/c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf`

**Last updated**: 2026-05-25

---

## AC-CC-01: AI classification layer on incoming calls

GIVEN a call arrives via Fireflies or another integration
WHEN it enters the processing pipeline
THEN it is first passed through an AI classification layer that identifies the call type

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-02: Phase 1 — only discovery sales calls are assessed

GIVEN a call has been classified
WHEN the classification result is "discovery sales call"
THEN it is passed to assessment using the default MEDDIC Discovery Scorecard and routed to the Call Library

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-03: Phase 1 — all other call types excluded from Call Library

GIVEN a call has been classified as any type other than discovery sales call
WHEN the classification is applied
THEN the call is NOT routed to assessment or to the Call Library

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-04: Per-account call type configuration

GIVEN different accounts have different sales processes
WHEN the system is configured
THEN call types and their associated assessment frameworks are configured per account; the same classification rules are not applied globally

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-05: Extensible for future call types

GIVEN new call types may need to be supported in future
WHEN the engineering implementation is done
THEN the system is built in a way that new call types and their mapped assessment frameworks can be added without architectural changes

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-06: Call type shown as UI tag in Call Library

GIVEN a call has been classified and is visible in the Call Library
WHEN a user views the call entry
THEN the classified call type is shown as a UI tag attached to the call

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-07: Classification applies to simulation extraction uploads

GIVEN a call is uploaded for simulation extraction
WHEN it is processed
THEN the call classification process also runs on this call

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## AC-CC-08: Manual Call Library uploads — assessed regardless of type

GIVEN a call is manually uploaded to the Call Library
WHEN classification runs
THEN assessment proceeds with the default framework and the call is listed in the Call Library even if it is not classified as a discovery call

(source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

---

## Related pages
- [[overview]]
- [[real-call-scoring]]
- [[call-library]]
- [[custom-scorecards]]
