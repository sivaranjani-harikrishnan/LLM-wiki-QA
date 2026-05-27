# Test Coverage: Course Reports

**Summary**: 77 test cases covering all course reporting metrics, learner views, Q&A breakdowns, and sections-based course reporting.

**Sources**: `Course Reports - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Completion Rate (TC0001–TC0008)
- TC0001: Completion rate = completed / assigned
- TC0002–TC0008: Various learner count combinations and retake scenarios

### Pass % (TC0009–TC0018)
- TC0009: Pass % = passed / completed (not assigned)
- TC0010: Retake can change pass status (failed → passed, passed → failed)
- TC0011: Threshold change applies only to new completions (not retroactive)
- TC0012: All completed (including failed) counted in avg score; only passed counted in pass %
- TC0013–TC0018: Various threshold settings and retake scenarios

### Avg Score (TC0019–TC0027)
- TC0019: Avg score = total score across all attempts (including retakes) / total attempts
- TC0020–TC0027: Multi-attempt and multi-learner scenarios

### Avg Time Spent (TC0028–TC0035)
- TC0028: Avg time spent = cumulative per learner / learner count; retakes added cumulatively per learner
- TC0029–TC0035: Retake time scenarios

### Total Time Spent (TC0036–TC0040)
- TC0036: Total time = cumulative across all completed learners across all attempts
- TC0037–TC0040: Multi-learner and retake scenarios

### Learner list (TC0041–TC0045)
- TC0041: Completed learners clickable; not-started disabled
- TC0042–TC0045: Learner list display and navigation

### Detailed report (TC0046–TC0060)
- TC0046: Latest score = last attempt; team avg = best scores / learner count
- TC0047: Ranking by best score; dynamic
- TC0048: Ramp-up rate shown
- TC0049: Time spent cumulative
- TC0050: Breakdown shows lessons + assessments
- TC0051: Q&A slider shows each question with correct/incorrect marking
- TC0052: Attempts dropdown shows last 3 (if >3 total)
- TC0053–TC0060: Sections-based course breakdown shows section structure

### Other (TC0061–TC0077)
- TC0061–TC0077: Edge cases, empty states, search in learner list, pagination

---

## Related pages

- [[overview]]
- [[courses]]
