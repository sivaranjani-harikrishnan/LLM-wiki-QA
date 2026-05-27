# Test Coverage: Call Library

**Summary**: 30 test cases covering Call Library navigation, UI, call card metadata, time grouping, detail view, score display, empty state, no-audio state, and duplicate prevention.

**Sources**: `Call library - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Navigation and rendering (TC0001–TC0005)
- TC0001: Navigate to Call Library from Studio
- TC0002: Page renders correctly with expected UI elements
- TC0003: Admin access to Call Library
- TC0004: Learner/rep access to Call Library (own calls only)
- TC0005: Empty state: "No calls added yet!" shown when no calls exist

### Call card UI and metadata (TC0006–TC0012)
- TC0006: Call card shows meeting date, title, prospect email, rep email, score as %
- TC0007: Score displayed as percentage (converted from 5-point scale)
- TC0008: Time grouping pill: Today
- TC0009: Time grouping pill: Yesterday
- TC0010: Time grouping pill: This Week
- TC0011: Time grouping pill: Last Week
- TC0012: Time grouping pill: 2 Weeks Ago / 3 Weeks Ago / Month+Year

### Call sources (TC0013–TC0018)
- TC0013: Calls from Zoom + HubSpot integration appear in library
- TC0014: Calls from Zoom + MS Dynamics integration appear in library
- TC0015–TC0018: Various multi-integration scenarios

### Call record detail (TC0019–TC0025)
- TC0019: Click call card → opens detail view
- TC0020: Detail view shows metadata (meeting date, title, prospect, rep)
- TC0021: Detail view shows summary
- TC0022: Detail view shows scorecard (parameter breakdown)
- TC0023: Detail view shows recording
- TC0024: No audio message when recording is unavailable
- TC0025: Scorecard breakdown matches the account's default scorecard used at call time

### Duplicate prevention and other edge cases (TC0026–TC0030)
- TC0026: Same deal, same call → only one record in library (no duplicates)
- TC0027–TC0030: Expired integration calls, multi-invitee calls, calls with multiple deals

---

## Related pages

- [[overview]]
- [[real-call-scoring]]
