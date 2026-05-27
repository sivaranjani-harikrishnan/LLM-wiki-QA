# Feature: Simulation Call Recording

**Summary**: Admins can listen to and view the full audio/transcript recording of each learner's simulation attempt from within the detailed report screen.

**Sources**: `Simulation Call Recording - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

Within the simulation detailed report, admins can open a call recording slider that shows the transcript and provides audio playback controls for any completed attempt. The slider syncs audio to transcript in real time.

## Who uses it

- **Admins / Content Publishers**: Access call recordings from the detailed report screen

## How it works

### Accessing the recording
1. Open a simulation → click a completed learner
2. In the detailed report screen, click the "Call Recording" button (shown inline with the breakdown section and attempts dropdown)
3. The learner list slides out of view; the call recording slider opens on the right

### Call Recording button UI
- Text: "call recording"
- Audio logo icon
- Only shown for completed learners (not for not-started)
- If the learner has no retakes, the attempts dropdown is not shown — only the call recording button

### Slider contents
- Heading: "call recording" (top left)
- Close button [x] (top right)
- Call type (e.g., Follow up, Cold call)
- Challenge level
- Transcript: both learner and AI turns, with profile pictures and timestamps
- Audio player controls:
  - Audio slider (scrubber)
  - Volume button
  - Play / Pause
  - Skip forward 15 seconds
  - Skip backward 15 seconds
  - Playback speed selector

### Per-attempt viewing
- When the admin switches attempts in the attempts dropdown, the call recording updates to show that attempt's recording
- Selecting an NA attempt (call under 2 minutes) shows an error message instead of the recording

### Scrolling
- Admins can scroll through the full transcript

## Things to know

- The UI shift (learner list slides out) happens automatically when the slider opens (source: TC0006)
- Audio controls all function correctly: play/pause, skip, speed change, and scrubbing all update the audio track (source: TC0009)
- NA calls show an error message, not an empty state (source: TC0008)

## Related pages

- [[overview]]
- [[test-coverage]]
- [[simulation-reports]]
