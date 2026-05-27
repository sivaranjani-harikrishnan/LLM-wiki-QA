# Feature: Mobile Deeplinking

**Summary**: Notification mailer links deeplink into the HeySales mobile app (iOS/Android), navigating users directly to the assigned learning; unauthenticated users are redirected to the login page first.

**Sources**: `Deeplinking for mobile application - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

When a learner receives a learning assignment notification email (mailer), clicking the "Get Started" button uses a deeplink to open the HeySales mobile app directly at the learning's preview page.

## Who uses it

- **Learners**: Receive notification emails with deeplink; click to launch app

## How it works

### Scenarios

| User state | App installed | Behaviour |
|---|---|---|
| Logged in | Yes | App opens directly to learning preview page in My Space |
| Logged out | Yes | App opens to login page; after login, redirects to learning preview |
| Invalid/expired session | Yes | App opens to login page; after login, redirects to learning preview |
| App not installed | N/A | Redirects to App Store (iOS) or Play Store (Android) |
| Logged in as wrong user (no access) | Yes | App opens; "No content" error message shown |

### Cross-platform
- iOS deeplink → App Store (if not installed) or HeySales iOS app (if installed)
- Android deeplink → Play Store (if not installed) or HeySales Android app (if installed)

### Mailer contents
- Learning details in the email body
- "Get Started" CTA button containing the deeplink

### After login (from deeplink)
- Successful login redirects the user to the specific learning's preview page in My Space

## Things to know

- Deeplinking is part of the "notification mailer" flow — triggered when a learner is assigned a learning (source: `Deeplinking for mobile application - Sheet1.csv`)
- Wrong user scenario: if user A's email links to a learning they don't have access to, a "No content" error is shown (source: TC0005)

## Related pages

- [[test-coverage]]
- [[push-notifications]]
- [[due-date-notifications]]
