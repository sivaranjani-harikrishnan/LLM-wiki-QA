# Feature: AI Search (Manage Courses)

**Summary**: AI-powered search in Manage Courses allows admins to find content using natural language, partial matches, skill names, and descriptions — ranked by relevance with name matches prioritised.

**Sources**: `AI Search Manage Courses - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## What it does

The AI Search feature in Manage Courses enables admins and content publishers to search across all learnings using natural language queries, skill-based searches, and partial or approximate name matches (via Atlas Search with typo tolerance).

## Who uses it

- **Admins / Content Publishers**: Search for learnings to manage or assign

## How it works

### Search ranking

Results are ranked in this priority order:
1. **Name match** (highest priority)
2. **Skill match**
3. **Description match**

### Search capabilities

| Search type | Behaviour |
|---|---|
| Exact name | Returns matching learning immediately |
| Partial name | Returns learnings containing the partial term |
| Skill name | Returns learnings tagged with that skill |
| Description terms | Returns learnings whose description contains those terms |
| Natural language / NLP | Extracts keywords and searches; e.g., "show me discovery call courses" returns discovery call content |
| Plural terms | Returns results for singular equivalents and vice versa |
| Typos / approximate matches | Returns results via Atlas Search fuzzy matching |
| Special characters | Handled gracefully (no crash) |
| Emojis | Handled gracefully |

### Empty states

- Spaces-only query: empty state shown
- No matching results: empty state shown with no results message

## Things to know

- Search is available in Manage Courses specifically (source: `AI Search Manage Courses - Sheet1 (1).csv`)
- Atlas Search powers the fuzzy/typo tolerance (source: TC descriptions in CSV)
- Ranking is name > skill > description (source: TCs covering ranking)

## Related pages

- [[test-coverage]]
- [[courses]]
