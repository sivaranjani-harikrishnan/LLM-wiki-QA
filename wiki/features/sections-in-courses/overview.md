# Feature: Sections in Courses

**Summary**: Sections are an optional grouping layer within courses that allow admins to organise lessons and assessments into named groups; learners see sections as collapsible panels with progress tracking.

**Sources**: `Sections index within Courses - Sheet1 (2).csv`

**Last updated**: 2026-05-25

---

## What it does

Sections let admins group related lessons and assessments together within a course. Sections are optional — courses can also contain ungrouped content, or a mix of both.

## Who uses it

- **Admins / Content Publishers**: Create, name, and organise sections
- **Learners**: Navigate course content through collapsible section panels

## How it works

### Creating sections
- "Add new section" button creates a section named "Untitled section [number]"
- Additional sections can be added by hovering under any existing section and clicking the Add Section icon
- Also available from the header CTAs (icons next to Course Structure heading for Section, Lesson, Assessment)
- Name field: optional, any alphanumeric + special characters; long names truncated with hover tooltip
- Description field: optional; character limit enforced; scrollable within field

### Content within sections
- Any number of lessons and assessments can be added within a section
- Podcasts and simulations (via Pick from Studio) can also be added inside sections
- After a section is created, the "Add new section" button is hidden inside the section; only "Add lesson" and "Add assessment" are shown
- Hover "Add new" button inside section to choose Lessons or Assessment

### Adding content outside sections
- Lessons and assessments can exist outside of sections (at the course structure level)
- Icons next to Course Structure heading: Section icon, Lesson icon, Assessment icon — each adds the respective element outside all sections

### Rearranging
- Lessons/assessments can be dragged within a section
- Lessons/assessments can be dragged across sections
- Lessons/assessments can be dragged from a section to outside the section
- Sections themselves are reordered using up/down arrows (first section: only down; last section: only up; middle sections: both)

### Deletion
- Empty section: deleted without confirmation
- Section with content: confirmation slider shown with warning "deleting the section will also delete lessons with it — consider relocating them using drag/drop feature into the course if you want to keep them"

### Empty section validation
- Cannot publish with empty sections
- If all content is removed from a section (by delete or drag-out), it becomes empty and blocks publishing
- Adding content back removes the empty error

### Progress logic
- Progress bar denominator = total lessons + assessments across all sections and top-level
- Progress bar updates when admin adds or removes elements
- Progress bar shown only when course has >1 element

### Discard changes
- After publishing, edits to sections → Discard returns course to last published version

## Learner view

- Sections displayed as collapsible panels (expand/collapse with arrow icons)
- Each section shows: name, description, lesson count, assessment count, content progress (X/Y completed)
- Progress bar fill in account primary colour
- Completed element: tick mark (✓); in-progress: percentage bar
- Clicking a section name navigates to first content of that section
- Overall course progress bar shown under Course Structure heading
- Scroll works within sections and descriptions

## Platform differences

- **Mobile app**: Sections NOT displayed; learners see flat content list
- **Demo URL**: Sections ARE displayed (same as web)
- **Web**: Full sections UI

## Courses without sections

- Courses can be published without any sections (only lessons + assessments at course level)
- Both models are valid: all-sections, no-sections, or mixed

## Score calculation

- Existing score calculation logic applies regardless of whether course uses sections

## Related pages

- [[test-coverage]]
- [[courses]]
- [[podcast-simulation-in-courses]]
- [[course-reports]]
