# LLM Wiki — HeySales (Testing Team)

A product knowledge base maintained for the HeySales AI sales training product.
Based on Andrej Karpathy's LLM Wiki pattern.

## Purpose

This wiki is a structured, interlinked knowledge base for the HeySales AI sales training product. It is used by the QA and testing team to understand how the product works, how it is verified, and what gaps exist in test coverage.

**Your role in this wiki**: Query and explore only. You can ask questions, run lint audits, and get QA-focused answers. You cannot modify, ingest, or update any wiki content.

**Scope**: All functional features of HeySales across all user-facing workflows. Performance, security, and accessibility are out of scope unless explicitly stated.

---

## Folder structure

```
raw/                          -- source documents (do not read or reference directly)
wiki/                         -- markdown pages you can query
wiki/index.md                 -- table of contents for the entire wiki
wiki/log.md                   -- record of all operations
wiki/contradictions.md        -- log of all contradictions found across source files
wiki/product/                 -- product-level context pages
wiki/features/                -- one folder per HeySales feature
wiki/features/<feature-name>/
  overview.md                 -- what the feature does, who uses it, how it works
  ac.md                       -- acceptance criteria (authoritative definition)
  test-coverage.md            -- existing test cases and what they verify
wiki/audiences/
  for-testing.md              -- QA-specific query guide
```

---

## Question answering

When you ask a question:

1. Read `wiki/index.md` first to find relevant pages
2. Read those pages and synthesise an answer
3. Cite specific wiki pages in the response
4. If the answer is not in the wiki, say so clearly
5. Surface untested scenarios from the ACs where relevant

### QA / Testing focus

All answers are tailored for the testing role by default:

- Focus on test cases, preconditions, steps, and expected results
- Surface untested scenarios by comparing AC definitions against existing test coverage
- Flag edge cases and behaviours that deviate from spec
- Highlight contradictions logged in `wiki/contradictions.md`
- Note where test coverage is thin, missing, or unverified

### Useful query patterns

```
What are the acceptance criteria for [feature]?
What test cases exist for [feature]?
What scenarios in [feature] are NOT covered by existing tests?
Are there any contradictions logged for [feature]?
What is the expected behaviour when [condition]?
What preconditions are needed to test [scenario]?
```

## Rules

- You cannot modify, create, or delete any wiki pages
- You cannot ingest new source documents
- You cannot resolve or add contradiction entries
- All answers cite specific wiki pages
- If a claim has no source in the wiki, it will be flagged as (source: unverified)



