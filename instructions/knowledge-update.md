# Knowledge Update

## Contradictions

Whenever two sources conflict, log to `../wiki/contradictions.md`. Do not halt ingestion — continue and log all contradictions at the end of the ingest step.

The contradictions file is append-only. Each entry:

```markdown
### [Short description of the contradiction]

- **Detected on**: YYYY-MM-DD
- **File A**: `raw/filename-a.ext` — [paraphrase of the claim]
- **File B**: `raw/filename-b.ext` — [paraphrase of the conflicting claim]
- **Topic**: Which feature or concept this relates to
- **Status**: Unresolved
```

When the user resolves a contradiction, update `Status` to `Resolved — [brief explanation]`. Never delete entries.

---

## Lint

When the user asks you to lint or audit the wiki:

- Check for contradictions between pages
- Find orphan pages (no inbound links from other pages)
- Identify concepts mentioned in pages that lack their own page
- Flag claims that may be outdated based on newer sources
- Check that all pages follow the correct page format
- Check that all `wiki/contradictions.md` entries have a Status field
- Report findings as a numbered list with suggested fixes

---

## Token usage logging

Every token-consuming operation must append an entry to `wiki/usage.md`. Do this as the final step of any operation, after all wiki writes are complete.

### Pricing reference (as of May 2026)

| Model | Input (per 1M tokens) | Output (per 1M tokens) |
|---|---|---|
| Claude Opus 4.6 | $5.00 | $25.00 |
| Claude Sonnet 4.6 | $3.00 | $15.00 |
| Claude Haiku 4.5 | $1.00 | $5.00 |

**Thinking tokens** are billed at the same rate as output tokens. Track separately for visibility.

Cost formula: `(input_tokens / 1,000,000 × input_rate) + ((output_tokens + thinking_tokens) / 1,000,000 × output_rate)`

### Entry format

```markdown
| YYYY-MM-DD HH:MM | <operation_type> | <source_file_or_description> | <model> | <input_tokens> | <output_tokens> | <thinking_tokens> | $<input_cost> | $<output_cost> | $<total_cost> |
```

Operation types: `ingest`, `question-answering`, `lint`, `page-update`, `other`

### File structure

```markdown
# Token Usage Log

| Date & Time | Operation | Description | Model | Input Tokens | Output Tokens | Thinking Tokens | Input Cost | Output Cost | Total Cost |
|---|---|---|---|---|---|---|---|---|---|

---

**Cumulative total: $X.XX** (updated after every entry)
```

Never delete old entries. Recalculate cumulative total after every new entry.

---

## Rules specific to knowledge update

- Always update `../wiki/index.md` and `../wiki/log.md` after any changes
- Always append a token usage entry to `../wiki/usage.md` after every operation
- Log all contradictions to `../wiki/contradictions.md` — never inline
