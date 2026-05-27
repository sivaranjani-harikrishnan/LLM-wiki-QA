# Feature: CRM Integration

**Summary**: Integrates HeySales with CRM platforms (initially HubSpot, with Sandler shown as a reference context) to surface deal intelligence alongside learning content, and to automate CRM field entries based on real call data.

**Sources**: `raw/0d05522f-3723-49a7-a227-93befffb116d_CRM_Integration_.pdf`, `raw/56f62fd9-8b7f-4e48-bfea-a20866f4e961_CRM_Entry_Automation.pdf`

**Last updated**: 2026-05-25

---

## What it does
CRM Integration connects HeySales to a rep's CRM so that deal context (challenges, suggestions, activities) can be surfaced alongside learning content. The CRM Entry Automation extension automatically populates CRM fields based on what happened during a rep's real calls.

## Who uses it
Sales reps (who have CRM-connected accounts) and managers reviewing deal progress alongside rep coaching data.

## How it works

### CRM Integration
The source document shows a screenshot of a CRM record (Sandler / HubSpot context) with deal challenges, suggestions, activities, contacts, leads, and playbooks visible alongside a HeySales course card. The intent is to surface relevant learning content in context with live deal data.

### CRM Entry Automation
After a real call, the system automatically populates CRM field entries based on what the rep said and did during the call. This removes the manual data entry burden from reps and ensures CRM records reflect actual call outcomes.

## Things to know
- The CRM Integration source document (`0d05522f`) is a single-page screenshot of a Sandler/HubSpot interface with no formal acceptance criteria. (source: 0d05522f-3723-49a7-a227-93befffb116d_CRM_Integration_.pdf)
- The CRM Entry Automation source document (`56f62fd9`) contains a one-sentence intent statement only. Formal ACs have not yet been defined for either feature. (source: 56f62fd9-8b7f-4e48-bfea-a20866f4e961_CRM_Entry_Automation.pdf)
- Real-call-scoring already includes a HubSpot integration step that matches calls to HubSpot deals and writes assessment notes back to the CRM — see [[real-call-scoring]] for the specified behaviour. (source: unverified)

## Related pages
- [[ac]]
- [[real-call-scoring]]
- [[call-library]]
