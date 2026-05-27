# Test Coverage: No Permission and Offline Screens

**Summary**: 12 test cases covering login error states (no HeySales access, invalid credentials), No Permission page behaviour, and offline screen behaviour across all main screens.

**Sources**: `No permission page_You are offline screens - Sheet1.csv`

**Last updated**: 2026-05-25

---

## TC0001: Paperflite user without HeySales access tries to login

**What this tests**: Validate paperflite user without access to hey sales should not be able to login

**Precondition**: User is a valid paperflite user but has no HeySales access

**Steps**:
1. Launch app
2. Enter valid PF credentials (no HeySales access)
3. Tap Login
4. Check the UI of No Permission page

**Expected result**: "No Permission" page shown with "You don't have permission to this application" and Back button

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0002: Same user with HeySales enabled can login

**What this tests**: Validate paperflite user with HeySales access should be able to login

**Expected result**: Login succeeds; user redirected to Home screen

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0003: Random user with no Paperflite account

**What this tests**: Validate An error message "bad credentials error(invalid username/password)" should be displayed

**Expected result**: "Invalid username/password" error on login screen; user stays on login page

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0004: Back button from No Permission page

**What this tests**: Validate Clicking on the back button user should land on the login page again

**Expected result**: User redirected to Login page

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0005: Retry login after No Permission

**What this tests**: Validate User should be able to login via a valid paperflite account with hey sales enabled after navigating back from No Permission

**Steps**:
1. Tap Go Back from No Permission page
2. Enter valid PF credentials (with HeySales access)
3. Tap Login

**Expected result**: Login succeeds; user redirected to Home screen

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0006–TC0008: Offline on main screens

**What this tests**: When the user goes offline on Home, My Space, or Explore screen, "You are Offline" page is displayed

**Expected result**: Offline page shown for each respective screen

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0009: Offline during content consumption

**What this tests**: Validate When the user goes to offline in middle of a lesson viewer, assessment viewer, or course view, there should be no offline page; app should continue to render the UI as much as loaded and stop

**Expected result**: No offline page during content viewing; cached UI continues rendering

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0010: Navigate back after going offline mid-content

**What this tests**: Validate When user navigates from the learning preview, "You are offline" page should be displayed

**Steps**:
1. Start learning preview
2. Turn off internet mid-way
3. Tap back to Home/My Space/Explore

**Expected result**: Offline page shown on the respective section

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0011: Reconnect internet from Offline page

**What this tests**: Validate When user is connected to internet while in offline page, the respective screen should render

**Expected result**: App detects restored connection; user redirected to correct screen with updated content

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## TC0012: UI validation of Offline page

**What this tests**: Validate The UI elements in the Offline page should match the UI screens

**Expected result**: All elements match design specification

(source: `No permission page_You are offline screens - Sheet1.csv`)

---

## Related pages

- [[overview]]
- [[mobile-deeplinking]]
