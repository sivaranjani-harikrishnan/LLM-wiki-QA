# Feature: Live Call Help

**Summary**: A planned AI feature that listens to sales calls in real time and surfaces guidance to reps during the call — including knowledge answers, objection counters, next-best questions, and buying signal alerts.

**Sources**: `raw/d480b950-b052-4053-8bb0-71f9c0dda5bb_Live_call_help.pdf`

**Last updated**: 2026-05-25

---

## What it does
Live Call Help is a real-time AI assist layer that runs during live sales calls. The AI listens to the call (via a meeting bot or browser audio capture), identifies what is happening, and surfaces relevant guidance to the rep — without the prospect seeing the suggestions.

## Who uses it
Sales reps (AEs, Junior AEs, call centre / support agents) who need in-call support for knowledge recall, objection handling, discovery coaching, buying signal detection, and script compliance.

## How it works

### Audio capture options
Two approaches are documented:

**A. Bot joins the meeting (Zoom/Teams)**
- An AI bot joins as a visible participant.
- Gets clean, mixed audio from the platform.
- Typical latency: approximately 2-3 seconds end-to-end.
- Higher audio quality and reliability; clearer compliance posture.

**B. Browser/desktop audio capture (local)**
- A desktop app or browser extension captures system audio.
- Processes locally and/or streams to cloud.
- Typical latency: approximately 1.3-1.8 seconds with optimisations.
- OS/device-dependent reliability; requires deep OS permissions.

### Types of guidance during the call
- **Informational**: Surfaces knowledge answers and battlecards when a competitor or technical topic is detected. Example: "Prospect mentioned competitor X; here's the battlecard."
- **Prescriptive/Assistive**: Suggests what to say next or what question to ask. Example: "Say this next", "Ask this question."
- **Passive**: Transcription, metrics, and logs with no active suggestion.

### Real-time behaviour patterns
- **Knowledge / answer surfacing**: When prospect asks a technical question, the panel shows key bullet points and relevant doc links.
- **Objection-specific responses**: Detects objection signals (e.g. "pricing is high") and shows a rebuttal and ROI case.
- **Next-best question**: Detects missing MEDDPICC fields and suggests the specific question to fill them.
- **Behaviour nudges**: Talk ratio alerts ("slow down", "ask open-ended question").
- **Risk / buying signal highlights**: Flags budget concerns or implementation timeline mentions.

### UX patterns
- **Floating side panel**: Slides in with a suggestion; auto-hides after a few seconds.
- **Inline transcript highlights**: Key phrases underlined or colour-coded in live transcript.
- **Discreet nudges**: Small banners or icons.
- **Cue cards**: Full cards with Q&A, talking points, and "mistakes to avoid".

Research indicates reps can handle 0-3 meaningful prompts during a call; suggestions must be clear, short, and easy to ignore if not needed.

### Intelligence data sources
The AI draws on:
- Static knowledge base (product docs, FAQs, internal wikis, PDFs)
- Uploaded sales playbooks (objection scripts, discovery frameworks, talk tracks)
- CRM data (deal stage, prior conversations, industry, persona)
- Past call transcripts ("what top reps said when they won")
- "Best rep" language patterns correlated with wins

### Technical pipeline
1. Audio capture (bot or local)
2. Speech recognition
3. NLP and classification (detect objections, topics, sentiments, entities)
4. Context lookup (knowledge base, playbooks, past calls)
5. Response decision (rules / templates / RAG / LLM)
6. Delivery (real-time push to in-call UI)

## Things to know
- This feature is in the design and research phase; the source document is a design brief with competitor research (Vivun, Poised, Colibri, Balto AI, Aside AI, Cluely AI). No formal acceptance criteria have been defined. (source: d480b950-b052-4053-8bb0-71f9c0dda5bb_Live_call_help.pdf)
- The AI should be positioned as "Assist" not "Control" — language should use "Suggested response" rather than "Say this," and reps should always be able to dismiss suggestions. (source: d480b950-b052-4053-8bb0-71f9c0dda5bb_Live_call_help.pdf)
- Content setup (knowledge base and playbooks) is described as "very important and critical" for the quality of suggestions. (source: d480b950-b052-4053-8bb0-71f9c0dda5bb_Live_call_help.pdf)
- Suggested Phase 1 scope: audio capture, identifying knowledge objections and technical questions, searching indexed content, and showing instant responses or sales methodology talking points. (source: d480b950-b052-4053-8bb0-71f9c0dda5bb_Live_call_help.pdf)

## Related pages
- [[ac]]
- [[real-call-scoring]]
- [[call-library]]
- [[call-classification]]
