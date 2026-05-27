# Test Coverage: Real Call Scoring

**Summary**: 20 HubSpot TCs and 26 MS Dynamics TCs covering integration setup, trigger conditions, multi-invitee scenarios, and expired integration behaviour.

**Sources**: `Real call scoring - Sheet1 (1).csv`, `MS Dynamics Real Call Scoring  - Sheet2.csv`

**Last updated**: 2026-05-25

---

## HubSpot TCs (TC0001–TC0020)

### TC0001: Zoom integration card in settings (HeySales enabled)
**What this tests**: Validate For accounts with heysales enabled, in settings integration Zoom card should be displayed

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0002: Zoom integration card in settings (HeySales disabled)
**What this tests**: Validate For accounts with heysales disabled, in settings integration Zoom card should not be displayed

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0003: Zoom integrations permission (USER-level)
**What this tests**: Validate The Zoom integration should be User level not account level — User A integrating Zoom does not affect User B's integration state

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0004: Call recording access toggle
**What this tests**: Validate User should be able to toggle on or off the Call recording toggle in the integration

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0005: Real call scoring when Zoom integrated but HubSpot not
**What this tests**: Validate If either of the integration is not integrated, Call scoring should not be triggered

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0006: Real call scoring when HubSpot integrated but Zoom not
**What this tests**: Validate If either of the integration is not integrated, Call scoring should not be triggered

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0007: Real call scoring when toggle is OFF despite both integrations
**What this tests**: Validate If the call recording access is toggled off, Call scoring should not be triggered

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0008: Invitee has no deal in HubSpot
**What this tests**: Validate If the invitee does not have a deal mapped in hubspot, Call scoring should not be triggered

**Precondition**: Invitee should be a contact in HubSpot but not mapped to any deal

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0009: Invitee has closed deal
**What this tests**: Validate If the deal is not active [closed deal], Call scoring should not be triggered

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0010: Invitee has active deal
**What this tests**: Validate If the deal is active [open deal] and call recording access is toggled on, Call scoring should be triggered. The call report should be pushed as a note to the contact in hubspot

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0011: Multiple invitees in one Zoom meeting
**What this tests**: Validate When there are multiple invitees in a zoom meeting, call report should be pushed only to the invitees with an active deal in hubspot

**Steps**: Map Deal A to contact 1, Deal B to contact 2, Deal C to contact 3; invite contacts 1–5; only 1, 2, and 3 get reports

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0012: Contact removed from deal (after a previous scored call)
**What this tests**: Validate when a contact is removed from the deal, call report should not be pushed after the zoom meeting

**Steps**: Map deal → call → verify report pushed → remove contact from deal → another call → verify no report pushed

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0013: Multiple contacts per one deal — report only to meeting participants
**What this tests**: Validate When multiple contacts are associated in one deal, after the zoom meeting the call report should be sent to only the participants of the zoom meeting

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0014: One contact with multiple deals
**What this tests**: Validate When multiple deals are associated with one contact, after the zoom meeting the call report should be sent to the contact

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0015: Default scorecard used for real call scoring
**What this tests**: Validate After the zoom meeting the reports should be generated based on the accounts default scorecard

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0016: Fields in the call scoring report
**What this tests**: Validate In the call report the Overall score, Parameter Breakdown, Sales rep positive, Prospect observation, and Suggestions should be listed

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0017: Expired integration stops scoring
**What this tests**: Validate When either of the integration is expired [Zoom / HubSpot] the call report should not be pushed

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0018: Call under 2 minutes still generates report
**What this tests**: Validate If the call is less [than] 2 mins the report should be generated

**Priority**: Medium | **Note**: This is notable — simulation calls under 2 min are marked NA, but real call scoring still generates a report

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0019: Reopened closed deal resumes scoring
**What this tests**: Validate When the closed deal is reopened, after the zoom meeting the call report should be sent to the contact

(source: `Real call scoring - Sheet1 (1).csv`)

---

### TC0020: Multiple calls = multiple separate reports
**What this tests**: Validate for every call a new report should be pushed as notes to the contact

(source: `Real call scoring - Sheet1 (1).csv`)

---

## MS Dynamics TCs (TC0001–TC0026)

Key scenarios tested:
- TC0001–TC0003: Account-level Zoom integration setup and visibility
- TC0004–TC0006: Scoring trigger conditions (both integrations required, opportunity-based)
- TC0007–TC0009: Call recording toggle behaviour at account level
- TC0010–TC0012: Active vs closed opportunity behaviour
- TC0013–TC0015: Multiple contacts per opportunity → one report to opportunity (not per contact who attended)
- TC0016–TC0018: Zoom access token auto-refresh after 1 hour; expired OAuth requires full reauth
- TC0019–TC0021: Deactivation stops scoring; reactivation resumes
- TC0022–TC0024: Both HubSpot and MS Dynamics integrated → reports pushed to BOTH CRMs
- TC0025–TC0026: UI elements for account-level integration and reauthentication flow

(source: `MS Dynamics Real Call Scoring  - Sheet2.csv`)

---

## Related pages

- [[overview]]
- [[call-library]]
- [[custom-scorecards]]
