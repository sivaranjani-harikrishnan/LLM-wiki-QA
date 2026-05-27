# Test Coverage: Microlearning (Let's Learn)

**Summary**: 31 test cases covering Let's Learn module visibility, article generation, asset management, history, privacy, and error handling.

**Sources**: `Microlearning - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Key TCs

### Module access (TC0001–TC0003)
- TC0001: Let's Learn module is visible to ALL users regardless of role (admin, learner, CP, BI analyst)
- TC0002: Input field and Add button layout
- TC0003: Module appears in HeySales left panel for all roles

### Asset management (TC0004–TC0009)
- TC0004: Supported asset types — paged: PDF, DOC, PPT; link: URL, CS Storyboards
- TC0005: 5-asset maximum enforced
- TC0006: Attempting >5 assets shows error
- TC0007: Unsupported assets cannot be added
- TC0008: Asset removed from list when deleted
- TC0009: Asset sources: Streams & Collections + URL entry

### Article generation (TC0010–TC0016)
- TC0010: Both prompt AND assets required; generating without either shows error
- TC0011: Invalid prompt → validation error
- TC0012: Article generates on valid prompt + assets
- TC0013: Failed asset causes entire generation to fail (not partial)
- TC0014: Generation progress shown while generating
- TC0015: Generated article displayed after completion
- TC0016: "Start new learning" button available from home page

### History pane (TC0017–TC0022)
- TC0017: History pane shows all modification prompts in sequence
- TC0018: Parent (original) prompt shown separately in history
- TC0019: User can switch between versions by clicking in history
- TC0020: Last modified version is shown by default
- TC0021: Switching versions restores that version's article
- TC0022: History persists across sessions

### Privacy (TC0023–TC0027)
- TC0023: Article is private — not visible to other users
- TC0024: Admin cannot see another user's Microlearning articles
- TC0025: Manager cannot access learner's Microlearning content
- TC0026: Article not visible in any admin report or dashboard
- TC0027: Microlearning podcast (if generated) is also private

### Delete and management (TC0028–TC0031)
- TC0028: User can delete an article from the home page
- TC0029: Deleting an article removes all associated data
- TC0030: Deleted article no longer appears in history
- TC0031: "Start new learning" resets the generation flow

---

## Related pages

- [[overview]]
- [[microlearning-podcast]]
