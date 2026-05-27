# Acceptance Criteria: Learner Reports

**Summary**: Defines the stage-based north star metric logic, readiness scoring rules, call excellence composition, win rate activation, and action card behaviour.

**Sources**: `raw/dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf`

**Last updated**: 2026-05-25

---

## North Star Metric ACs

## AC-LR-01: Stage-based north star metric

GIVEN a rep's scorecard is displayed
WHEN their current stage is determined
THEN the north star metric shifts based on stage: Stage 1 = Readiness score, Stage 2 = Call excellence score, Stage 3 = Win rate

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

---

## Stage 1 — Readiness ACs

## AC-LR-02: Readiness requires two pillars to be cleared

GIVEN a rep is in Stage 1 (onboarding)
WHEN readiness is evaluated
THEN both Pillar 1 (Knowledge) and Pillar 2 (Simulations) must be cleared; clearing one does not compensate for failing the other

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-03: Pillar 1 — Knowledge threshold

GIVEN a rep is working toward Pillar 1 clearance
WHEN their course scores are checked
THEN all required courses must be passed at a minimum score of 70%; a course is passed only by achieving the threshold, not by clicking through

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-04: Pillar 2 — Simulation threshold

GIVEN a rep is working toward Pillar 2 clearance
WHEN their simulation scores are checked
THEN the average best score across all three frameworks (discovery, demo/value prop, closing) must reach 85%; a minimum of 3 attempts per framework is required before any score is registered; the best single attempt per framework is used (not average)

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-05: Pillar 2 — Floor rule

GIVEN a rep is evaluated on Pillar 2
WHEN any individual framework score is below 70%
THEN readiness is blocked regardless of the overall 85% average — no framework may fall below 70%

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

---

## Stage 2 — Call Excellence ACs

## AC-LR-06: Call excellence score composition

GIVEN a rep is in Stage 2 (ramping on calls)
WHEN the call excellence score is calculated
THEN it is composed of 60% call quality score (AI-scored on the same three frameworks as simulations) and 40% stage conversion rate (discovery to proposal progression)

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-07: Transfer gap detection

GIVEN a rep has both simulation scores and real call scores on the same framework
WHEN the transfer gap is calculated
THEN it is defined as: simulation score minus real call score on the same framework; a gap of 10+ points signals a transfer problem (skill exists in practice but not applied live)

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-08: Real call readiness — framework status states

GIVEN a framework is tracked for a rep's real call performance
WHEN its status is determined
THEN it can be one of: Accumulating (fewer than 4 scored calls), Below threshold (minimum reached, average under 85%), Cleared (average at or above 85%), At risk (was cleared, rolling average has since dropped below threshold)

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-09: "At risk" does not revert stage

GIVEN a framework transitions to "At risk"
WHEN the rep's overall stage is evaluated
THEN "At risk" status raises a targeted coaching flag but does NOT revert the rep to a previous stage

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

---

## Stage 3 — Win Rate ACs

## AC-LR-10: Win rate activation threshold

GIVEN a rep has been on live calls
WHEN the win rate metric activates
THEN it requires 8 or more closed deals in a rolling 90-day window before it activates

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-11: Win rate calculation and display

GIVEN win rate is active for a rep
WHEN it is displayed
THEN it is calculated as closed won divided by total closed deals in a rolling 90-day window; it is always shown with the sample size (e.g. "62% based on 11 deals")

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

## AC-LR-12: Win rate benchmarked against same-tenure peers

GIVEN win rate is displayed for a rep
WHEN peer comparison is shown
THEN it is benchmarked against the team average and top-performer quartile at the same tenure band

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

---

## Rep Self-View ACs

## AC-LR-13: Rep sees same cards with different language

GIVEN a rep views their own scorecard
WHEN they see action cards
THEN the same cards are shown as to the manager, but the language shifts from diagnostic to directional; manager assignment controls are hidden

(source: dd1587b0-9cea-4b90-bf28-83450e64c150_Learner_Reports.pdf)

---

## Related pages
- [[overview]]
- [[simulations]]
- [[simulation-reports]]
- [[real-call-scoring]]
- [[courses]]
- [[course-reports]]
