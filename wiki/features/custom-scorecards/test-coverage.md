# Test Coverage: Custom Scorecards

**Summary**: Test cases for scorecard creation, management, and selection during simulation creation.

**Sources**: `Custom Scorecards - Scorecard creation.csv` (48 TCs), `Custom Scorecards - Simulation creation (1).csv` (17 TCs)

**Last updated**: 2026-05-25

---

## TC0001: Check the Scorecard option in settings

**What this tests**: Validate In the heysales enabled account Under settings for Admins and Content publishers there should be a new option "Scorecard"

**Priority**: Medium | **Type**: Functional

**Precondition**: Hey sales should be enabled, and user should have Admin / Content publisher access

**Steps**:
1. Log in as admin / Content publisher
2. Navigate to settings

**Expected result**: Scorecard option is visible in settings for Admin/Content Publisher

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0002: Check the scorecard option in settings as a non admin user

**What this tests**: Validate In the heysales enabled account Under settings for Normal user and BI Analyst the scorecard option should not be available

**Priority**: Medium | **Type**: Functional

**Precondition**: Hey sales should be enabled, and user should have Normal user / BI Analyst access

**Expected result**: Scorecard option is not visible for Normal users and BI Analysts

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0003: Check the Scorecard option in settings in an account without heysales enabled

**What this tests**: Validate If the heysales is not enabled, Under settings for all the users the scorecard option should not be available

**Priority**: Medium | **Type**: Functional

**Expected result**: Scorecard option is not visible for any user when HeySales is disabled

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0004: Check the UI of the Scorecard screen

**What this tests**: Validate In the scorecard screen, heading "scorecard" and a sub text, a default scorecard, a delete button, Rename button, clone button, and Create new scorecard button should be displayed

**Priority**: Medium | **Type**: Functional

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0005: Check deleting the default scorecard

**What this tests**: Validate User should not be able to delete the default scorecard, when user clicks on the delete button the default scorecard should not be available for selection

**Priority**: Medium | **Type**: Functional

**Expected result**: Delete button on default scorecard does nothing / is disabled

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0006: Check the UI of the scorecard card

**What this tests**: Validate In the scorecard the card name, Active / draft, type of the card, default tag, Parameter count, sub-parameter count, and last updated date should be displayed

**Priority**: Medium | **Type**: Functional

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0007: Check renaming the default scorecard

**What this tests**: Validate User should not be able to rename the default scorecard

**Priority**: Medium | **Type**: Functional

**Expected result**: Rename button on default scorecard does nothing / is disabled

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0008: Check having multiple scorecards as default

**What this tests**: Validate In an account there should be only one scorecard should be tagged as default

**Priority**: Medium | **Type**: Functional

**Steps**:
1. Make Scorecard A default
2. Make Scorecard B default
3. Verify Scorecard A loses default tag; Scorecard B gains it

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0009: Check deleting the default scorecard (impact on simulations)

**What this tests**: Validate When a default scorecard is deleted, the simulations to which the scorecard is tagged should not be affected. After the default scorecard is deleted system should make the paperflite scorecard as default

**Priority**: Medium | **Type**: Functional

**Steps**:
1. Make Scorecard X default
2. Create 2 simulations (assigned to 5 learners, 2 complete)
3. Delete Scorecard X
4. Verify simulations are unaffected; Paperflite scorecard becomes default

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## TC0010–TC0017: Simulation creation flow (scorecard selection)

Tests covering:
- TC0010: Two-step simulation creation flow (step 1: time/difficulty/scorecard; step 2: profile)
- TC0011: Default scorecard pre-populated during simulation creation
- TC0012: Preview button navigates to detailed scorecard screen
- TC0013: Change button navigates to filtered scorecard list
- TC0014: Scorecard list filtered by simulation call type (e.g. cold call only shows cold call + all-type scorecards)
- TC0015: Empty message shown when no scorecard matches simulation type
- TC0016: UI of scorecard section (heading, name, sub-text, parameter count, sub-parameter count, Preview + Change buttons)
- TC0017: Simulation completion report based on tagged scorecard

(source: `Custom Scorecards - Simulation creation (1).csv`)

---

## Scorecard creation detail TCs (from Scorecard creation CSV)

Key scenarios covered across TC0001–TC0048:
- Create scorecard slider (name + description fields)
- Parameter creation (untitled default, unlimited count)
- Sub-parameter requirement (at least 1 to publish)
- Weightage rules (numeric only, max 100, no negatives/decimals)
- Draft vs Active states
- Set-as-default toggle
- Call type selection (All/Discovery/Cold Call/Follow-up)
- Clone creates "Clone of [name]"
- Delete does not affect existing simulations
- Discard reverts to last published version
- Non-English document support

(source: `Custom Scorecards - Scorecard creation.csv`)

---

## Related pages

- [[overview]]
- [[ac]]
- [[simulations]]
