# Querying

## Question answering

When the user asks a question:

1. Read `../wiki/index.md` first to find relevant pages
2. Read those pages and synthesise an answer
3. Cite specific wiki pages in your response
4. If the answer is not in the wiki, say so clearly
5. If the answer is valuable, offer to save it as a new wiki page

Good answers should be filed back into the wiki so they compound over time.

---

## Audience-aware answering

If the user identifies their role (or it is clear from context), tailor the answer:

- **Testing / QA**: Focus on test cases, preconditions, steps, and expected results. Surface untested scenarios from the ACs.
- **Product / PM**: Focus on AC definitions, feature behaviour, and what is or isn't specified.
- **Engineering**: Focus on system behaviour, edge cases, and deviations from spec.
- **Support**: Focus on how the feature behaves in the field, common confusion points from support articles.
- **Onboarding / Sales**: Focus on the user-facing flow and what the feature does for the end user.
- **New hires**: Start from `../wiki/product/` context, then link to specific features.

---

## Useful query patterns

- "What are the acceptance criteria for [feature]?"
- "What test cases exist for [feature]?"
- "What ACs for [feature] have no test coverage?"
- "What edge cases are documented for [feature]?"
- "Does [behaviour] match the AC or is it a deviation?"
- "What preconditions apply to [feature] tests?"
- "Are there any contradictions logged for [feature]?"
