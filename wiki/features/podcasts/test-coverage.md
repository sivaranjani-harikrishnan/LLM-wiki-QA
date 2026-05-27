# Test Coverage: Podcasts

**Summary**: 42 TCs from Podcast Enhancements and 56 TCs from Podcast - New Type covering creation, audio types (including Narrative), editing, learner views, and error handling.

**Sources**: `Podcast Enhancements - Sheet1.csv`, `Podcast - New type  - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Creation basics (TC0001–TC0008)
- TC0001: Create podcast button creates empty podcast named "Untitled podcast" with empty banner
- TC0002: Default audio type is Conversational
- TC0003: Banner upload from Pexels, Paperflite default, and local (images and video)
- TC0004: Image banner cropping available; video banner has no crop option
- TC0005: Image banner positioning available; video has no position option
- TC0006: Naming field accepts alphanumeric and special characters
- TC0007: Naming field limit: 200 characters
- TC0008: Empty podcast UI: "You need to add assets to kick off your podcast journey!" help text with sub-text, Add Asset, Add Skill, Add Learner, Cancel & Exit buttons

### Asset management (TC0009–TC0015)
- TC0009: Add Asset button opens the add asset slider
- TC0010: Assets addable from Streams & Collections, Local Device, and URL
- TC0011: Supported assets (PDF, PPT, URL) can be selected and confirmed
- TC0012: Unsupported assets (ZIP, Excel, images, videos, SCORM, HTML) cannot be chosen from Streams & Collections
- TC0013: Adding both supported and unsupported from local → error on Confirm
- TC0014: After removing unsupported assets → Confirm takes admin to duration/audio type selection
- TC0026: More than 5 assets → error message

### Generation flow (TC0015–TC0017)
- TC0015: After Confirm, screen shows: listed assets with thumbnails, count, exclamatory help text, duration picker (default "I'm flexible"), audio type selector (default Conversational)
- TC0016: Click Generate → skeletal loading for topics → Details tab → transcript tab unlocked → audio loader → audio player
- TC0017: Duration selector options: 5, 10, 15, 20, 25, 30, I'm flexible

### Audio types (TC0018–TC0020, TC0045–TC0051)
- TC0018: Monologue audio type generates single-voice podcast
- TC0019: Narrative audio type selectable; generates Narrative podcast
- TC0020: Narrative audio quality: no fillers (hmm, hm hm), no random voices (ya, right), no awkward pauses, smooth single consistent voice
- TC0045: Conversational in learner view uses 2 voices
- TC0046: Monologue in learner view uses 1 voice
- TC0047: Narrative in learner view is smooth without fillers
- TC0048: Narrative verified on mobile (iOS and Android)
- TC0049: Narrative pill shown in Explore tiles
- TC0050: Narrative pill shown in My Courses tiles
- TC0051: Narrative pill shown inside playback view for both admin and learner

### Description and generation (TC0021–TC0025)
- TC0021: Description field accepts any alphanumeric + special characters
- TC0022: Description field limit: 1000 characters
- TC0023: Help text "generating topics... This may take a few minutes. Feel free to go back—we'll notify you once it's ready." shown during generation
- TC0024: Navigating to other modules during generation does NOT stop generation
- TC0025: Generated podcast shows banner, duration, audio type, Details, Transcript, topics list, audio controls, Skills, learner list, Completion card, Total time spent card, Avg time spent card

### Edit screen (TC0027–TC0034)
- TC0027: Edit in studio button → edit screen
- TC0028: Edit screen allows: add/remove assets, change audio type, duration, voice
- TC0029–TC0032: Cross-type editing (Conversational↔Narrative, Monologue↔Narrative, Narrative↔Conversational, Narrative↔Monologue)
- TC0033–TC0034: SEEK in edit screen — natural language prompts work for duration and audio type changes

### Publishing and error handling (TC0035–TC0041)
- TC0035: Cannot publish without required fields (Skills, Description); errors shown
- TC0036: Congratulations screen shown after publishing
- TC0037: Failed asset shows error screen with list of failed assets
- TC0038: Error screen shows "transcript generation failed" + "this usually happens when the assets don't have enough content in them..."
- TC0039: Retry retriggers generation
- TC0040: Upload new assets → remove failed, add new, regenerate
- TC0041: Same error handling during edit as during creation
- TC0042: 5-asset limit enforced during editing; error shown at >5

### Learner and assignment (TC0043–TC0056)
- TC0043: Assign podcast to individual learners
- TC0044: Assign podcast to user groups
- TC0052: Edits after assignment propagate: tone, type, duration, asset changes all update for learner
- TC0053: Edit propagation verified on mobile (iOS + Android)
- TC0054: New version of source asset uploaded → transcript + audio update for both admin and learner
- TC0055: All existing podcasts have Conversational type set
- TC0056: Learner can self-enrol from Explore page

---

## Related pages

- [[overview]]
- [[podcast-reports]]
- [[podcast-simulation-in-courses]]
