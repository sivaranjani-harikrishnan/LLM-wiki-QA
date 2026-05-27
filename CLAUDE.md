# LLM Wiki — HeySales

A product knowledge base maintained by Claude Code.
Based on Andrej Karpathy's LLM Wiki pattern.

## Purpose

This wiki is a structured, interlinked knowledge base for the HeySales AI sales training product. It is maintained by Claude and used by multiple teams — product, engineering, QA, support, onboarding, and new hires — to understand how the product works, how it is verified, and how it behaves in the field.

The human curates sources, asks questions, and guides the analysis. Claude maintains the wiki, surfaces insights, and compounds knowledge over time.

**Scope**: All functional features of HeySales across all user-facing workflows. Performance, security, and accessibility are out of scope unless explicitly stated.

---

## Folder structure

```
raw/                          -- source documents (immutable — never modify these)
wiki/                         -- markdown pages maintained by Claude
wiki/index.md                 -- table of contents for the entire wiki
wiki/log.md                   -- append-only record of all operations
wiki/contradictions.md        -- log of all contradictions found across source files
wiki/usage.md                 -- append-only log of token usage and cost per operation
wiki/product/                 -- product-level context pages
wiki/features/                -- one folder per HeySales feature
wiki/features/<feature-name>/
  overview.md                 -- what the feature does, who uses it, how it works
  ac.md                       -- acceptance criteria (authoritative definition)
  test-coverage.md            -- existing test cases and what they verify
wiki/audiences/               -- role-specific query guides
  for-testing.md
  for-support.md
  for-engineering.md
  for-pm.md
  for-onboarding.md
  for-new-hires.md
wiki/meta/
  content-standards.md        -- how each doc type should be written
  how-to-use-this-wiki.md     -- prompt patterns for each role
```

---

## Source types

Three types of documents will appear in `raw/`. Treat each differently during ingest:

- **Product ACs (Acceptance Criteria)**: The authoritative definition of intended behaviour. When a contradiction exists between an AC and any other source type, the AC is considered ground truth unless the user says otherwise.
- **Support articles**: Reflect how the product actually behaves in the field. Useful for surfacing edge cases, common user confusion, and real-world deviations from intended behaviour.
- **Test case documents**: Describe existing test coverage. The **Test Case Title** and **Description** fields are the most important — they define the intent of each test. Use these to understand what is verified and identify what is not.

### Test case spreadsheet columns

Incoming test case documents will have these columns:

```
Sprint Name, Test Case Title, Test Assignee, Description, Mode,
Priority, Type, Precondition, Test Data, Steps, Expected Result,
Actual Result, Tags
```

During ingest, **Test Case Title** and **Description** are primary. All other fields are supporting context.

---

## Ingest workflow

When the user adds a new source to `raw/` and asks you to ingest it:

1. Read the full source document
2. Identify its source type (AC, support article, or test case document)
3. Discuss key takeaways with the user before writing anything
4. Create a summary page in `wiki/` named after the source
5. Create or update the relevant feature pages under `wiki/features/<feature-name>/`
6. Create or update concept pages in `wiki/product/` for any product-level ideas
7. Add wiki-links ([[page-name]]) to connect related pages throughout
8. Update `wiki/index.md` with new or changed pages and one-line descriptions
9. Append an entry to `wiki/log.md` with the date, source name, and what changed
10. If any contradictions were found, log them to `wiki/contradictions.md`
11. Append a token usage entry to `wiki/usage.md`

A single source may touch 10–15 wiki pages. That is normal.

---

## Page formats

### `wiki/features/<feature-name>/overview.md`

```markdown
# Feature: <Feature Name>

**Summary**: One to two sentences describing what this feature does.

**Sources**: List of raw source files this page draws from.

**Last updated**: YYYY-MM-DD

---

## What it does
Short description (2–3 sentences max).

## Who uses it
Which user roles interact with this feature and how.

## How it works
Step-by-step user-facing flow.

## Things to know
Key behaviours drawn from support articles — common questions,
known edge cases, or behaviours that differ from user expectations.
Use plain language. Cite sources inline: (source: filename)

## Related pages
- [[ac]]
- [[test-coverage]]
- [[related-feature]]
```

### `wiki/features/<feature-name>/ac.md`

```markdown
# Acceptance Criteria: <Feature Name>

**Summary**: What this feature must do according to the product spec.

**Sources**: List of AC source files.

**Last updated**: YYYY-MM-DD

---

## <AC-ID>: <Short title>
GIVEN <precondition>
WHEN <action>
THEN <expected outcome>

(source: filename)

## Related pages
- [[overview]]
- [[test-coverage]]
```

### `wiki/features/<feature-name>/test-coverage.md`

```markdown
# Test Coverage: <Feature Name>

**Summary**: What test cases exist for this feature and what they verify.

**Sources**: List of test case source files.

**Last updated**: YYYY-MM-DD

---

## <TC-ID>: <Test Case Title>

**What this tests**: <Description field from spreadsheet — preserved as written>

**Covers**: <AC-ID if applicable>

**Priority**: <P1/P2/P3> | **Type**: <Functional/Negative/Edge case/etc.>

**Precondition**: <Precondition field>

**Steps**:
1. <Step>
2. <Step>

**Expected result**: <Expected Result field>

(source: filename)

---

## Related pages
- [[ac]]
- [[overview]]
```

### Standard page format (all other pages)

```markdown
# Page Title

**Summary**: One to two sentences describing this page.

**Sources**: List of raw source files this page draws from.

**Last updated**: YYYY-MM-DD

---

Main content here. Use clear headings and short paragraphs.
Link to related concepts using [[wiki-links]] throughout.

## Related pages
- [[related-concept-1]]
- [[related-concept-2]]
```

---

## Citation rules

- Every factual claim must reference its source: (source: filename)
- If two sources disagree, do not note it inline — log it to `wiki/contradictions.md`
- If a claim has no source, mark it as (source: unverified)

---

## Contradictions

Whenever two sources conflict, log to `wiki/contradictions.md`. Do not halt ingestion — continue and log all contradictions at the end of the ingest step.

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

## Question answering

When the user asks a question:

1. Read `wiki/index.md` first to find relevant pages
2. Read those pages and synthesise an answer
3. Cite specific wiki pages in your response
4. If the answer is not in the wiki, say so clearly
5. If the answer is valuable, offer to save it as a new wiki page

Good answers should be filed back into the wiki so they compound over time.

### Audience-aware answering

If the user identifies their role (or it is clear from context), tailor the answer:

- **Testing / QA**: Focus on test cases, preconditions, steps, and expected results. Surface untested scenarios from the ACs.
- **Product / PM**: Focus on AC definitions, feature behaviour, and what is or isn't specified.
- **Engineering**: Focus on system behaviour, edge cases, and deviations from spec.
- **Support**: Focus on how the feature behaves in the field, common confusion points from support articles.
- **Onboarding / Sales**: Focus on the user-facing flow and what the feature does for the end user.
- **New hires**: Start from `wiki/product/` context, then link to specific features.

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

## Rules

- Never modify anything in the `raw/` folder
- Always update `wiki/index.md` and `wiki/log.md` after any changes
- Log all contradictions to `wiki/contradictions.md` — never inline
- Always append a token usage entry to `wiki/usage.md` after every operation
- Keep page names lowercase with hyphens (e.g. `email-personalization.md`)
- The **Test Case Title** and **Description** fields are the primary fields when ingesting test case documents — preserve them faithfully
- Write in clear, plain language
- When uncertain about how to categorise something, ask the user