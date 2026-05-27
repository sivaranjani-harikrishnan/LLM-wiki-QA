# Test Coverage: AI Search (Manage Courses)

**Summary**: 29 test cases covering navigation, search by name/skill/description/type, ranking, empty states, and edge cases including special characters, typos, and NLP queries.

**Sources**: `AI Search Manage Courses - Sheet1 (1).csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Navigation and basic search (TC0001–TC0006)
- TC0001: Navigate to AI Search in Manage Courses
- TC0002: Search by name returns correct result
- TC0003: Search by skill returns learnings with that skill
- TC0004: Search by description keywords returns matching learnings
- TC0005: Search by learning type filters correctly
- TC0006: Empty query shows empty state

### Ranking (TC0007–TC0010)
- TC0007: Name match ranked above skill match
- TC0008: Skill match ranked above description match
- TC0009: Multiple results ranked correctly by relevance
- TC0010: Search query matching both name and skill returns name match first

### Edge cases (TC0011–TC0020)
- TC0011: Spaces-only query → empty state (no results)
- TC0012: Special characters in query → handled gracefully
- TC0013: Emoji in query → handled gracefully
- TC0014: Typo in search term → Atlas Search returns approximate matches
- TC0015: Partial name → returns learnings containing partial term
- TC0016: Plural terms → returns singular equivalents and vice versa
- TC0017: All uppercase query → returns correct results (case-insensitive)
- TC0018: Query with no matches → empty state with no results message
- TC0019: Very long search query → handled without errors
- TC0020: Numbers in query → handled correctly

### NLP queries (TC0021–TC0029)
- TC0021: Natural language query: "show me discovery call courses" → returns discovery call content
- TC0022: NLP keyword extraction returns relevant results
- TC0023–TC0029: Various natural language queries and expected result sets

---

## Related pages

- [[overview]]
- [[courses]]
