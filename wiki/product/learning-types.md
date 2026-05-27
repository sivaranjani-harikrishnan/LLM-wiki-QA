# Product: Learning Types

**Summary**: HeySales has three primary learning types — Courses, Podcasts, and Simulations — each with distinct creation flows, learner experiences, and reporting metrics.

**Sources**: Multiple ACs and test case CSVs from `raw/`

**Last updated**: 2026-05-25

---

## Courses

Courses are structured modules created in Manage Courses. They can contain:
- **Lessons**: Files (PDF, PPT, DOC, video) or URLs from Streams & Collections, Personal Drive, or URL
- **Assessments**: Quiz-style questions with a pass threshold
- **Sections**: Optional grouping layer for lessons and assessments
- **Podcasts** (via Pick from Studio): published podcasts embedded as units
- **Simulations** (via Pick from Studio): published simulations embedded as units

Learners must view all lessons and pass all assessments to end a course.

**Completion**: tracked per element. Progress bar shows X/Y elements completed.
**Score**: average of all assessment scores across all attempts.
**Pass threshold**: set by admin; changing threshold only applies to new completions.

Sections: optional grouping. Empty sections block publishing. Sections are not shown in the mobile app but are shown in Demo URLs.

## Podcasts

Podcasts are AI-generated audio created in Studio. Admin uploads 1–5 source assets (PDF, PPT, DOC, URL). Unsupported formats: ZIP, Excel, images, videos, SCORM, HTML.

Audio types:
- **Conversational**: two voices in dialogue
- **Monologue**: single voice
- **Narrative**: single smooth voice, no fillers, no random voices, no pauses

Duration: selectable 5/10/15/20/25/30 min or "I'm Flexible" (no strict length, optimised for content).

Generation stages: topics loading → Details tab → transcript generated → transcript tab unlocked → audio loader → audio player.

Navigation away during generation does not stop it.

Learners can self-enrol via Explore (if admin published without assigning) or are assigned by admin.

Edits made in Studio after assignment propagate to learners (tone, type, duration, asset changes update transcript and audio).

## Simulations

Simulations are AI role-play calls where the learner talks to an AI prospect. Types: Cold Call, Discovery, Follow-up, Elevator Pitch.

Admins configure:
- Call type / scenario
- Company profile, buyer profile, buyer needs
- Scorecard (defaults to account's default scorecard)
- Difficulty level
- Skills in focus
- Assigned learners

Learners take the call via browser (camera + mic for video mode, or audio-only). Reports are generated per attempt using the tagged scorecard.

**Elevator Pitch**: A simulation variant where the learner delivers a timed monologue (no AI prospect). Duration: 30 sec / 1 min / 1 min 30 sec / 2 min. Format: Video (default) or Audio. No buyer in the scenario.

**Scoring**: Out of 10 per parameter. Overall score calculated by scorecard. Calls under 2 minutes are marked as NA.

## Microlearning (Let's Learn)

Every user can generate a private AI article from their own prompts + assets (up to 5: PDF, DOC, PPT, URL, CS Storyboards). The article is private — no admin can see it. Users can generate a private audio podcast from the article. History pane shows all modification prompts; user can switch between versions.

## Comparison table

| Feature | Course | Podcast | Simulation | Microlearning |
|---|---|---|---|---|
| Created by | Admin/CP | Admin/CP | Admin/CP | Any user (private) |
| Assigned by | Admin/CP | Admin/CP | Admin/CP | Self |
| Learner interaction | View + quiz | Listen | Role-play call | Read/listen |
| Score | Assessment % | N/A (pass by default) | Scorecard (out of 10) | N/A |
| Reports visible to admin | Yes | Yes | Yes | No (private) |
| Retakes | Yes | Yes (replay) | Yes | N/A |
| Mobile app support | Yes | Yes | No | N/A |

## Related pages

- [[heysales-overview]]
- [[courses]]
- [[podcasts]]
- [[simulations]]
- [[elevator-pitch]]
- [[microlearning]]
- [[custom-scorecards]]
