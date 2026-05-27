# Acceptance Criteria: Due Date and Reminder Notifications

**Summary**: Defines how due dates are set for learnings, how overdue status is displayed, and when reminder notifications are sent.

**Sources**: `raw/7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf`

**Last updated**: 2026-05-25

---

## Due Date Setting ACs

## AC-DD-01: Due dates apply to assignments only

GIVEN a learning has a due date configured
WHEN determining which learners the due date applies to
THEN the due date applies only to assigned learners — not to self-enrolled learners

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-02: Due dates are optional

GIVEN a manager is assigning a learning
WHEN they configure the assignment
THEN setting a due date is optional, not mandatory

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-03: Specific due date type

GIVEN a manager is setting a due date
WHEN they choose a specific due date
THEN they pick a calendar date via a date picker; all assigned learners share this fixed deadline

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-04: Relative due date type

GIVEN a manager is setting a due date
WHEN they choose a relative due date
THEN they set a number of days from the assignment date; each learner's deadline is calculated from their individual assignment date

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

---

## Manager — Learners List ACs

## AC-DD-05: Manager can see overdue learners

GIVEN a manager views the learners list for a learning
WHEN the due date has passed
THEN learners who have not started or are in progress past the due date are clearly marked as overdue

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-06: Manager can see late completions

GIVEN a manager views the learners list for a learning
WHEN a learner completed the learning after the due date
THEN that learner is marked as having completed late (first completion was post due date)

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-07: Due date visible for in-progress and not-started learners

GIVEN a manager views the learners list
WHEN a learner is in-progress or not-started
THEN the due date for that learner is visible in the list

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

---

## Learner — My Space ACs

## AC-DD-08: Overdue section in My Space

GIVEN a learner has one or more overdue learnings
WHEN they view My Space
THEN a dedicated section calls out their overdue learnings

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-09: Due date visible inside learning

GIVEN a learner enters a learning in My Space that has a due date
WHEN they view the learning
THEN the due date is displayed inside the learning

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-10: Days-remaining copy alongside start/resume button

GIVEN a learner views a learning with a due date
WHEN they see the start/resume button
THEN the number of days remaining is also displayed with one of three states: "due in X days", "due today", or "overdue by X days"

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-11: Due date hidden after first completion

GIVEN a learner has completed a learning at least once
WHEN they view that learning
THEN the due date is no longer shown (due date is hidden for completed learners)

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

---

## UI Cards ACs

## AC-DD-12: Due date as metadata on learning cards

GIVEN a learning has a due date and is displayed as a card across the platform
WHEN the card is rendered
THEN the due date is attached as metadata on the card

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-13: Due status on cards

GIVEN a learning card is displayed
WHEN the due date is today or has passed
THEN the card shows "due today" or "overdue by X days" as appropriate

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

---

## Reminder Notification ACs

## AC-DD-14: Assignment notification includes due date

GIVEN a learner is assigned a learning that has a due date
WHEN the assignment notification is sent
THEN the notification also indicates the due date

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-15: Midpoint notification (50% of assignment-to-due window)

GIVEN a learner has not completed an assigned learning
WHEN 50% of the time between assignment date and due date has elapsed
THEN a reminder notification is sent (rounded down to nearest whole day for odd-day periods)

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-16: 7-day-before notification (conditional)

GIVEN a learner has not completed an assigned learning
WHEN 7 days remain before the due date
THEN a reminder notification is sent only if the assignment-to-due window was more than 30 days

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-17: 3-day-before notification (conditional)

GIVEN a learner has not completed an assigned learning
WHEN 3 days remain before the due date
THEN a reminder notification is sent only if the assignment-to-due window was more than 10 days

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-18: 1-day-before notification

GIVEN a learner has not completed an assigned learning
WHEN 1 day remains before the due date
THEN a reminder notification is sent; if the total assignment-to-due window is only 2 days, only this notification fires

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-19: Updated assignment triggers notification

GIVEN an existing assignment is updated (due date added or changed)
WHEN the update is saved
THEN a notification email is triggered for in-progress and not-started learners; previously overridden settings are preserved for re-assignments

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

## AC-DD-20: Notification template

GIVEN reminder notifications are sent
WHEN the email is composed
THEN it uses the same template/design as the existing assignment notification, with only copy changes

(source: 7d2d128b-8896-48dc-aa06-6dae1c3bd0ef_Due_date_and_reminder_notifications.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[courses]]
- [[push-notifications]]
