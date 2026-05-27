# Test Coverage: Simulations

**Summary**: Test cases covering simulation creation, profile extraction, and admin creation flow.

**Sources**: `Custom Scorecards - Simulation creation (1).csv`, `Profile extraction - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Profile Extraction TCs (TC0001–TC0025)

### TC0001: Creating a simulation
**What this tests**: Validate Admins should be able to create simulation successfully

**Precondition**: User should have admin or Content publisher role

(source: `Profile extraction - Sheet1.csv`)

---

### TC0002: "Add source" button in scenario screen
**What this tests**: Validate In the scenario screen there should be an "add source" button available

(source: `Profile extraction - Sheet1.csv`)

---

### TC0003: Click on "add source" button
**What this tests**: Validate Clicking on the add source button should bring the Call recording slider

(source: `Profile extraction - Sheet1.csv`)

---

### TC0004: Empty state in call recording slider
**What this tests**: Validate In the call recording slider if no calls have been uploaded an empty message should be displayed

(source: `Profile extraction - Sheet1.csv`)

---

### TC0005: UI of call recording slider
**What this tests**: Validate In the call recording slider there should be upload new call button, list of all the uploaded calls, add and cancel button

(source: `Profile extraction - Sheet1.csv`)

---

### TC0006: "Upload new call" button
**What this tests**: Validate clicking on the "upload new call" should open the local file upload

(source: `Profile extraction - Sheet1.csv`)

---

### TC0007: File type restriction for upload
**What this tests**: Validate User should be able to upload only MP4 and MP3 from local device

(source: `Profile extraction - Sheet1.csv`)

---

### TC0008: Add source button updates to "Generate" after upload
**What this tests**: Validate After uploading a video the add source button should update as generate

(source: `Profile extraction - Sheet1.csv`)

---

### TC0009–TC0010: Generate button and extraction progress
**What this tests**: Clicking Generate starts extraction; "transcribing the call recording" placeholder shown during extraction

(source: `Profile extraction - Sheet1.csv`)

---

### TC0011: Successful extraction auto-fills profile
**What this tests**: Validate After successful extraction company profile, Buyer profile, and Buyer need should be updated from the call

(source: `Profile extraction - Sheet1.csv`)

---

### TC0012–TC0015: Error states
**What this tests**: Random MP4/MP3 fails extraction; error screen shows "profile generation failed" with retry and upload-new-asset buttons; retry retriggers extraction; upload new asset opens file picker

(source: `Profile extraction - Sheet1.csv`)

---

### TC0016: Editing extracted details
**What this tests**: Validate user should be able to edit the extracted details in all 3 sections of the simulation

(source: `Profile extraction - Sheet1.csv`)

---

### TC0017: Image/paged files rejected
**What this tests**: Validate User should not be able to add image / paged files for extraction

(source: `Profile extraction - Sheet1.csv`)

---

### TC0018–TC0019: Previously uploaded calls
**What this tests**: All previously uploaded calls listed and scrollable; user can create simulation from previously extracted call

(source: `Profile extraction - Sheet1.csv`)

---

### TC0020: UI of call card
**What this tests**: Validate In the call card, Uploaded files name, created date and time, Company name, Buyer name, Created by name with profile pic, and a delete icon should be displayed

(source: `Profile extraction - Sheet1.csv`)

---

### TC0021–TC0022: Delete an extracted call
**What this tests**: User can delete a call (with confirmation slider); deleting a call does not disturb simulations generated from it

(source: `Profile extraction - Sheet1.csv`)

---

### TC0024: Account isolation
**What this tests**: Validate the call extracted under Account A should not be visible under Account B

(source: `Profile extraction - Sheet1.csv`)

---

### TC0025: Upload call while editing a published simulation
**What this tests**: Validate User should be able to edit the published simulation and add a call to generate a new transcription

(source: `Profile extraction - Sheet1.csv`)

---

## Related pages

- [[overview]]
- [[simulation-reports]]
- [[custom-scorecards]]
