# Test Coverage: Due Date and Reminder Notifications

**Summary**: 75 test cases covering due date picker, relative due dates, hourglass icons, reassignment rules, reminder schedule, deactivated users, and no-clash rule.

**Sources**: `Due date and reminder notifications - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Due date picker (TC0001–TC0010)
- TC0001: Specific due date picker opens calendar; past dates disabled
- TC0002: Default time is 12:00 AM (non-changeable)
- TC0003–TC0006: Relative due date options (1d/3d/7d/14d/1mo/2mo) and custom numeric field
- TC0007: Due date not mandatory (can assign without due date)
- TC0008–TC0010: User groups get same due date as individuals

### Hourglass icons (TC0011–TC0020)
- TC0011: Green hourglass — completed on time
- TC0012: Red hourglass — completed late
- TC0013: In-progress shows due/overdue date + progress
- TC0014: Not-started shows due/overdue date
- TC0015: Completed hides due date (Retake only)
- TC0016–TC0020: Various completion timing scenarios

### Reassignment rules (TC0021–TC0030)
- TC0021: Not-started learner reassigned → original assignment date kept
- TC0022: In-progress learner reassigned → original assignment date kept
- TC0023: Completed learner reassigned → new assignment date used
- TC0024–TC0030: Various reassignment and due date scenarios

### Reminder schedule (TC0031–TC0060)
- TC0031: 50% of gap always sent (e.g., 20-day gap → reminder at day 10)
- TC0032: If gap >30 days → 7-day reminder also sent
- TC0033: If gap >10 days → 3-day reminder also sent
- TC0034: 1-day reminder always sent
- TC0035: No-clash: if 50% reminder and 1-day would coincide → only 1 email sent
- TC0036: Reminders stop after completion
- TC0037: Deactivated users excluded from reminders
- TC0038: Reassignment without starting does not trigger new notification
- TC0039–TC0060: Various gap length scenarios testing which reminders fire

### Edge cases (TC0061–TC0075)
- TC0061–TC0075: Combinations of learner states, reassignment, and reminder timing edge cases

---

## Related pages

- [[overview]]
- [[push-notifications]]
