# Test Coverage: Learners List Analytics

**Summary**: 18 test cases covering the In-Progress column addition for courses and podcasts, and completion data display per learning type.

**Sources**: `Learners list Analytics - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## Key TCs

### In-Progress column (TC0001–TC0006)
- TC0001: In-Progress column added for courses (progress bar based on lessons + assessments completed) and podcasts (based on % of duration listened)
- TC0002: Simulations do NOT have an In-Progress column
- TC0003: Course In-Progress shows progress bar + started date
- TC0004: Podcast In-Progress shows % of duration listened + last engaged date + started date
- TC0005: Retake in-progress: completion flag not shown
- TC0006: In-Progress column UI and layout

### All-learners column (TC0007–TC0008)
- TC0007: All-learners column shows profile pic, name, and count
- TC0008: Not-started column shows assigned/enrolled date

### Completed column (TC0009–TC0018)
- TC0009: Courses — green % if passed, red % if failed (only for courses with assessments)
- TC0010: Courses — time spent + completed date
- TC0011: Podcasts — completion flag + last engaged date
- TC0012: Podcasts — time spent
- TC0013: Simulations — score shown
- TC0014: Simulations — "NA" shown if call ended in <2 min
- TC0015: Simulations — last call logged date shown
- TC0016: Retake in-progress: no completion flag even if previously completed
- TC0017: Completion flag + data is specific per learning type (not generic)
- TC0018: Completed date shown for courses; last engaged for podcasts

---

## Related pages

- [[overview]]
- [[courses]]
- [[podcasts]]
- [[simulations]]
