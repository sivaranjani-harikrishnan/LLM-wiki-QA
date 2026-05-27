# Meta: Content Standards

**Summary**: Standards for writing and maintaining all pages in this wiki.

**Last updated**: 2026-05-25

---

## Page types and their required formats

### `wiki/features/<feature-name>/overview.md`
Required sections:
- What it does (2–3 sentences)
- Who uses it (roles)
- How it works (step-by-step)
- Things to know (field behaviours, edge cases, surprises)
- Related pages (wiki-links)

### `wiki/features/<feature-name>/ac.md`
Required sections:
- One AC block per rule: GIVEN / WHEN / THEN format
- Source citation per block

### `wiki/features/<feature-name>/test-coverage.md`
Required sections:
- TC ID and title
- What this tests (Description field from source, preserved verbatim)
- Priority and Type
- Precondition
- Steps
- Expected result
- Source citation

### `wiki/product/` pages
Standard page format with clear headings and short paragraphs.

### `wiki/audiences/` pages
Scenario-based, written in plain language for the target role. May use Q&A format for support.

---

## Citation rules

- Every factual claim must end with `(source: filename)` referencing the raw source file
- If a claim derives from multiple sources, cite all: `(source: file-a.csv, file-b.pdf)`
- If a claim is unverified or inferred, mark it `(source: unverified)`
- Do NOT note contradictions inline — log them to `wiki/contradictions.md`

## Wiki-link syntax

Use `[[page-name]]` for internal links. Examples:
- `[[custom-scorecards]]` — links to the custom-scorecards overview folder
- `[[custom-scorecards/test-coverage]]` — links to a specific page within a folder
- `[[heysales-overview]]` — links to product-level overview

## Writing style

- Plain language; avoid jargon where possible
- Short sentences; short paragraphs
- Use tables for comparisons
- Active voice ("Learner clicks" not "the button is clicked by the learner")
- Concrete: include field names, button labels, error messages as they appear in the product
- No emojis
- No marketing language

## File naming conventions

- All filenames: lowercase with hyphens (e.g., `email-personalization.md`)
- Feature folder names: descriptive and hyphenated
- Never use spaces in filenames

## Source types and trust hierarchy

| Source type | Trust level |
|---|---|
| Product ACs (UUID-prefixed PDFs) | Highest — ground truth |
| Support articles (numeric-prefixed PDFs) | Field behaviour — useful for edge cases |
| Test case CSVs | Describes verified behaviours |

When AC contradicts a test case, the AC is ground truth unless the user says otherwise.

## Related pages

- [[how-to-use-this-wiki]]
