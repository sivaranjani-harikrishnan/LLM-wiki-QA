# Feature: Push Notifications

**Summary**: HeySales sends browser push notifications to learners when they are assigned new content; notifications deeplink directly to the learning preview page in the mobile app.

**Sources**: `Push notifications - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## What it does

When a learner is assigned a new learning, the system sends a push notification (on mobile: iOS/Android) prompting them to start. Tapping the notification opens the HeySales app and navigates directly to the learning.

## Who uses it

- **Learners**: Receive push notifications for new assignments
- **Admins**: Do not receive push notifications for assignments

## How it works

### Browser permission prompt
- First login on a device triggers a permission prompt asking the user to allow/deny notifications
- If allowed: notifications are enabled
- If denied: no prompt shown again on subsequent logins; notifications are not sent
- Prompt is not repeated after the first login decision

### Notification content
- Correct title (the learning's name)
- Correct message body
- Deeplink to the learning preview page in My Space

### Deeplink behaviour
| Scenario | Behaviour |
|---|---|
| User logged in | App opens directly to the learning preview page in My Space |
| User logged out | App opens to login page; after login, redirects to learning preview |
| App not installed | Redirects to App Store (iOS) or Play Store (Android) |
| Invalid/expired session | App opens login page; after login, redirects to learning preview |
| User has no access to the learning | "No content" error message shown |
| Learning deleted after notification sent | "No content" error shown on tap |

### Logged-out users
Logged-out users do NOT receive push notifications. Notifications are only delivered to currently logged-in users.

### Offline behaviour
If the user is offline when the notification is sent, it is delivered when the device reconnects to the internet.

### Device-level settings
- Users can disable/enable notifications via device settings (iOS/Android)
- Disabling in device settings stops notifications; re-enabling resumes them

### Cross-platform
- iOS notification tap → App Store (if app not installed) or app (if installed)
- Android notification tap → Play Store (if app not installed) or app (if installed)

## Related pages

- [[test-coverage]]
- [[due-date-notifications]]
- [[mobile-deeplinking]]
