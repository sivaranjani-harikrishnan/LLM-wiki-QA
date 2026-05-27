# Product: HeySales Overview

**Summary**: HeySales is an AI-powered sales training platform built on top of Paperflite, enabling organisations to create, assign, and measure structured learning experiences for sales teams.

**Sources**: Multiple PDFs and CSVs from `raw/` (see feature pages for source-level citations)

**Last updated**: 2026-05-25

---

## What it is

HeySales is a sales enablement and readiness platform accessed through the Paperflite left-navigation panel. It gives sales organisations three types of AI-generated learning: **Courses**, **Podcasts**, and **Simulations** — plus a Live (Real Call) Scoring capability that assesses actual Zoom calls against scorecards.

HeySales must be explicitly enabled on a Paperflite account. Once enabled, it is visible in the Paperflite left panel for all users who have access.

## Core modules

| Module | What it is |
|---|---|
| Manage Courses | Admin interface to create, publish, and assign courses, podcasts, simulations |
| Studio | Where admins create and edit podcasts and simulations |
| Let's Learn | Per-user AI article + audio generation (Microlearning) |
| My Space | Learner's assigned content queue |
| Explore | Browse and self-enrol in published content |
| Reports | Dashboards for completion rates, scores, time spent |

## Learning types

Three learning types exist. Each has its own creation flow, learner experience, and reporting:

- **Courses**: Structured content modules containing lessons (files, URLs), assessments (quizzes), podcasts, and simulations. Learners must complete all elements to end a course. Courses may optionally use Sections to group content.
- **Podcasts**: AI-generated audio content based on admin-uploaded source assets (PDF, PPT, DOC, URL). Three audio types: Conversational (two voices), Monologue (one voice), Narrative (one smooth voice, no fillers). Duration can be set from 5–30 min or flexible.
- **Simulations**: AI role-play conversations where a learner practises a sales call against an AI prospect. Variants include Cold Call, Discovery, Follow-up, and Elevator Pitch. Reports generate a scored breakdown against a Scorecard.

## Real Call Scoring

When a user integrates Zoom + a CRM (HubSpot or MS Dynamics), completed Zoom calls are automatically assessed using the account's default scorecard. Reports are pushed to the CRM as notes (HubSpot) or activity/timeline entries (MS Dynamics).

## SEEK

SEEK is HeySales's built-in AI assistant. It can be used from within the Studio edit screen to modify podcasts via natural-language prompts (e.g., "Change the duration to 10 mins", "change the type to Narrative").

## Microlearning (Let's Learn)

Every user (regardless of role) can use the Let's Learn module to generate a private AI article from their own source files and prompts. These articles can also generate a private audio podcast (Microlearning Podcast). These are strictly private — not visible to admins or managers.

## Key architectural facts

- HeySales is an overlay on Paperflite; the Paperflite account must have HeySales enabled
- Each Paperflite account has exactly one **Default Scorecard** at any time (Paperflite MEDDIC scorecard is always the fallback)
- Real Call Scoring via HubSpot uses USER-level Zoom integration; via MS Dynamics uses ACCOUNT-level Zoom integration
- When both Fireflies and Zoom are integrated, Fireflies takes priority for real call scoring

## Related pages

- [[user-roles]]
- [[learning-types]]
- [[custom-scorecards]]
- [[real-call-scoring]]
- [[microlearning]]
