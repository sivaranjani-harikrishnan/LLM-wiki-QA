# Test Coverage: Simulation Reports

**Summary**: 59 test cases covering all simulation reporting metrics, learner views, rankings, time tracking, and attempt handling.

**Sources**: `Simulations Reports - Simulation Reports.csv`

**Last updated**: 2026-05-25

---

## Key TCs by topic

### Completion Rate (TC0001–TC0005)
- TC0001: Completion rate card shows assigned vs completed
- TC0002: Completion rate updates when new learners are added
- TC0003: Completed learners are clickable; not-started are disabled
- TC0004–TC0005: Completion rate card UI and placement

### Avg Score (TC0006–TC0010)
- TC0006: Avg score = total score across all attempts (including retakes) / total attempts
- TC0007: Avg score card UI
- TC0008–TC0010: Edge cases — single learner, multiple retakes, all completed

### Avg Time Spent (TC0011–TC0015)
- TC0011: Avg time spent = cumulative per learner / number of completed learners; does NOT separately include retake time
- TC0012–TC0015: Various learner count and retake scenarios

### Learner list and detailed report (TC0016–TC0025)
- TC0016: Completed learners clickable, not-started disabled
- TC0017: Detailed report screen shows back button, learner count, search bar, learner list with score + call date, report panel
- TC0018–TC0025: Search functionality, navigation between learners

### Latest Score and Team Avg (TC0026–TC0030)
- TC0026: Latest score = last attempt's score
- TC0027: Team avg = sum of best scores / completed learner count
- TC0028–TC0030: Dynamic recalculation as more learners complete

### Attempts taken (TC0031–TC0035)
- TC0031: Attempts count displayed; bar graph shows last 3 if >3 total
- TC0032: Attempts dropdown lists all attempts; NA for <2 min calls
- TC0033–TC0035: Attempt switching updates breakdown content

### Ramp-up rate (TC0036–TC0040)
- TC0036: Ramp-up rate = assigned vs enrolled; hours if <24h, days if ≥24h

### Time Spent (TC0041–TC0043)
- TC0041: Time spent = cumulative across all attempts

### Ranking (TC0044–TC0047)
- TC0044: Ranking based on best score; dynamic

### Breakdown section (TC0048–TC0059)
- TC0048: Last call date and duration in breakdown
- TC0049–TC0059: Parameter-by-parameter display, call property list correctness

---

## Related pages

- [[overview]]
- [[simulation-call-recording]]
