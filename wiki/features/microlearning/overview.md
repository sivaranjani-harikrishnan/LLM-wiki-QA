# Feature: Microlearning (Let's Learn)

**Summary**: Let's Learn is a private, per-user AI article generator accessible to all HeySales users regardless of role. Users submit prompts and source assets to generate personal learning articles.

**Sources**: `Microlearning - Sheet1.csv`

**Last updated**: 2026-05-25

---

## What it does

The Let's Learn module allows every HeySales user to generate a private AI article from their own content (documents, URLs) and a natural-language prompt. The article is strictly private — no admin or manager can see it. Users can also generate a private audio podcast from the article.

## Who uses it

- **All users**: Including learners, admins, and content publishers — all can use Let's Learn
- **No admin visibility**: Articles and podcasts generated in Let's Learn are private to the user who created them

## How it works

### Accessing Let's Learn
- Let's Learn is always visible in the HeySales left panel for all users regardless of role
- Access is NOT gated by HeySales enablement for learners (all users see it)

### Article generation
1. User enters a prompt in the input field
2. User adds up to 5 source assets:
   - Supported: PDF, DOC, PPT (paged); URL, CS Storyboards (link-type)
3. Both prompt AND assets are required to generate an article
4. Invalid prompt → validation error shown
5. Article generates; History pane records the prompt

### History pane
- Shows all modification prompts in sequence
- User can switch between versions (previous versions restored on click)
- Last modified version is shown by default
- Parent (original) prompt shown separately in history

### Working with articles
- Users can start a new learning from the home page
- Users can delete an article from the home page
- On deletion, all associated data (including any generated podcast) is removed

### Error handling
- Failed asset → entire generation fails (not partial)

## Privacy rules

- Articles are strictly private to the generating user
- No manager, admin, or other user can view another user's Microlearning articles or podcasts
- This is fundamentally different from admin-created podcasts that are assignable

## Asset limits

- Maximum 5 assets per article generation
- Supported: PDF, DOC, PPT, URL, CS Storyboards
- SCORM, images, videos, ZIP, and Excel are not supported

## Microlearning Podcast

From any generated article, the user can generate a private audio podcast. See [[microlearning-podcast]].

## Related pages

- [[test-coverage]]
- [[microlearning-podcast]]
- [[podcasts]]
- [[learning-types]]
