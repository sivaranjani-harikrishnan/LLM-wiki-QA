# Feature: Call Classification

**Summary**: An AI layer that classifies incoming calls by type (discovery, pricing, internal, etc.) so that only relevant sales calls are assessed and routed to the Call Library, with appropriate scorecards applied per call type.

**Sources**: `raw/c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf`

**Last updated**: 2026-05-25

---

## What it does
Call Classification runs an AI classification step on every incoming call (from Fireflies/Zoom/Teams integrations and manual uploads) to determine what type of call it is. In Phase 1, only calls classified as "discovery sales call" are passed for assessment and into the Call Library. Internal calls, support calls, and other non-sales calls are filtered out.

## Who uses it
This is a system-level feature. It runs automatically for all accounts that have Fireflies or other integrations enabled. Admins can configure which call types are assessed per account.

## How it works
1. A call arrives via Fireflies or other integration.
2. The AI classification layer analyses the call and assigns a call type tag.
3. In Phase 1: only calls tagged "discovery sales call" are passed to assessment with the MEDDIC Discovery Scorecard; all other types are not routed to the Call Library.
4. The classified call type is shown as a UI tag on the call in the Call Library.
5. For manually uploaded calls: classification still runs, but assessment proceeds with the default framework and the call is listed in the Call Library regardless of type.

## Things to know
- Call types are configurable per account — different accounts can have different call type rules. (source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)
- The system is designed to be extensible: new call types and their mapped assessment frameworks can be added in future. (source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)
- Classification also runs for calls uploaded for simulation extraction. (source: c0401f79-2c33-4e68-8845-ecdf1a8e6da8_Call_Classification.pdf)

## Related pages
- [[ac]]
- [[real-call-scoring]]
- [[call-library]]
- [[custom-scorecards]]
