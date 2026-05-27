# Feature: Profile Extraction

**Summary**: Profile Extraction lets admins upload an MP4 or MP3 call recording to auto-populate the Company Profile, Buyer Profile, and Buyer Needs fields during simulation creation.

**Sources**: `Profile extraction - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Instead of manually entering simulation scenario details, admins can upload a real call recording. The system transcribes it and extracts structured profile data to pre-fill the simulation creation fields.

## Who uses it

- **Admins / Content Publishers**: Use during simulation creation or editing

## How it works

### Accessing
- In simulation creation → Scenario screen → "Add Source" button
- Clicking "Add Source" opens the Call Recording slider

### Call Recording slider
- Empty state: "no calls uploaded" empty message shown
- With calls: lists all previously uploaded call recordings for the account
- Buttons: Upload New Call, Add, Cancel

### Uploading a call
1. Click "Upload new call" → local file picker opens
2. Supported types: MP4, MP3 only
3. Rejected types: images, paged files (PDF, PPT, DOC), ZIP, etc.
4. After upload: "Add Source" button changes to "Generate"

### Extraction process
1. Click Generate → "transcribing the call recording" placeholder shown
2. On success: Company profile, Buyer profile, Buyer needs auto-filled from transcript
3. On failure: error screen shown with "profile generation failed" message + Retry and Upload New Asset buttons
4. Retry: retriggers extraction
5. Upload New Asset: opens file picker for a new recording

### Call library within slider
- All previously uploaded calls listed (account-scoped; Account A calls not visible to Account B)
- Call card shows: uploaded file name, created date/time, Company name, Buyer name, Created by name + profile pic, delete icon
- Scroll works for large lists

### Reusing extracted calls
- Previously extracted calls can be selected to create new simulations
- All relevant details pre-filled from the selected call's extracted data

### Deleting an extracted call
1. Click delete icon → confirmation slider shown
2. Confirm → call deleted from slider
3. Simulations already generated from the deleted call are NOT affected

### Editing published simulations
- Available during editing: upload new call and re-extract profile data for a published simulation

### Isolation
- Calls extracted under Account A are not visible in Account B's call recording slider

## Related pages

- [[simulations]]
- [[test-coverage]]
