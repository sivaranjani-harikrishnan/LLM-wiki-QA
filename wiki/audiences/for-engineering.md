# Audience Guide: Engineering

**Summary**: Key system behaviours, edge cases, integration architecture, and data flows that engineers working on HeySales need to understand.

**Last updated**: 2026-05-25

---

## Integration architecture

### HubSpot (USER-level Zoom)
- Each user connects their own Zoom account independently
- Scoring trigger: Zoom integrated + HubSpot integrated + recording toggle ON + invitee has active deal
- Report destination: Note on the HubSpot contact
- Multi-invitee: report per invitee with active deal
- See: [[real-call-scoring/overview]]

### MS Dynamics (ACCOUNT-level Zoom)
- One Zoom integration for the entire account
- Scoring trigger: same conditions as HubSpot but opportunity-based
- Report destination: Activity + Timeline on the opportunity
- Multi-contact per opportunity: ONE report per opportunity (not per participant)
- Zoom access token auto-refreshes after 1 hour (expired OAuth = full reauth)
- See: [[real-call-scoring/overview]]

### Both CRMs simultaneously
- Reports pushed to BOTH when both integrations active
- Fireflies + Zoom: Fireflies takes priority

## Calculation formulas

### Simulation metrics
- Avg score = sum of all attempts' scores / total attempts count (includes retakes)
- Avg time spent = cumulative time per learner / completed learner count (does NOT add retake time separately)
- Team avg = sum of best scores / completed learner count
- Ranking = based on best score (dynamic)

### Course metrics
- Avg score = total score across all attempts (including retakes) / total attempts
- Avg time spent = per-learner cumulative time / learner count (retakes add cumulatively per learner)
- Pass % = passed learners / completed learners (threshold changes not retroactive)

### Podcast metrics
- Avg listen time = total listen time / (started + completed learners); not-started excluded
- Replay does NOT change any metric

## Data isolation rules

- Profile extraction calls are account-scoped (Account A calls not visible in Account B)
- Microlearning articles and podcasts are user-scoped (strictly private per user)
- Call records in Call Library are account-scoped

## Key state machines

### Scorecard
- Draft → Published (Active)
- Cannot delete default scorecard (Paperflite MEDDIC)
- Deleting a non-default scorecard: existing simulation reports unaffected; system reverts to Paperflite scorecard as new default if deleted scorecard was default

### Simulation scoring
- Call <2 min → NA (not scored)
- Call ≥2 min → AI generates report using tagged scorecard
- Real call scoring via Zoom: calls <2 min STILL generate a report (different from simulation logic)

### Podcast generation
- Generation continues in background when user navigates away
- Failed asset → error state (shows per-asset retry + upload new)
- Max 5 assets enforced at creation AND edit time

### Course sections
- Empty section (no content or all content removed) → blocks publish
- Adding any content back removes empty error
- Section deletion with content → confirmation required; deletes nested content

## learningModalities array (Microlearning)
The Microlearning feature uses a `learningModalities` array where the article and the private podcast are stored as separate entries within the same document. Deleting the article removes all modality entries.

## Due date reminder schedule
The system calculates reminders based on gap between assignment date and due date:
- Always: 50% of gap
- If gap >30 days: 7-day reminder
- If gap >10 days: 3-day reminder
- Always: 1-day reminder
- No-clash: if 50% and 1-day land on same day → send only 1 email
- Stop on completion; skip deactivated users

## Mobile deeplink flow
1. Notification mailer contains "Get Started" deeplink
2. iOS → App Store (if not installed) or HeySales iOS app
3. Android → Play Store (if not installed) or HeySales Android app
4. If session invalid → redirect to login; after login → redirect to learning preview page

## Related pages

- [[for-testing]]
- [[real-call-scoring/overview]]
- [[custom-scorecards/overview]]
- [[microlearning/overview]]
