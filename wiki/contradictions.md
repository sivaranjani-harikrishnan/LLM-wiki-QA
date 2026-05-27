# Contradictions

This file is an append-only log of contradictions found across source documents.

---

### Call Library time grouping labels

- **Detected on**: 2026-05-25
- **File A**: `Call library - Sheet1 (1).csv` — Test cases describe time grouping pills as "Today", "Yesterday", "This Week", "Last Week", "2 Weeks Ago", "3 Weeks Ago", and "Month + Year" for older calls
- **File B**: Product AC documents (general descriptions) — Some descriptions mention only "today/yesterday/this week/last week/previous month" as grouping categories without "2 weeks ago" and "3 weeks ago" intermediate labels
- **Topic**: Call Library time grouping display
- **Status**: Unresolved

---

### Real call scoring: call duration threshold

- **Detected on**: 2026-05-25
- **File A**: `Real call scoring - Sheet1 (1).csv` TC0018 — "If the call is less [than] 2 mins the report should be generated" (real call scoring via Zoom generates a report even for sub-2-minute calls)
- **File B**: `Simulations Reports - Simulation Reports.csv` — Simulation calls under 2 minutes are marked as NA (not scored)
- **Topic**: Minimum call duration for scoring
- **Status**: Unresolved — the behaviours appear intentionally different (simulation context vs real call context) but this has not been explicitly confirmed by an AC document

---

### Podcast audio types naming (Enhancements vs New Type CSVs)

- **Detected on**: 2026-05-25
- **File A**: `Podcast Enhancements - Sheet1.csv` — Lists audio types as Conversational and Monologue (TC0018 mentions "Monolog" as alternative spelling)
- **File B**: `Podcast - New type  - Sheet1.csv` — Adds "Narrative" as a third audio type (TC0019); sprint name includes "Audio type - Narrative"
- **Topic**: Podcast audio type options
- **Status**: Resolved — Narrative is an additive third type introduced in the newer CSV; both documents are correct and complementary. Three total types: Conversational, Monologue, Narrative.
