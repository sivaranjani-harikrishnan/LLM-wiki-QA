# Acceptance Criteria: Push Notifications

**Summary**: No formal AC document exists for push notifications. Acceptance criteria below are inferred from test cases. See [[test-coverage]] for the full test case list.

**Sources**: `raw/Push notifications - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## AC-PN-01: Permission prompt shown on first session

GIVEN a user logs in to the HeySales app for the first time
WHEN the app launches
THEN a permission prompt asks whether the user would like to allow push notifications from the app

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-02: Allowing notifications registers the device

GIVEN the permission prompt is shown
WHEN the user taps "Allow"
THEN the app registers successfully for push notifications and the user begins receiving notifications when triggered

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-03: Denying notifications suppresses all push notifications

GIVEN the permission prompt is shown
WHEN the user taps "Deny"
THEN the app does not receive any push notifications and no background notifications appear

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-04: Permission prompt not shown on subsequent sessions

GIVEN a user has previously responded to the permission prompt (allowed or denied)
WHEN they log in again
THEN the permission prompt is not shown again; notification behaviour follows their prior selection

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-05: Push notification sent on learning assignment

GIVEN a learning assignment is triggered for a user
WHEN the event fires
THEN a push notification appears on the user's device with the correct title and message format as configured

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-06: Push notification deeplinks to the learning

GIVEN a push notification is tapped
WHEN the app opens
THEN the user is navigated directly to the respective Learning Preview page

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-07: Logged-out users do not receive push notifications

GIVEN a user is logged out of the app
WHEN a notification would normally be triggered
THEN the notification is not sent

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-08: Notifications disabled in system settings suppresses delivery

GIVEN a user has disabled notifications for the app in their device system settings
WHEN a notification would normally be triggered
THEN no notification appears on the device

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-09: Re-enabling notifications from system settings restores delivery

GIVEN a user re-enables notifications for the app in their device system settings
WHEN a notification would normally be triggered
THEN push notifications are received correctly

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-10: Push notifications work correctly on iOS and Android

GIVEN a push notification is triggered
WHEN it is delivered to either iOS or Android
THEN notifications are delivered and displayed correctly on both platforms

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-11: Device offline — notification not delivered

GIVEN a user's device is offline
WHEN a notification would normally be triggered
THEN the notification does not appear on the device

(source: Push notifications - Sheet1 (1).csv)

## AC-PN-12: Deeplink to deleted learning shows no-content error

GIVEN a push notification deeplinks to a learning that has since been deleted
WHEN the user taps the notification
THEN a no-content error message is displayed

(source: Push notifications - Sheet1 (1).csv)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[mobile-deeplinking]]
- [[due-date-notifications]]
