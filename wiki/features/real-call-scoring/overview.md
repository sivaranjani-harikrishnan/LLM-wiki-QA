# Feature: Real Call Scoring

**Summary**: Real Call Scoring automatically assesses completed Zoom calls against a scorecard and pushes the report to the CRM when both Zoom and CRM (HubSpot or MS Dynamics) integrations are active.

**Sources**: `Real call scoring - Sheet1 (1).csv`, `MS Dynamics Real Call Scoring  - Sheet2.csv`

**Last updated**: 2026-05-25

---

## What it does

When a HeySales user completes a Zoom call with a prospect who has an active deal in the CRM, the system:
1. Records the call (if call recording toggle is on)
2. Generates a scored call report using the account's default scorecard
3. Pushes the report to the CRM (as a note or activity)

## Who uses it

- **Sales reps (any user)**: Connect Zoom in their personal integration settings; their real calls are scored
- **Admins**: May view call reports in the Call Library

## HubSpot integration (User-level)

### Setup
- Settings → Integrations → Zoom card (only visible when HeySales is enabled)
- Each user connects their own Zoom account independently (USER-level, not account-level)
- Call recording access toggle: ON/OFF per user

### Trigger conditions (all must be true)
1. Zoom is integrated
2. HubSpot is integrated
3. Call recording toggle is ON
4. Invitee is a contact in HubSpot
5. Invitee has an active (open) deal in HubSpot

### When scoring is NOT triggered
- Either integration not connected
- Call recording toggle is OFF
- Invitee has no deal in HubSpot
- Invitee's deal is closed (not active)
- Either integration is expired
- Call is the user's own (no external invitees with deals)

### Multi-invitee behaviour
- Multiple invitees in one Zoom meeting: report pushed only to those invitees with an active deal
- Multiple contacts associated with one deal: report pushed to all contacts who participated in the meeting
- One contact associated with multiple deals: one report pushed (to the contact)
- Contact removed from deal after a call: future calls do not push report (call history unaffected)
- Reopened closed deal: scoring resumes

### Report contents
- Overall score
- Parameter Breakdown
- Sales rep positives
- Prospect observation
- Suggestions

### Call frequency
- Every call generates a separate new note (multiple calls = multiple separate reports)

### Expired integration
- When integration expires, call scoring stops until reauthorised

### Call duration
- Calls under 2 minutes still generate a report (source: `Real call scoring - Sheet1 (1).csv` TC0018)

---

## MS Dynamics integration (Account-level)

### Key differences from HubSpot

| Aspect | HubSpot | MS Dynamics |
|---|---|---|
| Zoom integration level | USER-level | ACCOUNT-level (one for whole account) |
| CRM object | Deal + Contact | Opportunity |
| Report destination | Note on contact | Activity + Timeline on opportunity |
| Multi-contact per opportunity | Report per meeting participant | One report per opportunity |
| Expired token | User must reauthorise | Zoom access token auto-refreshes after 1 hour; expired OAuth needs full reauth |

### Both CRMs integrated simultaneously
- When both HubSpot and MS Dynamics are integrated, the call report is pushed to BOTH CRMs

### Deactivation / reactivation
- Deactivating the account-level integration stops scoring
- Reactivating resumes scoring for future calls

## Call Library

Call records from real call scoring are visible in the Call Library in HeySales Studio. See [[call-library]].

## Default scorecard used

Real call scoring always uses the **account's current default scorecard** at the time of the call. (source: `Real call scoring - Sheet1 (1).csv` TC0015)

## Fireflies integration priority

When both Fireflies and Zoom are integrated, Fireflies takes priority for real call scoring. (source: product ACs)

## Related pages

- [[test-coverage]]
- [[call-library]]
- [[custom-scorecards]]
- [[heysales-overview]]
