# Feature: Due Date and Reminder Notifications

**Summary**: Admins can set due dates on learning assignments; the system sends automated email reminders to learners on a cascading schedule based on the gap between assignment and due date.

**Sources**: `Due date and reminder notifications - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Due dates can be attached to any learning assignment (course, podcast, simulation). The system sends reminder emails to learners who have not yet completed the learning, according to a fixed reminder schedule.

## Who uses it

- **Admins / Content Publishers**: Set due dates when assigning learners
- **Learners**: Receive reminder emails; see due/overdue status in their content list

## Due date types

### Specific Date
- Date picker with calendar
- Past dates are disabled
- Default time: 12:00 AM (not changeable)

### Relative Due Date
- Predefined options: 1 day, 3 days, 7 days, 14 days, 1 month, 2 months
- Custom numeric field (numeric only)
- Calculated from the date of assignment

## Due date is not mandatory

Admins can assign content without setting a due date.

## Hourglass icons in learner list

- Green hourglass: learner completed on time
- Red hourglass: learner completed late
- Due/overdue date shown for in-progress and not-started learners
- Completed learners: due date hidden (Retake only)

## Reassignment rules

| Learner state at reassignment | Assignment date used |
|---|---|
| Not started | Original first assignment date kept |
| In progress | Original first assignment date kept |
| Completed | New assignment date used |

## User groups

Learners assigned through a user group receive the same due date as individual learners.

## Reminder email schedule (cascading)

The reminder schedule is based on the gap between assignment date and due date:

| Condition | Reminder sent |
|---|---|
| Always | 50% of gap (e.g., if 20-day gap → reminder at day 10) |
| If gap > 30 days | 7-day reminder before due |
| If gap > 10 days | 3-day reminder before due |
| Always | 1-day reminder before due |

### No-clash rule
If the 50% reminder and the 1-day reminder would fall on the same day, only ONE email is sent (not two).

### Reminders stop on completion
Once a learner completes the learning, no further reminders are sent.

### Deactivated users
Deactivated users are excluded from all reminder emails.

### Reassignment without starting
If a learning is reassigned before the learner starts it, no new assignment notification is triggered.

## Related pages

- [[test-coverage]]
- [[push-notifications]]
- [[learners-list-analytics]]
