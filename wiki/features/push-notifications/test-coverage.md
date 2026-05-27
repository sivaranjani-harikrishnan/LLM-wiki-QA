# Test Coverage: Push Notifications

**Summary**: 12 test cases covering browser permission prompts, notification delivery, deeplink behaviour, offline handling, and device settings.

**Sources**: `Push notifications - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## TC0001: First-login permission prompt (iOS/Android)
**What this tests**: Validate that browser permission prompt is shown to user on first login on iOS/Android

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0002: Allow notifications
**What this tests**: User allows notification permission → notifications enabled and delivered

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0003: Deny notifications
**What this tests**: User denies notification permission → prompt not shown again; notifications not delivered

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0004: Prompt not repeated on subsequent logins
**What this tests**: Validate that permission prompt is not shown again after first login decision

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0005: Notification for learning assignment
**What this tests**: Validate notification has correct title + message when learning is assigned; deeplinks to learning preview page in My Space

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0006: Deeplink — user logged in
**What this tests**: Validate clicking notification opens app directly to learning preview page in My Space

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0007: Deeplink — user logged out
**What this tests**: Validate clicking notification opens app to login page; after login, redirects to learning preview

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0008: Logged-out users do not receive notifications
**What this tests**: Validate logged-out users do not receive push notifications

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0009: Device-level settings — disable
**What this tests**: Validate disabling notifications via device settings stops delivery

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0010: Device-level settings — enable
**What this tests**: Validate re-enabling notifications via device settings resumes delivery

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0011: Offline behaviour
**What this tests**: Validate notification is delivered when device reconnects after being offline

(source: `Push notifications - Sheet1 (1).csv`)

---

## TC0012: Deeplink to deleted learning
**What this tests**: Validate tapping notification for a deleted learning shows "no content" error

(source: `Push notifications - Sheet1 (1).csv`)

---

## Related pages

- [[overview]]
- [[due-date-notifications]]
- [[mobile-deeplinking]]
