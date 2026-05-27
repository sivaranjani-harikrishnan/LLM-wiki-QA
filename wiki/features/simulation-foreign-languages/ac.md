# Acceptance Criteria: Simulation — Foreign Languages

**Summary**: Defines language selection, AI prospect behaviour, rep expectations, and reporting for foreign language simulations.

**Sources**: `raw/8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf`

**Last updated**: 2026-05-25

---

## AC-FL-01: Language selection in simulation setup

GIVEN a creator is setting up a call simulation
WHEN they go through the setup flow
THEN there is a step to select a language from a predefined list (e.g. English, Spanish, French, German)

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-02: Default language is English

GIVEN a creator does not select a language during simulation setup
WHEN the simulation is created
THEN the language defaults to English

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-03: Chosen language shown in simulation overview

GIVEN a language has been selected
WHEN the learner views the simulation overview before starting
THEN the chosen language is displayed clearly

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-04: Chosen language shown in UI cards

GIVEN a simulation has a language configured
WHEN it appears in any UI card across the platform
THEN the chosen language is displayed on that card

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-05: AI prospect communicates entirely in chosen language

GIVEN a language has been selected for the simulation
WHEN the simulation begins
THEN the AI prospect speaks entirely in the chosen language, including the initial greeting

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-06: AI prospect does not switch languages

GIVEN the simulation is in progress in a foreign language
WHEN the rep responds in a different language
THEN the AI prospect does not switch to the rep's language; it continues speaking in the originally chosen language

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-07: Performance evaluated in chosen language

GIVEN the rep completes a simulation in a foreign language
WHEN the system evaluates their performance
THEN evaluation is conducted in the chosen language

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

## AC-FL-08: Reports localised or in English (configurable)

GIVEN a simulation in a foreign language is completed
WHEN the report and feedback are generated
THEN they are localized to the selected language or appear in English, depending on the configurable setting

(source: 8593129a-9341-4b00-85f3-c9d04a539c59_Simulation_-_Foreign_Languages.pdf)

---

## Related pages
- [[overview]]
- [[simulations]]
- [[simulation-reports]]
