# Test Coverage: Simulation Call Recording

**Summary**: 10 test cases covering the call recording slider in the simulation detailed report screen.

**Sources**: `Simulation Call Recording - Sheet1.csv`

**Last updated**: 2026-05-25

---

## TC0001: Call recording button in detailed report screen

**What this tests**: Validate For admins and content publishers in the detailed report screen in line with the break down and attempts dropdown the Call recording button should be displayed

**Precondition**: The simulation should be assigned to x number of learners and few learners should have completed the simulation

**Steps**:
1. Log in as admin / Content publisher
2. Navigate to Hey sales module
3. Open any simulation
4. Click on any completed learner
5. Check the Call recording button

**Expected result**: Call recording button is displayed inline with breakdown section and attempts dropdown

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0002: UI of the call recording button

**What this tests**: Validate The call recording button should have "call recording" text and a audio logo

**Expected result**: Button shows "call recording" text and an audio icon

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0003: Placement when learner has no retakes

**What this tests**: Validate If the learner has no retakes the attempts dropdown should not be displayed, only the call recording button should displayed

**Expected result**: Without retakes, attempts dropdown is hidden; only call recording button shown

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0004: Click on the Call recording button

**What this tests**: Validate Clicking on the Call recording button should bring a slider with the respective attempts call log

**Expected result**: Slider appears with call log for the current attempt

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0005: UI in the call recording slider

**What this tests**: Validate In the call recording slider there should be heading "call recording" on the top left of the slider, a Close button [x] on top right of the screen, Call type [Follow up, Cold call etc], Challenge Level of the call, transcript of the learner and the AI with their respective profile pics and time stamp, audio slider, Volume button, Play / pause, forward / reverse 15s buttons, play back speed button should be displayed

**Expected result**: All UI elements present as specified

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0006: UI shift when call recording button is clicked

**What this tests**: Validate When the call recording button is clicked the slider should be displayed and the List of completed learners should slide out of the UI

**Expected result**: Learner list slides out; recording slider takes its place

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0007: Call recording log of different attempts

**What this tests**: Validate The call log in the recording screen should be updated with respect to the attempt

**Steps**:
1. Open detailed report for a learner with multiple attempts
2. Click Call recording button
3. Switch between attempts in dropdown
4. Click Call recording button again

**Expected result**: Recording and transcript update to match selected attempt

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0008: Call recording of NA call (learner ends within 2 mins)

**What this tests**: Validate For call with no sufficient data [NA call] in the call recording slider an error message should be displayed

**Precondition**: The learner should end the call within 2 mins

**Steps**:
1. Open simulation
2. Click on completed learner
3. Switch to NA attempt in dropdown
4. Click Call recording button

**Expected result**: Error message displayed (not empty state)

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0009: Audio playback options

**What this tests**: Validate Admins should be able to Play / Pause, skip forward / reverse, increase / decrease play back speed, Drop or Jump to a particular time in the audio playback slider and the audio track should sync to the current selections

**Expected result**: All audio controls functional; audio syncs correctly

(source: `Simulation Call Recording - Sheet1.csv`)

---

## TC0010: Scrolling through the transcript

**What this tests**: Validate Admins should be able to scroll through the transcript in the call recording screen

**Expected result**: Transcript is scrollable

(source: `Simulation Call Recording - Sheet1.csv`)

---

## Related pages

- [[overview]]
- [[simulation-reports]]
