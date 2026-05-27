# Acceptance Criteria: Podcast and Simulation in Courses

**Summary**: Defines how podcasts and simulations behave when included in courses — covering completion logic, progress, permissions, and scoring.

**Sources**: `raw/23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf`, `raw/40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf`

**Last updated**: 2026-05-25

---

## Podcast in Course ACs

## AC-PIC-01: Only published podcasts can be added to courses

GIVEN a course creator is adding content to a course
WHEN they choose to add a podcast
THEN only published podcasts are available for selection; draft or unpublished podcasts cannot be added

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

## AC-PIC-02: Podcast completion is global

GIVEN a podcast is included in one or more courses
WHEN a learner completes that podcast — whether from the standalone podcast player or from within a course
THEN the completion is recorded globally and automatically marks the podcast as complete in all courses that contain it

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

## AC-PIC-03: Progress carries across contexts

GIVEN a learner has partially listened to a podcast in one context (e.g. standalone)
WHEN they access the same podcast from within a course
THEN their listen progress is preserved and continues from where they left off

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

## AC-PIC-04: Removal and deletion handling

GIVEN a podcast is included in a course
WHEN the podcast is removed from the course or deleted entirely
THEN the course handles this gracefully (no broken state); existing completion records are preserved

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

## AC-PIC-05: Course access grants podcast access

GIVEN a learner is enrolled in a course that contains a podcast
WHEN the learner accesses the course
THEN they automatically have access to that podcast even if they do not have standalone podcast access

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

## AC-PIC-06: Required vs optional podcast

GIVEN a podcast is added to a course
WHEN the course creator configures the element
THEN they can mark the podcast as required (must complete to finish the course) or optional

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

## AC-PIC-07: Reporting matrices

GIVEN podcasts are included in courses
WHEN managers view course reports
THEN reporting shows podcast completion data within the course context alongside other course elements

(source: 23a8dd06-14f0-4d7d-81c8-46b09404aed4_Podcast_in_Course.pdf)

---

## Simulation in Course ACs

## AC-SIC-01: Simulation completion is per-course

GIVEN a simulation is included in one or more courses
WHEN a learner completes that simulation as a standalone activity (outside any course)
THEN the standalone completion does NOT automatically mark the simulation as complete within any course; course completion must be earned separately for each course

(source: 40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf)

## AC-SIC-02: Two completion stages

GIVEN a learner finishes a simulation run inside a course
WHEN the system processes the completion
THEN there are two stages: (1) the learner finishes the simulation run, and (2) the AI generates the scoring report; both must complete for the simulation to be fully counted

(source: 40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf)

## AC-SIC-03: "Course completed — final scores pending" state

GIVEN all course elements are completed but the AI report for a simulation has not yet generated
WHEN the course completion is evaluated
THEN the system shows a "Course completed — final scores pending" message rather than blocking completion

(source: 40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf)

## AC-SIC-04: Knowledge score vs Simulation score — simulation more prominent

GIVEN a simulation has both a knowledge assessment score and an overall simulation score
WHEN scores are displayed in the course context
THEN the Simulation score is displayed more prominently than the Knowledge score

(source: 40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf)

## AC-SIC-05: Only latest attempt counts for course score

GIVEN a learner attempts a simulation in a course multiple times
WHEN the course score is calculated
THEN only the learner's most recent attempt score counts toward the course score

(source: 40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf)

## AC-SIC-06: All attempts tracked in global report

GIVEN a learner has multiple simulation attempts within a course
WHEN a manager views the global simulation report (not just the course report)
THEN all attempts (not just the latest) are visible

(source: 40c5008c-c51d-4ae7-803f-c981c57a2961_Simulations_in_Course.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[podcasts]]
- [[simulations]]
- [[courses]]
- [[course-reports]]
- [[podcast-reports]]
