# Test Coverage: Sections in Courses

**Summary**: 49 test cases covering section creation, naming, content management, rearranging, deletion, learner view, progress bar, and platform differences.

**Sources**: `Sections index within Courses - Sheet1 (2).csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Creation (TC0001–TC0005)
- TC0001: Create a course
- TC0002: Course structure shows "Add new section" button in primary colour alongside Add lesson and Add assessment
- TC0003: Clicking Add new section creates "Untitled section [number]"; hover under section to add more
- TC0004: Section name field: any alphanumeric + special characters
- TC0005: Long name truncated; on-hover tooltip shown

### Naming and description (TC0006–TC0008)
- TC0006: Description field accepts any alphanumeric + special characters
- TC0007: Character limit enforced for description; scrollable within field
- TC0008: Clicking section name places cursor; user can rename

### Content management (TC0009–TC0016)
- TC0009: After adding section, only Add lesson + Add assessment shown inside (no "Add section" inside)
- TC0010: Unlimited lessons and assessments per section; scroll works
- TC0011: Hovering under existing section shows "Add section" icon; clicking creates new section
- TC0012: Unlimited sections in a course; scroll works
- TC0013: Empty section name → error on publish
- TC0014: Header icons (Section, Lesson, Assessment) add respective elements outside sections
- TC0015: Hover "Add new" inside section → Lessons or Assessment options shown
- TC0016: Adding lessons/assessments outside sections via header icons

### Rearranging (TC0017–TC0020)
- TC0017: Drag and drop lessons/assessments within a section (no UI glitch)
- TC0018: Drag and drop lessons/assessments across sections (no UI glitch)
- TC0019: Section arrows: first section = down only; last section = up only; middle = both; clicking reorders
- TC0020: Drag lessons/assessments from section to course structure level (outside section)

### Deletion (TC0021–TC0022)
- TC0021: Delete section with content → confirmation slider with warning text
- TC0022: Delete empty section → no confirmation needed

### Empty section state (TC0023–TC0024)
- TC0023: Removing all content from a section → empty; cannot publish
- TC0024: Adding content back to empty section removes error

### Section validation (TC0025–TC0030)
- TC0025: Discard changes after publishing reverts to last published version
- TC0026: Cannot publish course with empty sections
- TC0027: Name and description both optional
- TC0028: Course without sections publishable (lessons + assessments only at course level)
- TC0029: Course with only sections (lessons/assessments inside sections) publishable
- TC0030: Course with mixed (sections + top-level content) publishable

### Learner view (TC0031–TC0040)
- TC0031: Learner sees all sections, lessons, assessments in creator-specified order
- TC0032: Sections expand/collapse with arrow icons; scroll works within section
- TC0033: Section shows name, description, lesson count, assessment count
- TC0034: Content count shown as X/Y (completed/total)
- TC0035: Completed element shows ✓; in-progress shows percentage bar
- TC0036: Scroll works in course structure, within sections, and section descriptions
- TC0037: Must complete all elements (in and out of sections) to end course
- TC0038: Clicking section name navigates to first content of that section
- TC0039: Score calculation same with or without sections
- TC0040: Sections NOT shown in mobile app

### Platform differences (TC0040–TC0041)
- TC0040: Sections NOT in mobile app
- TC0041: Sections shown in Demo URL

### Progress bar (TC0042–TC0049)
- TC0042: Progress bar shown under Course Structure heading for learners
- TC0043: Progress bar fill based on lessons + assessments completed
- TC0044: Progress bar fill in account primary colour
- TC0045: Progress fraction shown next to bar (0/X for fresh course)
- TC0046: Numerator updates as learner completes elements
- TC0047: Denominator updates when admin adds/removes elements
- TC0048: Progress bar shown only when course has >1 element
- TC0049: Progress bar works correctly for courses with sections, without sections, and mixed

---

## Related pages

- [[overview]]
- [[courses]]
