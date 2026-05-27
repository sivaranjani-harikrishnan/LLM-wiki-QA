# Audience Guide: Support

**Summary**: How support agents should use this wiki to diagnose issues, understand expected product behaviour, and answer customer questions about HeySales.

**Last updated**: 2026-05-25

---

## Quick reference: common support scenarios

### "I don't see the Scorecard option in Settings"
- Is HeySales enabled on the account? If not, the Scorecard option does not appear for any user
- Is the user an Admin or Content Publisher? Normal users and BI Analysts do not see Scorecard in Settings
- See: [[custom-scorecards/overview]]

### "My real call scoring is not working"
Check all of:
1. Is Zoom integrated? (Settings → Integrations → Zoom card visible only when HeySales enabled)
2. Is the CRM (HubSpot or MS Dynamics) integrated?
3. Is the call recording toggle ON?
4. Does the Zoom meeting invitee have an **active** (open) deal in the CRM? Closed deals do not trigger scoring
5. Is the integration expired? (expired = no scoring)
6. HubSpot: is the user's Zoom connected (USER-level, not account-level)?
7. MS Dynamics: is the ACCOUNT-level Zoom connected?
See: [[real-call-scoring/overview]]

### "My scorecard was deleted — what happened to my simulations?"
Deleting a scorecard does NOT affect simulations that were already using it. Reports remain intact. The system reverts to the Paperflite default scorecard for future simulations.
See: [[custom-scorecards/overview]]

### "Learner says they can't end the course"
The learner must view all lessons AND complete all assessments — including those inside and outside sections. Check if there are any incomplete elements.
See: [[courses/overview]], [[sections-in-courses/overview]]

### "Podcast edits are not showing for learner"
Edits to standalone podcasts propagate to learners automatically. BUT: if the podcast was added to a course via Pick from Studio, edits to the podcast in Studio do NOT reflect in the course.
See: [[podcasts/overview]], [[podcast-simulation-in-courses/overview]]

### "Section is not showing in mobile app"
Sections are not displayed in the mobile HeySales app. This is expected behaviour. Sections are visible on web and in Demo URLs.
See: [[sections-in-courses/overview]]

### "Learner's Microlearning article is not showing for the admin"
Microlearning (Let's Learn) articles and podcasts are strictly private per user. No admin, manager, or other user can see them. This is by design.
See: [[microlearning/overview]]

### "The call under 2 minutes didn't generate a simulation report"
Correct — simulation calls under 2 minutes are marked as NA (not scored). However, real call scoring (via Zoom + CRM) DOES generate a report even for calls under 2 minutes.
See: [[simulation-reports/overview]], [[real-call-scoring/overview]]

### "Reminders are not being sent to a deactivated user"
Deactivated users are automatically excluded from all reminder emails. This is expected.
See: [[due-date-notifications/overview]]

### "Both HubSpot and MS Dynamics are connected — which CRM gets the call report?"
Both. When both integrations are active simultaneously, the call report is pushed to both CRMs.
See: [[real-call-scoring/overview]]

### "Fireflies is connected — which integration takes priority?"
When Fireflies and Zoom are both integrated, Fireflies takes priority for real call scoring.
See: [[real-call-scoring/overview]]

## Related pages

- [[for-testing]]
- [[for-engineering]]
- [[heysales-overview]]
