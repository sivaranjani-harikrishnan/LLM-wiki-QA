# Ingestion

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

When the user adds a new source to `../raw/` and asks you to ingest it:

1. Read the full source document
2. Identify its source type (AC, support article, or test case document)
3. Discuss key takeaways with the user before writing anything
4. Create a summary page in `../wiki/` named after the source
5. Create or update the relevant feature pages under `../wiki/features/<feature-name>/`
6. Create or update concept pages in `../wiki/product/` for any product-level ideas
7. Add wiki-links ([[page-name]]) to connect related pages throughout
8. Update `../wiki/index.md` with new or changed pages and one-line descriptions
9. Append an entry to `../wiki/log.md` with the date, source name, and what changed
10. If any contradictions were found, log them to `../wiki/contradictions.md`
11. Append a token usage entry to `../wiki/usage.md`

A single source may touch 10–15 wiki pages. That is normal.

---

## Rules specific to ingestion

- The **Test Case Title** and **Description** fields are the primary fields when ingesting test case documents — preserve them faithfully
- Do not halt ingestion when contradictions are found — continue and log all contradictions at the end
- Never modify anything in the `raw/` folder
