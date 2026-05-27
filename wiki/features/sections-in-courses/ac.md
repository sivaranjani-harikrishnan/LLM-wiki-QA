# Acceptance Criteria: Sections in Courses

**Summary**: No formal AC document exists for sections in courses. Acceptance criteria below are inferred from test cases. See [[test-coverage]] for the full test case list.

**Sources**: `raw/Sections index within Courses - Sheet1 (2).csv`

**Last updated**: 2026-05-25

---

## Creator / Admin ACs

## AC-SC-01: Add Section button shown in course structure

GIVEN an admin or content publisher is viewing an empty or existing course structure
WHEN they view the course structure panel
THEN an "Add new section" button in the primary colour is displayed alongside the add lesson and add assessment buttons

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-02: Creating a section

GIVEN a creator clicks "Add new section"
WHEN the section is created
THEN it is given the default name "Untitled section" and assigned a series number

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-03: Section name supports alphanumeric and special characters with truncation

GIVEN a creator is editing a section name
WHEN they enter a long name
THEN the system truncates the name in the UI and shows the full name on hover as a tooltip

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-04: Section name and description are optional

GIVEN a creator creates a section
WHEN they do not fill in the name or description fields
THEN both fields are treated as optional — however a blank name prevents publishing (see AC-SC-07)

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-05: Section content management

GIVEN a section exists in the course structure
WHEN a creator interacts with it
THEN they can add any number of lessons and assessments within the section; a new section button appears on hover at the bottom of any section; content can be dragged and dropped within sections, across sections, and between sections and the main course structure

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-06: Section reordering via arrows

GIVEN multiple sections exist in the course structure
WHEN a creator views the section headers
THEN the first section shows a down arrow only, the last section shows an up arrow only, and all middle sections show both; clicking arrows reorders sections in steps

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-07: Cannot publish a course with empty sections

GIVEN a course has one or more sections with no content
WHEN the creator attempts to publish
THEN publishing is blocked and an error message is displayed; a section becomes empty when all its content is dragged out or deleted

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-08: Deleting a section with content shows confirmation

GIVEN a section contains lessons or assessments
WHEN the creator clicks delete on the section
THEN a confirmation slider is shown with help text advising the creator to relocate content via drag/drop if they want to keep it

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-09: Deleting an empty section requires no confirmation

GIVEN a section contains no content
WHEN the creator clicks delete
THEN the section is deleted immediately without a confirmation dialog

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-10: Discard changes reverts to last published version

GIVEN a creator has made changes to sections after publishing
WHEN they click "Discard changes"
THEN the course structure reverts to the last published version

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-11: Courses can exist with or without sections

GIVEN a creator is building a course
WHEN they configure the course structure
THEN they may create a course with no sections (only lessons/assessments), a course with only sections (all content inside sections), or a hybrid (content both inside and outside sections)

(source: Sections index within Courses - Sheet1 (2).csv)

---

## Learner View ACs

## AC-SC-12: Learner sees sections, lessons, and assessments in creator order

GIVEN a learner opens a course with sections
WHEN the course structure renders
THEN all sections, lessons, and assessments are displayed in the order set by the creator

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-13: Sections expand and collapse in learner view

GIVEN a learner is viewing a course with sections
WHEN they interact with a section
THEN sections can be expanded and collapsed; the section name, description, and content count (completed/total, e.g. "2/5") are shown; a tick mark shows completed items and a progress bar shows in-progress items

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-14: Clicking a section navigates to first content item

GIVEN a learner clicks on a section header
WHEN the click is registered
THEN the learner is navigated to the first content item within that section

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-15: Course completion requires all content regardless of section structure

GIVEN a learner is in a course with content inside and outside sections
WHEN they try to end the course
THEN they must have viewed all lessons and completed all assessments — regardless of whether content is in sections or not

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-16: Score calculation unchanged by sections

GIVEN a course uses sections
WHEN the score is calculated
THEN the existing score calculation logic applies identically to courses with or without sections

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-17: Sections not displayed in mobile app

GIVEN a learner views a course via the HeySales mobile app
WHEN the course has sections
THEN sections are not displayed in the mobile app

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-18: Sections displayed in Demo URL

GIVEN a learner views a course via a Demo URL
WHEN the course has sections
THEN sections are displayed in the Demo URL view

(source: Sections index within Courses - Sheet1 (2).csv)

## AC-SC-19: Progress bar shown for courses with more than one content item

GIVEN a learner views a course structure
WHEN the course has more than one lesson or assessment (with or without sections)
THEN a progress bar is displayed showing completion fraction (e.g. "0/5"); the fraction updates as content is completed; the denominator updates when content is added or removed

(source: Sections index within Courses - Sheet1 (2).csv)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[courses]]
- [[course-reports]]
