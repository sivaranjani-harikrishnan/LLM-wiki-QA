# Feature: No Permission and Offline Screens

**Summary**: The HeySales mobile app shows distinct error screens when a user lacks HeySales access ("No Permission") or loses internet connectivity ("You are Offline").

**Sources**: `No permission page_You are offline screens - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Two error states protect the mobile app experience:

1. **No Permission page**: Shown when a valid Paperflite user without HeySales access tries to log in
2. **You are Offline page**: Shown when the user loses internet connectivity while navigating the app

## Who uses it

- **All mobile app users**: Both screens can be encountered by any user

---

## No Permission screen

### When shown
- User has valid Paperflite credentials but HeySales is not enabled for their account
- Invalid credentials (wrong username/password) show a different error: "Invalid username/password" on the login screen (user stays on login page)

### UI elements
- Text: "You don't have permission to this application"
- Back button

### Back button
- Clicking Back returns user to the login page

### After enabling HeySales access
- User can return to login page (via Back) and log in successfully with the same credentials once HeySales is enabled

---

## You are Offline screen

### When shown
- User is logged in and loses internet connection while on Home, My Space, or Explore screens
- Tapping back while in a learning (lesson/assessment/course) when offline also shows Offline screen on the respective section

### When NOT shown (exception)
- Mid-content (lesson viewer, assessment viewer, course view): the Offline page is NOT shown; the app continues to render already-loaded UI and stops loading new content

### Reconnect behaviour
- When internet is restored while on the Offline page, the respective screen (Home/My Space/Explore) renders automatically

### UI elements
- Match design specification (UI screens)

---

## Related pages

- [[test-coverage]]
- [[push-notifications]]
- [[mobile-deeplinking]]
