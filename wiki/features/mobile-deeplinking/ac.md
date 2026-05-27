# Acceptance Criteria: Mobile Deeplinking

**Summary**: No formal AC document exists for mobile deeplinking. Acceptance criteria below are inferred from test cases. See [[test-coverage]] for the full test case list.

**Sources**: `raw/Deeplinking for mobile application - Sheet1.csv`

**Last updated**: 2026-05-25

---

## AC-DL-01: Deeplink navigates logged-in user to learning

GIVEN a user has the mobile app installed and is already logged in
WHEN they click the "Get started" deeplink in a notification mailer
THEN they are navigated directly to the learning in the app

(source: Deeplinking for mobile application - Sheet1.csv)

## AC-DL-02: Deeplink navigates logged-out user to login page

GIVEN a user has the mobile app installed but is not logged in
WHEN they click the deeplink in a notification mailer
THEN they are navigated to the login page of the app

(source: Deeplinking for mobile application - Sheet1.csv)

## AC-DL-03: Deeplink when app is not installed redirects to app store

GIVEN a user does not have the mobile app installed
WHEN they click the deeplink
THEN they are redirected to the App Store (iOS) or Play Store (Android) for installation

(source: Deeplinking for mobile application - Sheet1.csv)

## AC-DL-04: Deeplink with invalid or expired session redirects to login

GIVEN a user clicks a deeplink with an invalid or expired session
WHEN the app processes the deeplink
THEN they are navigated to the login page

(source: Deeplinking for mobile application - Sheet1.csv)

## AC-DL-05: Deeplink with different user account shows no-content error

GIVEN a user clicks a deeplink for a learning they do not have access to
WHEN they log in to the app with a different account
THEN a no-content error message is displayed

(source: Deeplinking for mobile application - Sheet1.csv)

## AC-DL-06: Cross-platform deeplink routing

GIVEN a notification deeplink is clicked
WHEN the link is opened on iOS
THEN the user is navigated to the App Store; when opened on Android, the user is navigated to the Play Store

(source: Deeplinking for mobile application - Sheet1.csv)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[push-notifications]]
