# Feature: SMS Notifications

**Summary**: SMS Notifications is a planned feature under competitor research. The source document shows how Blackboard Ultra implements SMS notifications as an alternative to push notifications.

**Sources**: `13407f23-355c-4b46-829c-34cf362825de_SMS_Notifications.pdf`

**Last updated**: 2026-05-25

---

## What it does

Not yet formally specified for HeySales. The research document shows the Blackboard Ultra approach:

### Blackboard Ultra reference model
- Users who don't have the mobile app can receive text-based SMS messages for course activity
- Setup: User enters mobile phone number in profile settings, then enables SMS Notification Settings
- Users select which courses to receive notifications for and configure notification destinations (mobile, email, SMS, text-to-voice)

## Status

Competitor research. No HeySales-specific acceptance criteria or requirements have been written.

## Things to know

- The source PDF is a competitor reference document, not a HeySales product spec. (source: `13407f23-..._SMS_Notifications.pdf`)
- SMS Notifications for HeySales would likely complement existing [[push-notifications]] and [[due-date-notifications]] as a fallback channel for users without the app.

## Related pages

- [[push-notifications]]
- [[due-date-notifications]]
- [[notifications]]
