# Feature: Custom Scorecards

**Summary**: Custom Scorecards let admins define custom assessment frameworks with named parameters and sub-parameters, which are used to score both simulations and real sales calls.

**Sources**: `Custom Scorecards - Scorecard creation.csv`, `Custom Scorecards - Simulation creation (1).csv`

**Last updated**: 2026-05-25

---

## What it does

Scorecards are assessment frameworks that define how a sales call is evaluated. Each scorecard contains parameters (e.g. "Conversation Quality") and sub-parameters, each scored 1–5. When a simulation or real call is completed, the AI scores the call against the tagged scorecard.

## Who uses it

- **Admins** and **Content Publishers**: Create, edit, publish, clone, and manage scorecards from Settings → Scorecard
- **Learners**: Never interact with scorecards directly; their calls are scored against the scorecard attached to their simulation

## How it works

### Access
- Settings → Scorecard is only visible to Admin and Content Publisher roles when HeySales is enabled
- Normal users and BI Analysts do not see this option

### The Default Scorecard
- Every account always has a "Paperflite" default scorecard (MEDDIC-based)
- The default scorecard **cannot be deleted or renamed**
- One scorecard must always be marked as default; marking a new scorecard as default removes the tag from the previous one
- If a custom default is deleted, the system reverts to the Paperflite scorecard as default

### Creating a Scorecard
1. Click "Create new scorecard" in Settings → Scorecard
2. A slider opens; enter name + description
3. Add parameters (default is "Untitled" — no limit on count)
4. Add at least one sub-parameter per parameter (required to publish)
5. Set weightage (numeric only, max 100 per parameter, no negatives or decimals)
6. Choose call type: All / Discovery / Cold Call / Follow-up
7. Save (draft) → Publish (active)

### States
- **Draft**: saved but not active; not selectable for simulations
- **Active**: published and available for selection

### Call Type filtering
During simulation creation, the scorecard picker only shows scorecards matching the simulation's call type OR scorecards tagged as "All". If no matching scorecard exists for the simulation type, an empty message is shown.

### Cloning
The clone button creates a copy named "Clone of [original name]".

### Deleting
Deleting a scorecard does not affect simulations already using it. The deleted scorecard's reports remain intact. The system reverts to the Paperflite default scorecard for future simulations if the deleted scorecard was the default.

### Discarding
Clicking Discard reverts to the last saved (published) version.

## Things to know

- The scorecard section in simulation creation shows: scorecard name, sub-text, parameter count, sub-parameter count, Preview and Change buttons (source: `Custom Scorecards - Simulation creation (1).csv` TC0016)
- Preview navigates to the detailed scorecard screen (source: TC0012)
- Change navigates to the scorecard list filtered by simulation type (source: TC0013)
- The default scorecard is pre-populated when creating a new simulation (source: TC0011)
- Edits to the default scorecard setting in Settings do NOT affect already-published simulations (source: `Elevator pitch - phase 1 - Sheet2.csv` TC0011)

## Related pages

- [[ac]]
- [[test-coverage]]
- [[simulations]]
- [[real-call-scoring]]
