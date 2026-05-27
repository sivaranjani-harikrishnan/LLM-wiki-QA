# Test Coverage: Podcast and Simulation in Courses

**Summary**: 49 test cases covering Pick from Studio panel, podcast and simulation library, search, adding/rearranging/deleting units, section behaviour, and post-addition change propagation.

**Sources**: `Simulation and Podcast in Courses - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Course structure with Add Unit (TC0001–TC0006)
- TC0001: Create a course
- TC0002: Course structure shows "Add Unit" button in primary colour
- TC0003: Click Add Unit → slider with Lessons, Assessments, Pick from Studio
- TC0004: Click Lessons → add asset slider (Streams & Collections, Personal Drive, URL, Cleverstory)
- TC0005: Add lessons within and outside sections
- TC0006: Add assessments within and outside sections

### Pick from Studio — Podcasts (TC0007–TC0026)
- TC0007: Pick from Studio shows published podcasts + simulations; draft/deleted excluded; search works; multiple selection; read-only after add
- TC0008: Podcast metadata in slider: banner, duration, last updated date
- TC0009: Hover selected podcast → [x] to remove from selection
- TC0010: Deleted podcast not listed; if already in course, removed from all courses on deletion
- TC0011: Podcast UI in course structure: name, thumbnail, duration, type, Details, Transcript, Play, fwd/rws, volume, speed
- TC0012: Cannot edit podcast name/banner/skill from course structure
- TC0013: Edits to podcast in Studio after adding to course do NOT reflect in course
- TC0014: Deleted podcast removed from course; no longer available
- TC0015: Same podcast addable to multiple courses; deleting removes from all
- TC0016: Cancel in Pick from Studio: no items added
- TC0017: Delete unit → removes that unit from course
- TC0018: Delete section → removes entire section
- TC0019: Rearrange podcast unit via drag icon
- TC0020: Rearrange section via up/down arrows
- TC0021–TC0026: Search functionality (published, unpublished, special chars, case, partial, deleted, inapplicable content)

### Pick from Studio — Simulations (TC0030–TC0049)
- TC0030: Add published simulations from Pick from Studio
- TC0031: Cannot edit simulation in course structure
- TC0032: Edits to simulation in Studio do NOT reflect in course
- TC0033: Deleted simulation removed from course and all courses
- TC0034: Same simulation addable to multiple courses
- TC0035: Delete simulation unit from course
- TC0036: Delete section with simulation
- TC0037: Rearrange simulation unit
- TC0038: Rearrange simulation within sections
- TC0039–TC0044: Search functionality for simulations (same rules as podcasts)
- TC0045: Add multiple simulations within sections
- TC0046: Move simulation from section to outside
- TC0047: Sections support all types: lessons, assessments, podcasts, simulations
- TC0048: Save and publish from all screens
- TC0049: Pick from Studio scroll with many items; tabs switch correctly

---

## Related pages

- [[overview]]
- [[courses]]
- [[podcasts]]
- [[simulations]]
