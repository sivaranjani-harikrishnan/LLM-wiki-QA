# Feature: Podcast and Simulation in Courses

**Summary**: Published podcasts and simulations can be embedded as learning units within courses, accessible via "Pick from Studio" in the course structure builder.

**Sources**: `Simulation and Podcast in Courses - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Courses can include published podcasts and simulations as standalone units, mixing them with lessons and assessments. This lets admins build multi-format learning programs in a single course.

## Who uses it

- **Admins / Content Publishers**: Add podcasts and simulations to courses via Pick from Studio
- **Learners**: Complete podcasts and simulations as part of a course

## How it works

### "Add Unit" flow
1. Click "Add Unit" in course structure → slider with 3 options: Lessons, Assessments, Pick from Studio
2. "Pick from Studio" opens a library panel with tabs: Podcast | Simulation
3. Default tab: Podcast (showing all published podcasts)
4. Switching to Simulation shows all published simulations

### Library panel
- Only published items shown (drafts and deleted items not listed)
- Search: supports partial matches, case-insensitive, special characters, no-space variations
- Selecting multiple items → all listed in a new pane before confirming
- Hovering a selected item shows [x] to remove it from the selection
- Cancel: no items added to course
- Add: all selected items added as separate units

### After adding to course

**Podcast unit UI** (creator view):
- Podcast name, thumbnail, duration, type, Details, Transcript, Play button, forward/reverse buttons, volume button, playback speed button

**Simulation unit UI** (creator view):
- Same read-only view; no editing allowed in course context

### Read-only in course context
- Admins **cannot** edit podcast/simulation name, banner, or skills from within the course structure
- These properties are read-only in the course context

### Impact of post-addition edits
- Editing the podcast/simulation in Studio after adding to course: changes **do NOT** reflect in the course
- Deleting the podcast/simulation from Studio: removes it from **all** courses it was embedded in
- Same podcast/simulation can be added to multiple courses simultaneously

### Rearranging
- Podcast/simulation units can be dragged to reorder within the course
- Can be moved inside or outside sections
- Sections can be reordered using up/down arrow icons

### Deleting
- Delete unit icon removes that specific unit from the course
- Delete section icon removes the entire section (including all units in it)

### Saving and publishing
- Save available from course page and course structure screen
- Publish available from both screens

## Things to know

- Only published podcasts/simulations appear in Pick from Studio (source: `Simulation and Podcast in Courses - Sheet1.csv` TC0007)
- Draft podcasts/simulations are specifically excluded (source: TC0007)
- Deleted podcasts/simulations automatically removed from all courses (source: TC0010, TC0033)
- Edits to podcast in Studio do NOT flow into course (source: TC0013)
- Edits to simulation in Studio do NOT flow into course (source: TC0032)
- Podcast banner: image and video banners both render in course structure (source: TC0011)
- Sections support all learning types: lessons, assessments, podcasts, simulations (source: TC0047)

## Related pages

- [[test-coverage]]
- [[courses]]
- [[podcasts]]
- [[simulations]]
- [[sections-in-courses]]
