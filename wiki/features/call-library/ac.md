# Acceptance Criteria: Call Library

**Summary**: Defines the list view, detailed view, ordering, and upload behaviour for the Call Library.

**Sources**: `raw/c6215e1e-5b20-4b16-83a1-3ab63a6bcc55_Call_Library.pdf`, `raw/64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf`

**Last updated**: 2026-05-25

---

## List View ACs

## AC-CL-01: List view columns

GIVEN a user is viewing the Call Library list
WHEN calls are displayed
THEN each row shows: call summary, prospect email(s), rep email, date, time, deal name, and deal value

(source: c6215e1e-5b20-4b16-83a1-3ab63a6bcc55_Call_Library.pdf)

## AC-CL-02: Recency ordering with labelled groups

GIVEN the Call Library list is displayed
WHEN calls are ordered
THEN they are grouped by recency with labels: Today, Yesterday, This Week, Last Week, and Previous Month

(source: c6215e1e-5b20-4b16-83a1-3ab63a6bcc55_Call_Library.pdf)

## AC-CL-03: No duplicate calls

GIVEN multiple call sources may capture the same call
WHEN calls are displayed in the Call Library
THEN duplicate entries for the same call are not shown

(source: c6215e1e-5b20-4b16-83a1-3ab63a6bcc55_Call_Library.pdf)

---

## Detailed View ACs

## AC-CL-04: Detailed view fields

GIVEN a user clicks into a call in the Call Library
WHEN the detailed call view is shown
THEN it displays: duration, score, positives, observations, suggestions, parameter-level score breakdown, and the call recording

(source: c6215e1e-5b20-4b16-83a1-3ab63a6bcc55_Call_Library.pdf)

---

## Upload Call ACs

## AC-UC-01: Manual call upload

GIVEN a user wants to add a call that was not captured automatically
WHEN they use the upload feature
THEN they can manually upload a call recording to the Call Library

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-02: Upload date shown (not call date)

GIVEN a call is manually uploaded
WHEN its date is displayed in the Call Library
THEN the upload date is shown, not the original call date

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-03: "Uploaded by" pill

GIVEN a call was manually uploaded
WHEN it is displayed in the Call Library
THEN an "Uploaded by: [name]" pill is shown to distinguish it from automatically captured calls

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-04: Score pill

GIVEN a call has been scored
WHEN it is displayed in the Call Library
THEN a score pill is shown on the call entry

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-05: Prospect name extracted

GIVEN a call recording is uploaded
WHEN the system processes the upload
THEN the prospect's name is automatically extracted from the recording or metadata and shown in the call entry

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-06: Same detailed view as Zoom calls

GIVEN an uploaded call has been processed
WHEN the user views its detailed page
THEN it uses the same detailed view layout as Zoom-captured calls

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-07: Bulk upload supported

GIVEN a user wants to upload multiple calls at once
WHEN they use the upload feature
THEN bulk upload is supported (specific limit to be determined)

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

## AC-UC-08: Processing state persists on refresh

GIVEN a call has been uploaded and is being processed
WHEN the user refreshes the page
THEN the processing state is preserved and the call continues processing; progress is not lost

(source: 64ea62a4-7af2-4b76-988c-3c8a35353dde_Upload_Call_in_Call_Library.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[real-call-scoring]]
- [[custom-scorecards]]
