# Wiki Structure

## Purpose

This wiki is a structured, interlinked knowledge base for the HeySales AI sales training product. It is maintained by Claude and used by multiple teams — product, engineering, QA, support, onboarding, and new hires — to understand how the product works, how it is verified, and how it behaves in the field.

The human curates sources, asks questions, and guides the analysis. Claude maintains the wiki, surfaces insights, and compounds knowledge over time.

**Scope**: All functional features of HeySales across all user-facing workflows. Performance, security, and accessibility are out of scope unless explicitly stated.

---

## Folder layout

```
../raw/                          -- source documents (immutable — never modify these)
../wiki/                         -- markdown pages maintained by Claude
../wiki/index.md                 -- table of contents for the entire wiki
../wiki/log.md                   -- append-only record of all operations
../wiki/contradictions.md        -- log of all contradictions found across source files
../wiki/usage.md                 -- append-only log of token usage and cost per operation
../wiki/product/                 -- product-level context pages
../wiki/features/                -- one folder per HeySales feature
../wiki/features/<feature-name>/
  overview.md                    -- what the feature does, who uses it, how it works
  ac.md                          -- acceptance criteria (authoritative definition)
  test-coverage.md               -- existing test cases and what they verify
../wiki/audiences/               -- role-specific query guides
  for-testing.md
  for-support.md
  for-engineering.md
  for-pm.md
  for-onboarding.md
  for-new-hires.md
../wiki/meta/
  content-standards.md           -- how each doc type should be written
  how-to-use-this-wiki.md        -- prompt patterns for each role
```

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

## General rules

- Never modify anything in the `../raw/` folder
- Always update `../wiki/index.md` and `../wiki/log.md` after any changes
- Log all contradictions to `../wiki/contradictions.md` — never inline
- Keep page names lowercase with hyphens (e.g. `email-personalization.md`)
- Write in clear, plain language
- When uncertain about how to categorise something, ask the user
