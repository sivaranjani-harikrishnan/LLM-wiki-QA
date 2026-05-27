# Acceptance Criteria: Courses

**Summary**: Defines course scheduling, archiving, due dates, completion progress display, and the completion screen shown to learners.

**Sources**: `raw/0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf`, `raw/8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf`, `raw/1338a993-a002-40cd-a3d1-bb00057a1a79_Course_Completion__.pdf`

**Last updated**: 2026-05-25

---

## Scheduling ACs

## AC-CS-01: Minimum and maximum scheduling window

GIVEN a creator wants to schedule a course for future publication
WHEN they set the scheduled publication date
THEN the minimum lead time is 1 hour from now and the maximum is 2 years in the future

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CS-02: Scheduled status

GIVEN a course is saved with a future publication date
WHEN the course is viewed before that date
THEN its status displays as "Scheduled"

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CS-03: Auto-publication

GIVEN a course has a scheduled publication date
WHEN that date and time is reached
THEN the course automatically publishes without requiring manual action

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

---

## Archiving ACs

## AC-CA-01: Manual archiving

GIVEN a course is published
WHEN an admin manually archives the course
THEN the course is moved to an archived state and no longer appears in active course listings

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CA-02: Scheduled archiving

GIVEN a course is published
WHEN an admin sets a scheduled archive date
THEN the course automatically archives on that date

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CA-03: Content-driven archiving via Paperflite asset expiry

GIVEN a course contains Paperflite assets
WHEN a linked Paperflite asset expires
THEN the course is automatically archived as a result of the asset expiry

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

---

## Due Date ACs

## AC-CD-01: Specific date due date

GIVEN a course has a due date configured
WHEN the due date is set as a specific calendar date
THEN all enrolled learners have the same fixed deadline

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CD-02: Relative due date (relative to enrollment)

GIVEN a course has a due date configured
WHEN the due date is set as relative (e.g. "X days after enrollment")
THEN each learner's deadline is calculated from their individual enrollment date

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CD-03: Overdue tracking

GIVEN a learner has not completed a course by its due date
WHEN the due date passes
THEN the system marks the learner as overdue for that course

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

## AC-CD-04: Reminder notifications

GIVEN a course has a due date
WHEN the due date is approaching
THEN reminder notifications are sent to learners who have not yet completed the course

(source: 0c7e0ab5-b0aa-4726-b90b-28bea18ac713_COURSE_MANAGEMENT.pdf)

---

## Course Completion Progress ACs

## AC-CP-01: Progress bar above first element

GIVEN a learner is enrolled in a course with multiple elements
WHEN they view the course
THEN a progress bar is displayed above the first course element

(source: 1338a993-a002-40cd-a3d1-bb00057a1a79_Course_Completion__.pdf)

## AC-CP-02: Fraction display

GIVEN a learner is in progress on a course
WHEN they view the progress indicator
THEN a fraction is shown (e.g. "3 / 7") showing completed elements over total elements

(source: 1338a993-a002-40cd-a3d1-bb00057a1a79_Course_Completion__.pdf)

## AC-CP-03: Real-time progress update

GIVEN a learner completes a course element
WHEN they return to the course view
THEN the progress bar and fraction update in real time to reflect the completion

(source: 1338a993-a002-40cd-a3d1-bb00057a1a79_Course_Completion__.pdf)

## AC-CP-04: Only shown for courses with more than one element

GIVEN a course has exactly one element
WHEN a learner views that course
THEN no progress bar or fraction is displayed

(source: 1338a993-a002-40cd-a3d1-bb00057a1a79_Course_Completion__.pdf)

## AC-CP-05: In-progress button shows resume state

GIVEN a learner has started but not completed a course
WHEN they view the course entry point (e.g. course card)
THEN the primary button reads "Resume" and shows "X% completed"

(source: 1338a993-a002-40cd-a3d1-bb00057a1a79_Course_Completion__.pdf)

---

## Course Completion Screen ACs

## AC-CCS-01: Celebration state

GIVEN a learner completes a course
WHEN the completion screen is shown
THEN it presents a celebration state (visual celebration animation or congratulatory display)

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-02: Skills earned

GIVEN a learner completes a course
WHEN the completion screen is shown
THEN it displays the skills they earned from completing the course

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-03: Score percentage

GIVEN a learner completes a course
WHEN the completion screen is shown
THEN the learner's overall score percentage is displayed

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-04: Peer percentile

GIVEN a learner completes a course
WHEN the completion screen is shown
THEN their score's percentile relative to peers is displayed

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-05: Time comparison

GIVEN a learner completes a course
WHEN the completion screen is shown
THEN their time to complete is shown with a comparison to peers or an average

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-06: Attempts to pass

GIVEN a learner completes a course (possibly after multiple attempts)
WHEN the completion screen is shown
THEN the number of attempts it took to pass is displayed

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-07: Progression delta on retake

GIVEN a learner has retaken a course and improved their score
WHEN the completion screen is shown
THEN a progression delta is displayed showing the improvement from their previous attempt

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

## AC-CCS-08: Leaderboard position

GIVEN a learner completes a course
WHEN the completion screen is shown
THEN their current leaderboard position (ranking among peers) is displayed

(source: 8ddff8f3-cfc1-4175-9431-cb6827f78c4c_Course_Completion_Screen.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[podcast-simulation-in-courses]]
- [[course-reports]]
- [[due-date-notifications]]
- [[sections-in-courses]]
