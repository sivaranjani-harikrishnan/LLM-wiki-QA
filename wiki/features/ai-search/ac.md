# Acceptance Criteria: AI Search

**Summary**: Defines how AI-powered search works within Manage Courses, including what fields are searched, ranking, and UI states.

**Sources**: `raw/5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf`

**Last updated**: 2026-05-25

---

## AC-AS-01: AI search within Manage Courses (Phase 1 scope)

GIVEN a user is in the Manage Courses section
WHEN they enter a search query
THEN AI search is available in this context (this is Phase 1; My Learning and Mobile are future phases)

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-02: Keyword extraction pipeline

GIVEN a user enters a search query
WHEN the search is processed
THEN the AI agent extracts keywords from the query and passes them to Atlas Search, which returns results to the UI

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-03: Fields searched in Phase 1

GIVEN a search query is executed
WHEN matching is performed
THEN results are matched against: name of the learning and description of the learning

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-04: Fields not in Phase 1 scope

GIVEN Phase 1 of AI search
WHEN search is executed
THEN skills mapped to the learning and type of the learning are NOT searched in this phase (deferred to future phases)

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-05: Three UI states

GIVEN a search query has been entered
WHEN the results are displayed
THEN the UI handles three states: (1) results found, (2) no results found, (3) no results but AI suggests follow-up queries — state 3 is not in Phase 1 scope

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-06: Ranking order

GIVEN search results are returned
WHEN they are ranked
THEN the ranking priority order (heaviest weightage first) is: name > description > skill > type

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-07: Mixed result types

GIVEN a search query returns results
WHEN results are displayed
THEN results can be mixed content types (podcasts, courses, simulations, etc.) and are not grouped into fixed sections

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

## AC-AS-08: Partial and combination match

GIVEN a search query is executed
WHEN matching is applied
THEN partial match and combination match logic follows the same rules as Paperflite's Global Search Atlas Search implementation

(source: 5945b0d7-edae-427f-946c-ea0e2354a50d_AI_Search_-_Manage_Courses__.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[courses]]
