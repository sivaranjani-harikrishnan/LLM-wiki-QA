# Feature: Assistant

**Summary**: An AI assistant within HeySales that helps sales reps access knowledge, create practice artifacts, search learning content, get personalised growth recommendations, and navigate the app quickly.

**Sources**: `raw/68775298-2901-4e3f-8bc4-31a732a202ec_Assistant.pdf`

**Last updated**: 2026-05-25

---

## What it does
The Assistant gives reps a conversational interface to interact with the HeySales platform. It operates across four modes: Knowledge (Seek), Creation, Search, Recommendation, and Shortcuts. Each mode is optimised for a different intent — from synthesising course content into talking points, to creating simulations on demand, to surfacing the next best learning.

## Who uses it
Sales reps (primary) who want pre-call prep, on-demand practice, or fast navigation. Managers may also use it to surface team insights.

## How it works

### Knowledge (Seek)
The rep asks for synthesised answers drawn from courses and podcasts — talking points, objection counters, competitor comparisons, or topic briefs. The assistant pulls from ingested learning content rather than returning a list of lessons.

Example prompts:
- "Prep me to position against XYZ competitor for today's call — give talking points and traps to avoid."
- "Give me a 2-minute brief on pricing objections — top counters and when to use them."
- "Summarize my last Deal Intelligence podcast into 5 takeaways + 3 talk points."

### Creation (Simulations and assessments)
The rep asks the assistant to create a practice artifact — a simulation, quiz, checklist, or talk track — on demand.

Example prompts:
- "Create a dry-run simulation for a discovery call with XYZ (use case: Digital Sales Rooms)."
- "Simulate objection 'price is too high' with a skeptical CFO persona."
- "Generate a 10-question quiz from my last Deal Intelligence podcast."

### Search (Find learnings fast)
The rep asks for a ranked list of learning items filtered by facets such as skill, type, duration, difficulty, status, recency, or team effectiveness.

Example prompts:
- "Show lessons/podcasts/simulations tagged pricing negotiation, <15 min, not completed by me."
- "Find objection handling podcasts my team completed and found effective."
- "Items I can finish in 20 minutes on integration basics."

### Recommendation (Personalised growth)
The rep asks what to do next based on their skill gaps, history, and team benchmarks. The assistant proposes a learning path or sequence.

Example prompts:
- "Based on my skill standings vs team, recommend learnings to close gaps."
- "I keep scoring low on security — give me a remediation path."
- "I want to prep for certification in 2 weeks — recommend a path."

### Shortcuts (Fast navigation)
The rep asks for quick app actions without any synthesis or content creation.

Example prompts:
- "Continue the podcast I was last listening to."
- "List my incomplete learnings nearing due date."
- "Retake the last quiz I failed."

## Things to know
- The source document contains example prompt patterns per mode, not formal acceptance criteria. Formal ACs have not yet been defined for this feature. (source: 68775298-2901-4e3f-8bc4-31a732a202ec_Assistant.pdf)
- The five modes (Knowledge, Creation, Search, Recommendation, Shortcuts) are conceptually distinct — each is intended for a different user intent. (source: 68775298-2901-4e3f-8bc4-31a732a202ec_Assistant.pdf)

## Related pages
- [[ac]]
- [[simulations]]
- [[podcasts]]
- [[courses]]
- [[ai-search]]
