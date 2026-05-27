# Acceptance Criteria: Real Call Scoring

**Summary**: Defines how real sales calls are captured, matched to CRM deals, scored, and recorded back to the CRM — covering Zoom, Fireflies, and Plaud integrations.

**Sources**: `raw/f0cece95-9ee6-4de3-92f3-08300902c90b_Real_call_scoring_.pdf`, `raw/4d017570-754d-4492-a8fa-7a46dc0ece03_Real_call_scoring_-_Zoom_x_Hubspot.pdf`, `raw/fe566fb8-cfa2-4b1a-bb78-2ea6a85a992d_Fireflies_-_Real_Call_Scoring.pdf`, `raw/410adf66-e65e-4744-8307-c29c4d0d106d_Plaud_-_Real_Call_Scoring.pdf`

**Last updated**: 2026-05-25

---

## General ACs

## AC-RCS-01: Rejection criteria

GIVEN a call recording is received by the system
WHEN the system checks eligibility for scoring
THEN calls are rejected (not scored) if they have: no transcript, no audio, or a duration of zero

(source: f0cece95-9ee6-4de3-92f3-08300902c90b_Real_call_scoring_.pdf)

## AC-RCS-02: Sales call identification logic

GIVEN a call is received
WHEN the system determines whether to score it
THEN it uses defined logic to identify whether the call is a sales call before processing it for scoring

(source: f0cece95-9ee6-4de3-92f3-08300902c90b_Real_call_scoring_.pdf)

---

## Zoom x HubSpot ACs

## AC-ZH-01: User-level Zoom toggle

GIVEN a rep wants to enable Zoom integration for real call scoring
WHEN they configure their integration settings
THEN the Zoom toggle is user-level (each rep enables it for themselves individually)

(source: 4d017570-754d-4492-a8fa-7a46dc0ece03_Real_call_scoring_-_Zoom_x_Hubspot.pdf)

## AC-ZH-02: Account-level HubSpot integration

GIVEN an organisation wants to use HubSpot for deal matching
WHEN the HubSpot integration is configured
THEN it is set at the account level (one configuration applies to all users in the organisation)

(source: 4d017570-754d-4492-a8fa-7a46dc0ece03_Real_call_scoring_-_Zoom_x_Hubspot.pdf)

## AC-ZH-03: Full technical flow

GIVEN a Zoom call ends for a user with the integration enabled
WHEN the system processes the call
THEN it follows this flow: webhook received → check user integration → fetch meeting details → match HubSpot contact and deal → retrieve transcript → run assessment → write notes back to CRM

(source: 4d017570-754d-4492-a8fa-7a46dc0ece03_Real_call_scoring_-_Zoom_x_Hubspot.pdf)

## AC-ZH-04: Email and domain fallback matching

GIVEN the system is trying to match a Zoom call participant to a HubSpot contact
WHEN a direct email match fails
THEN the system falls back to domain-based matching to find the relevant HubSpot deal

(source: 4d017570-754d-4492-a8fa-7a46dc0ece03_Real_call_scoring_-_Zoom_x_Hubspot.pdf)

## AC-ZH-05: Initial rollout filter

GIVEN the Zoom x HubSpot integration is being rolled out
WHEN determining which calls are processed during initial rollout
THEN only calls tagged as "Guided Walkthrough/Access" call type are processed

(source: 4d017570-754d-4492-a8fa-7a46dc0ece03_Real_call_scoring_-_Zoom_x_Hubspot.pdf)

---

## Fireflies Integration ACs

## AC-FF-01: Account-level Fireflies integration

GIVEN an organisation wants to use Fireflies for call capture
WHEN the Fireflies integration is configured
THEN it is set at the account level (not per user)

(source: fe566fb8-cfa2-4b1a-bb78-2ea6a85a992d_Fireflies_-_Real_Call_Scoring.pdf)

## AC-FF-02: All call types flow through Fireflies

GIVEN the Fireflies integration is enabled
WHEN any recorded call is processed
THEN all call types flow through Fireflies: app recordings, uploaded calls, and Zoom-integrated calls

(source: fe566fb8-cfa2-4b1a-bb78-2ea6a85a992d_Fireflies_-_Real_Call_Scoring.pdf)

## AC-FF-03: Fireflies takes priority over Zoom

GIVEN both Fireflies and Zoom integrations are enabled for an account
WHEN a call is processed for scoring
THEN Fireflies takes priority over the Zoom integration; calls are routed through Fireflies

(source: fe566fb8-cfa2-4b1a-bb78-2ea6a85a992d_Fireflies_-_Real_Call_Scoring.pdf)

---

## Plaud Integration ACs

## AC-PL-01: In-person recording via Plaud device

GIVEN a rep is conducting an in-person sales meeting
WHEN they want to capture and score the call
THEN they can use a Plaud physical recording device to record the conversation

(source: 410adf66-e65e-4744-8307-c29c4d0d106d_Plaud_-_Real_Call_Scoring.pdf)

## AC-PL-02: Rep selects CRM deal before recording

GIVEN a rep is about to start a Plaud recording
WHEN they initiate the recording
THEN they first select the relevant CRM deal to associate the recording with

(source: 410adf66-e65e-4744-8307-c29c4d0d106d_Plaud_-_Real_Call_Scoring.pdf)

## AC-PL-03: Full Plaud recording flow

GIVEN a rep has selected a CRM deal
WHEN they complete a Plaud recording
THEN the flow is: start recording → stop recording → processing → webhook → transcript and assessment generated → notes written back to CRM

(source: 410adf66-e65e-4744-8307-c29c4d0d106d_Plaud_-_Real_Call_Scoring.pdf)

## AC-PL-04: One-time device serial number linking

GIVEN a rep sets up their Plaud device
WHEN they link it to their HeySales account
THEN they enter the device serial number once; it is permanently linked to their account from that point

(source: 410adf66-e65e-4744-8307-c29c4d0d106d_Plaud_-_Real_Call_Scoring.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[call-library]]
- [[custom-scorecards]]
