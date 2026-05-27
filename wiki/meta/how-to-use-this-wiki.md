# Meta: How to Use This Wiki

**Summary**: Prompt patterns and navigation guide for each role.

**Last updated**: 2026-05-25

---

## Navigation

Always start with `wiki/index.md` to find the page you need. From there, follow wiki-links (`[[page-name]]`) to related pages.

## Role-specific prompt patterns

### QA / Testing
- "What test cases exist for [feature]?" → Read `wiki/features/<feature>/test-coverage.md`
- "What are the preconditions for testing real call scoring?" → Read `wiki/features/real-call-scoring/test-coverage.md`
- "What behaviours are specified but not tested?" → Compare `ac.md` against `test-coverage.md`
- "What are the edge cases for podcast generation?" → Read `wiki/features/podcasts/test-coverage.md`
- Full guide: `wiki/audiences/for-testing.md`

### Product / PM
- "What does [feature] do?" → Read `wiki/features/<feature>/overview.md`
- "What are the acceptance criteria for Custom Scorecards?" → Read `wiki/features/custom-scorecards/ac.md`
- "What contradictions exist between sources?" → Read `wiki/contradictions.md`
- Full guide: `wiki/audiences/for-pm.md`

### Engineering
- "How is avg score calculated for simulations?" → Read `wiki/features/simulation-reports/overview.md`
- "What's the difference between HubSpot and MS Dynamics real call scoring?" → Read `wiki/features/real-call-scoring/overview.md`
- "What are the reminder email rules?" → Read `wiki/features/due-date-notifications/overview.md`
- Full guide: `wiki/audiences/for-engineering.md`

### Support
- "Learner is not receiving reminders" → Read `wiki/features/due-date-notifications/overview.md`
- "Real call scoring not triggering" → Read `wiki/features/real-call-scoring/overview.md`
- "Scorecard deleted — impact?" → Read `wiki/features/custom-scorecards/overview.md`
- Full guide: `wiki/audiences/for-support.md`

### New hires
- Start with: `wiki/audiences/for-new-hires.md`
- Then: `wiki/product/heysales-overview.md`, `wiki/product/user-roles.md`, `wiki/product/learning-types.md`

### Sales / Onboarding
- Full guide: `wiki/audiences/for-onboarding.md`

## Adding to the wiki

When the user provides a new source document:
1. Claude reads it and identifies the source type (AC / support article / test case)
2. Claude discusses key takeaways
3. Claude creates or updates feature pages under `wiki/features/`
4. Claude updates `wiki/index.md`, `wiki/log.md`, `wiki/contradictions.md`, and `wiki/usage.md`

## Lint / audit

Ask Claude to "lint the wiki" to find:
- Orphan pages (no inbound links)
- Missing citations
- Outdated claims based on newer sources
- Contradictions between pages
- Format compliance issues

## Related pages

- [[content-standards]]
- [[index]]
