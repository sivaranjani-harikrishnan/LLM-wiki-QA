# Feature: Podcasts

**Summary**: Podcasts are AI-generated audio content created from admin-uploaded source assets, available in three audio types and assignable to learners for async listening.

**Sources**: `Podcast Enhancements - Sheet1.csv`, `Podcast - New type  - Sheet1.csv`, `Podcast Reports - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Admins upload up to 5 source documents and the system generates an audio podcast of configurable duration and style. Learners listen to the podcast in their My Space or through Explore. Admins can track completion, listen time, and learner engagement.

## Who uses it

- **Admins / Content Publishers**: Create, edit, publish, assign podcasts
- **Learners**: Listen to assigned or self-enrolled podcasts

## How it works

### Creating a podcast
1. Click "Create Podcast" in Studio → empty podcast created with "Untitled podcast" name and empty banner
2. Default audio type: Conversational
3. Add assets: up to 5 from Streams & Collections, Local Device, or URL
4. Supported formats: PDF, PPT, DOC, URL
5. Unsupported: ZIP, Excel, images, videos, SCORM, HTML
6. After selecting assets → click Confirm → opens duration + audio type selection screen
7. Choose duration: 5 / 10 / 15 / 20 / 25 / 30 min or "I'm Flexible"
8. Choose audio type: Conversational / Monologue / Narrative
9. Click Generate

### Generation stages
1. Topics loading (skeletal loading; help text: "generating topics... This may take a few minutes. Feel free to go back—we'll notify you once it's ready.")
2. Details tab auto-selected; topics listed on completion
3. Transcript tab unlocked after transcript generation
4. Audio loader shown at bottom after transcript
5. Audio player shown on completion

Navigation away during generation does NOT stop it.

### Audio types
- **Conversational**: Two voices in dialogue (default for all existing podcasts)
- **Monologue**: Single voice
- **Narrative**: Single smooth voice — no fillers (hmm, hm hm), no random voices (ya, right), no awkward pauses, no self-corrections

### Naming and description
- Podcast name: up to 200 characters; any alphanumeric + special characters
- Description: up to 1000 characters; unlocked after generation; required for publishing
- Skills: required for publishing

### Banner
- Sources: Pexels, Paperflite default, Local upload (max 10 MB)
- Images: cropping available after selection
- Videos: no crop option (position option not available for video either)

### Edit screen
- Admin can: add/remove assets, change audio type, change duration, change voice
- SEEK: AI assistant in edit screen accepts natural language prompts (e.g., "Change duration to 10 mins", "change type to Narrative")
- Editing after assignment: changes propagate to learners (transcript and audio update)

### Deleting
- Deleted podcast is removed from all courses it was embedded in
- Deleted podcast no longer appears in Pick from Studio library

### Error handling during generation
- Failed assets show error screen: "transcript generation failed" with sub-text "this usually happens when the assets don't have enough content in them"
- Each failed asset shows Retry and Upload new assets options
- Retry retriggers generation for failed asset
- Admin can remove failed assets and add new ones, then regenerate

### Asset limit enforcement
- 5-asset limit applies at both creation and editing stages
- Error shown if >5 assets attempted

## Learner experience

- Conversational: two voices
- Monologue: one voice
- Narrative: smooth single voice, no fillers (verified on mobile iOS and Android)
- Narrative podcast shows "Narrative" pill in Explore tiles, My Courses tiles, and inside playback view (for both admin and learner)
- Replay does not increment completion count (completion recorded once)
- All edits made by admin after assignment propagate to learner (including tone, type, duration, asset changes)
- New version of source asset uploaded in Paperflite → transcript and audio update for both admin and learner

## Enrolling

- Admin assigns learners directly from Studio
- Learners can self-enrol from Explore page

## Related pages

- [[test-coverage]]
- [[podcast-reports]]
- [[microlearning-podcast]]
- [[podcast-simulation-in-courses]]
