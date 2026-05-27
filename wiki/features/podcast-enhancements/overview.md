# Feature: Podcast Enhancements

**Summary**: Enhancements to the core podcast feature covering the creation flow, audio type selection, asset management, error handling, notifications, and source asset viewer.

**Sources**: `raw/9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf`, `raw/Podcast Enhancements - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does
Podcast Enhancements builds on the core podcast creation experience by adding the ability to configure audio type (Conversational or Monologue), manage source assets, set podcast duration, and view generation errors with clear recovery paths. It also introduces push notifications and email notifications for generation success/failure, and a source asset viewer with AI summaries.

## Who uses it
- **Admins and content publishers**: who create and manage podcasts.
- **Learners**: who consume podcasts and see the source assets viewer.

## How it works
The creation flow and all enhancement behaviours are documented in detail in [[podcasts]]. Acceptance criteria are in [[ac]].

Key areas covered by the enhancements:
- Assets must be uploaded before podcast generation can begin
- Audio type: Conversational (two voices) or Monologue (single voice); Conversational is the default
- Maximum 5 source assets per podcast
- Three error scenarios: unsupported asset type, generation failure, and duration/type validation failure
- Push, toast, and email notifications on generation success or failure
- Source assets are viewable from the podcast with an AI-generated summary per asset
- Duration is set using a duration picker (short, medium, long)

## Things to know
- The enhancements PDF (`9230ccf6`) was ingested as part of the podcasts feature. All ACs from that source are in [[podcasts]] and [[ac]]. (source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)
- The test coverage CSV (`Podcast Enhancements - Sheet1.csv`) with 42 test cases is documented in [[test-coverage]].

## Related pages
- [[ac]]
- [[test-coverage]]
- [[podcasts]]
- [[podcast-reports]]
- [[microlearning-podcast]]
