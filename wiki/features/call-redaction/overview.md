# Feature: Call Redaction

**Summary**: Automatically redacts personal and private information from call transcripts before they are passed to the LLM for assessment, while preserving the original transcript for display in reports.

**Sources**: `raw/bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf`

**Last updated**: 2026-05-25

---

## What it does
Call Redaction censors sensitive personal information (e.g. credit card credentials) from call transcripts before they are sent to the AI for scoring. This protects privacy while still enabling full assessment.

## Who uses it
This is a system-level process — it runs automatically. It is invisible to end users but affects all calls that flow through real call scoring and simulation extraction pipelines.

## How it works
1. A call recording arrives (via Zoom, Fireflies, Teams integration, manual upload, or simulation extraction upload).
2. Before the transcript is sent to the LLM for assessment, the redaction process runs.
3. The LLM receives only the redacted transcript.
4. The original (unredacted) transcript continues to be shown in the evaluation reports UI.

## Things to know
- The redacted transcript is used for scoring; the original transcript is shown to users in reports. (source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)
- Technical details of how redacted vs original transcripts are stored were pending confirmation from the engineering team at time of writing. (source: bbfc1a2f-a5fd-4f22-b5b7-739d3953ef70_Call_redaction.pdf)

## Related pages
- [[ac]]
- [[real-call-scoring]]
- [[call-library]]
- [[simulations]]
