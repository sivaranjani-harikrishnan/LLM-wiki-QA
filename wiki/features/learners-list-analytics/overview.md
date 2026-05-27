# Feature: Learners List Analytics

**Summary**: The learners list in HeySales shows all assigned learners with their status across courses and podcasts, including a new In-Progress column for tracking partial completion.

**Sources**: `Learners list Analytics - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## What it does

The learners list provides admins with a per-learner view of engagement status across all learning types, broken into Not Started, In Progress, and Completed columns with learning-type-specific data.

## Who uses it

- **Admins / Content Publishers**: Monitor learner progress across all assignments

## Columns

### All Learners
- Profile picture
- Name
- Total learner count

### Not Started
- Assigned date (courses, podcasts) / Enrolled date (simulations)

### In Progress
- **Courses**: Progress bar (based on lessons + assessments completed); started date
- **Podcasts**: Progress bar (based on % of total duration listened); last engaged date; started date
- **Simulations**: NOT available — simulations do not have an In-Progress column

### Completed
| Learning Type | Data Shown |
|---|---|
| Courses | Completion flag (green % if passed, red % if failed — only for courses with assessments); Time spent; Completed date |
| Podcasts | Completion flag; Last engaged date; Time spent |
| Simulations | Score; "NA" if call ended in <2 min; Last call logged date |

### Completion flag behaviour
- Retake in-progress: no completion flag shown (even if previously completed)
- Completion flag + data shown per learning type (not generic)

## Key differences by learning type

| Feature | Courses | Podcasts | Simulations |
|---|---|---|---|
| In-Progress column | Yes (progress bar) | Yes (% duration) | No |
| Completed: score shown | Yes (% with pass/fail colour) | No | Yes (out of 10) |
| Completed: time spent | Yes | Yes | No |
| NA state | No | No | Yes (<2 min call) |

## Related pages

- [[test-coverage]]
- [[courses]]
- [[podcasts]]
- [[simulations]]
- [[course-reports]]
