# Acceptance Criteria: No Permission Page / You Are Offline Screens

**Summary**: No formal AC document exists for these screens. Acceptance criteria below are inferred from test cases. See [[test-coverage]] for the full test case list.

**Sources**: `raw/No permission page_You are offline screens - Sheet1.csv`

**Last updated**: 2026-05-25

---

## No Permission Page ACs

## AC-NPO-01: Paperflite user without HeySales access cannot log in

GIVEN a user is a valid Paperflite user but has no HeySales access
WHEN they attempt to log in to HeySales
THEN the no-permission page is displayed and login is blocked

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-02: Granting HeySales access enables login

GIVEN a Paperflite user previously blocked by no-permission
WHEN HeySales access is enabled for their account
THEN they are able to log in successfully

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-03: Non-Paperflite user sees credentials error

GIVEN a user with no Paperflite account attempts to log in to HeySales
WHEN they enter credentials
THEN a "bad credentials error (invalid username/password)" message is displayed

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-04: Back button from no-permission page returns to login

GIVEN a user is on the no-permission page
WHEN they tap the back button
THEN they are navigated back to the login page

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-05: Retry login from no-permission page

GIVEN a user is on the no-permission page
WHEN they retry login with a valid Paperflite account that has HeySales access
THEN they are logged in successfully

(source: No permission page_You are offline screens - Sheet1.csv)

---

## Offline Screen ACs

## AC-NPO-06: Offline on main screens shows "You Are Offline" page

GIVEN a user loses internet connectivity while on the Home, My Space, or Explore screen
WHEN the connection drops
THEN the "You are Offline" page is displayed

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-07: Offline during content consumption — no offline page

GIVEN a user is actively consuming content (lesson viewer, assessment viewer, or course view) and loses connectivity
WHEN the connection drops
THEN no offline page is shown; the app continues to render the UI as far as it has loaded and stops

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-08: Navigating back from content while offline shows offline page

GIVEN a user is in content consumption and offline
WHEN they navigate back from the learning preview
THEN the "You are Offline" page is displayed

(source: No permission page_You are offline screens - Sheet1.csv)

## AC-NPO-09: Reconnecting internet while on offline page restores the screen

GIVEN a user is on the "You are Offline" page
WHEN internet connectivity is restored
THEN the respective screen renders correctly

(source: No permission page_You are offline screens - Sheet1.csv)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[mobile-deeplinking]]
