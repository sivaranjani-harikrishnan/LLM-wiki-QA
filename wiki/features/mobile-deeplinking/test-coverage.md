# Test Coverage: Mobile Deeplinking

**Summary**: 6 test cases covering deeplink behaviour for logged-in, logged-out, app-not-installed, expired session, wrong-user, and cross-platform scenarios.

**Sources**: `Deeplinking for mobile application - Sheet1.csv`

**Last updated**: 2026-05-25

---

## TC0001: Deeplink when user is logged in

**What this tests**: Validate Clicking on the Get started Button in the notification mailer should navigate them to the learning in the app

**Steps**:
1. Open notification mailer
2. Click the learning deeplink

**Expected result**: App opens directly; user lands on specific learning's preview page in My Space

(source: `Deeplinking for mobile application - Sheet1.csv`)

---

## TC0002: Deeplink when user is logged out

**What this tests**: Validate Clicking on the Get started Button in the notification mailer should navigate them to the log in page of the app

**Steps**:
1. Open notification mailer
2. Click the learning deeplink
3. Enter valid credentials and log in

**Expected result**: App opens to login page; after successful login, user redirected to specific learning's preview page in My Space

(source: `Deeplinking for mobile application - Sheet1.csv`)

---

## TC0003: Deeplink when app is not installed

**What this tests**: Validate User should be redirected to the App Store (iOS) or Play Store (Android) page of the application for installation

**Expected result**: Redirected to App Store (iOS) or Play Store (Android)

(source: `Deeplinking for mobile application - Sheet1.csv`)

---

## TC0004: Deeplink with invalid/expired session

**What this tests**: Validate Clicking on the Get started Button in the notification mailer should navigate them to the log in page of the app

**Steps**:
1. Open notification mailer with expired session
2. Click deeplink
3. Enter valid credentials

**Expected result**: App opens to login page; after login, redirected to learning preview page in My Space

(source: `Deeplinking for mobile application - Sheet1.csv`)

---

## TC0005: Deeplink with different user login (no access to learning)

**What this tests**: Validate When the user tries to log in to the app as a user with no access to the learning, no content error message should be displayed

**Steps**:
1. Open notification mailer
2. Click deeplink
3. Log in as an unassigned user

**Expected result**: "No content" error message displayed

(source: `Deeplinking for mobile application - Sheet1.csv`)

---

## TC0006: Cross-platform validation

**What this tests**: Validate Clicking the link notification from iPhone should navigate the user to app store and clicking the link notification from android should navigate the user to Play store

**Expected result**: iOS → App Store; Android → Play Store

(source: `Deeplinking for mobile application - Sheet1.csv`)

---

## Related pages

- [[overview]]
- [[push-notifications]]
