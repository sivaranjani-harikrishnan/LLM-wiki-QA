# Acceptance Criteria: Podcasts

**Summary**: Defines how podcasts are created, what types exist, how errors are handled during generation, what notifications are sent on success, and how source assets are viewed while listening.

**Sources**: `raw/9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf`, `raw/67743586-7ef0-4c47-97f1-4f6378cf9a91_Error_Screen_-_Podcast_Generation.pdf`, `raw/ca48016d-9832-4701-be10-41a48efed75b_Podcast_Generation_Success_-_Notifications.pdf`, `raw/cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf`

**Last updated**: 2026-05-25

---

## Podcast Creation ACs

## AC-PC-01: New creation flow — upload first

GIVEN a user initiates podcast creation
WHEN they start the creation flow
THEN they upload source assets first, then configure duration and audio experience settings

(source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)

## AC-PC-02: Podcast types — Monologue and Conversational

GIVEN a user is creating a podcast
WHEN they select the podcast type
THEN they can choose between Monologue (single host voice) and Conversational (dialogue between two voices)

(source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)

## AC-PC-03: Asset limit of 5

GIVEN a user is uploading source assets for a podcast
WHEN they add assets
THEN a maximum of 5 assets are allowed per podcast

(source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)

## AC-PC-04: Link assets supported

GIVEN a user is uploading source assets
WHEN they add assets
THEN linking assets (not just file uploads) is a supported input method

(source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)

## AC-PC-05: Details and Transcript tabs

GIVEN a podcast has been created
WHEN a user views the podcast
THEN they see a Details tab (metadata) and a Transcript tab (auto-generated transcript)

(source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)

## AC-PC-06: Edit Studio changes

GIVEN a podcast is being edited
WHEN a user accesses the Edit Studio
THEN the updated Edit Studio interface is presented with the enhanced editing capabilities

(source: 9230ccf6-a387-47a1-aa35-99bfb6a88cc8_Podcast_Enhancements.pdf)

---

## Error Handling ACs

## AC-PE-01: Single asset failure — Replace only

GIVEN a podcast generation was attempted with a single source asset
WHEN that asset fails during generation
THEN the user sees an error screen with only a "Replace" option (no "Continue without" option, since there are no other assets)

(source: 67743586-7ef0-4c47-97f1-4f6378cf9a91_Error_Screen_-_Podcast_Generation.pdf)

## AC-PE-02: Mixed batch failure — Continue or Replace

GIVEN a podcast generation was attempted with multiple source assets
WHEN some assets fail and some succeed
THEN the user sees an error screen with two options: "Continue with N assets" (skip the failed ones) or "Replace Failed" (swap out the failed assets)

(source: 67743586-7ef0-4c47-97f1-4f6378cf9a91_Error_Screen_-_Podcast_Generation.pdf)

## AC-PE-03: Complete failure — Upload Different Files

GIVEN a podcast generation was attempted
WHEN all source assets fail
THEN the user sees an error screen with only an "Upload Different Files" option

(source: 67743586-7ef0-4c47-97f1-4f6378cf9a91_Error_Screen_-_Podcast_Generation.pdf)

---

## Success Notification ACs

## AC-PN-01: Browser push notification

GIVEN a podcast generation completes successfully
WHEN the browser has permission to send notifications
THEN a browser push notification is sent; clicking it navigates the user to the podcast in the studio

(source: ca48016d-9832-4701-be10-41a48efed75b_Podcast_Generation_Success_-_Notifications.pdf)

## AC-PN-02: In-app toast notification

GIVEN a podcast generation completes successfully
WHEN the user is active in the web app
THEN a toast notification appears in the bottom-right corner with a 3-step copy update and a "Listen now" CTA; the toast is dismissible and is hidden when the user is already on the podcast screen

(source: ca48016d-9832-4701-be10-41a48efed75b_Podcast_Generation_Success_-_Notifications.pdf)

## AC-PN-03: Email notification

GIVEN a podcast generation completes successfully
WHEN the system sends the success notification
THEN an email is sent to the creator; the email's CTA links to the podcast in the web app

(source: ca48016d-9832-4701-be10-41a48efed75b_Podcast_Generation_Success_-_Notifications.pdf)

## AC-PN-04: Three trigger points

GIVEN podcast generation can complete at different times
WHEN the generation finishes
THEN all three notification channels (push, toast, email) are triggered at podcast generation completion

(source: ca48016d-9832-4701-be10-41a48efed75b_Podcast_Generation_Success_-_Notifications.pdf)

---

## Source Asset Viewer ACs

## AC-SA-01: Source assets listed in right panel

GIVEN a user is listening to a podcast
WHEN the podcast is playing
THEN the source assets used to create the podcast are listed in the right panel of the player

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

## AC-SA-02: Click asset to open viewer

GIVEN source assets are listed in the right panel
WHEN a user clicks on an asset
THEN that asset opens in a viewer inline (without leaving the podcast player)

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

## AC-SA-03: Switch between multiple assets without interrupting playback

GIVEN multiple source assets are listed
WHEN the user switches from viewing one asset to another
THEN podcast audio playback is not interrupted

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

## AC-SA-04: Transcript coexistence

GIVEN the source asset viewer is visible
WHEN the podcast transcript is also available
THEN both the transcript and the asset viewer can be displayed simultaneously without conflict

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

## AC-SA-05: Audio controls remain accessible

GIVEN the source asset viewer is open
WHEN the user is reading a source asset
THEN audio playback controls (play/pause, scrubber, etc.) remain accessible

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

## AC-SA-06: AI summary per asset

GIVEN a source asset is opened in the viewer
WHEN the user views the asset
THEN an AI-generated summary for that asset is displayed

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

## AC-SA-07: Synchronized reference — future scope

GIVEN the source asset viewer
WHEN synchronized highlighting (audio position → asset highlight) is considered
THEN this feature is deferred to future scope and not in the current implementation

(source: cf1f9c0c-3fb3-4bc6-a3a2-b867e208e94e_Source_Asset(s)_Viewer_-_Podcasts.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[podcast-reports]]
- [[podcast-simulation-in-courses]]
- [[microlearning-podcast]]
- [[push-notifications]]
