# Acceptance Criteria: Microlearning Podcast

**Summary**: Defines how a podcast can be generated from within a microlearning article, its visibility, lifecycle, and behaviour.

**Sources**: `raw/bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf`

**Last updated**: 2026-05-25

---

## AC-MLP-01: Podcast option in microlearning article view

GIVEN a user is viewing a microlearning article
WHEN they look at the right panel of the article view
THEN a podcast generation option is displayed in that right panel

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

## AC-MLP-02: Creator chooses type and duration

GIVEN a user initiates podcast generation from a microlearning
WHEN they configure the podcast
THEN they select the podcast type (Monologue or Conversational) and set the desired duration

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

## AC-MLP-03: Private — only creator sees it

GIVEN a microlearning podcast is generated
WHEN other users view the microlearning or podcast lists
THEN the podcast is private and only visible to its creator

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

## AC-MLP-04: Deleting microlearning deletes podcast

GIVEN a microlearning has an associated podcast
WHEN the microlearning article is deleted
THEN the associated podcast is also deleted

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

## AC-MLP-05: Progress remembered

GIVEN a user starts listening to a microlearning podcast
WHEN they stop and return later
THEN their playback progress is remembered and they can resume from where they left off

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

## AC-MLP-06: Podcast icon in list only when generated

GIVEN a list of microlearning articles is displayed
WHEN a microlearning has an associated podcast generated
THEN a podcast icon appears next to that microlearning in the list; no icon is shown until a podcast exists

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

## AC-MLP-07: Cannot delete podcast alone

GIVEN a microlearning has an associated podcast
WHEN the user tries to delete the podcast independently (without deleting the microlearning)
THEN this is not permitted; the podcast can only be removed by deleting the parent microlearning

(source: bb0de7b9-a1c9-4ad8-8e58-fe4a3c5912c5_Microlearning_-_Podcast_.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[microlearning]]
- [[podcasts]]
