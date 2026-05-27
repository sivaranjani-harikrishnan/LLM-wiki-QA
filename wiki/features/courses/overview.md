# Feature: Courses

**Summary**: Courses are structured learning modules containing lessons, assessments, podcasts, and simulations; learners must complete all elements to finish a course.

**Sources**: `Sections index within Courses - Sheet1 (2).csv`, `Simulation and Podcast in Courses - Sheet1.csv`, `Course Reports - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## What it does

Courses give admins a structured way to deliver multi-piece learning programs. A course can mix lessons (content files or URLs), assessments (quizzes), podcasts, and simulations — organised optionally with Sections.

## Who uses it

- **Admins / Content Publishers**: Create, publish, and assign courses
- **Learners**: Complete courses element-by-element; view progress in My Space

## How it works

### Creating a course
1. Navigate to Manage Courses → Create New Course → empty course created
2. Click "Create course structure"
3. Available buttons: Add Unit (Lessons / Assessments / Pick from Studio), Add new Section
4. "Add Unit" slider has three options: Lessons, Assessments, Pick from Studio

### Unit types

#### Lessons
From: Streams & Collections, Personal Drive, URL, Cleverstory (if integration enabled)

#### Assessments
Quiz-style questions with a pass threshold (admin-configured). Can be inside or outside sections.

#### Pick from Studio (Podcasts and Simulations)
- Shows library of all published podcasts and simulations
- Draft podcasts/simulations are NOT shown
- Deleted podcasts/simulations do NOT appear
- Search works case-insensitively, supports partial matches and special characters
- Multiple items can be added at once

### Sections
- Optional grouping layer for lessons and assessments (podcasts and simulations can also be inside sections)
- Section defaults to name "Untitled section [number]"
- Name and description fields: optional
- Cannot publish with empty sections
- Empty section = one that has no content or from which all content has been removed
- Warning when deleting a section with content: "deleting the section will also delete lessons with it — consider relocating them using drag/drop feature into the course if you want to keep them"
- Deleting an empty section: no confirmation needed
- Rearranging sections: up/down arrows (first section shows only down arrow; last section shows only up arrow; middle sections show both)
- Sections are NOT shown in the mobile app
- Sections ARE shown in Demo URLs
- Progress bar visible in learner view under Course Structure heading (only when course has >1 element)

### Learner view (sections)
- Sections are collapsible/expandable
- Section card shows: section name, description, number of lessons, number of assessments
- Content count shown as X/Y (completed/total)
- Progress bar fill in account primary colour
- Completed element: tick mark (✓); in-progress: percentage bar
- Clicking a section navigates to first content of that section

### Learner completion rules
- Must view all lessons AND pass all assessments (inside and outside sections) to end the course
- Progress bar denominator updates when admin adds or removes elements

### Podcast/Simulation in courses — important behaviours
- Edits made to a podcast/simulation in Studio after adding it to a course do NOT reflect in the course
- If a podcast/simulation is deleted from Studio, it is removed from all courses it was embedded in
- Same podcast/simulation can be added to multiple courses simultaneously
- Admin cannot edit podcast/simulation properties from within the course structure (name, banner, skills are read-only in course context)

### Saving and publishing
- Save button available from course page and course structure screen
- Publish makes course available to assigned learners
- Discard reverts to last published version

## Score and pass rules

- Pass threshold set by admin on the assessment level
- Changing threshold only applies to new completions
- All completions (even failed attempts) count in avg score calculation

## Mobile

- Courses available in mobile HeySales app
- Sections not displayed in mobile app

## Related pages

- [[course-reports]]
- [[sections-in-courses]]
- [[podcast-simulation-in-courses]]
- [[learners-list-analytics]]
- [[learning-types]]
