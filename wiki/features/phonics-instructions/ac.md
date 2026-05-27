# Acceptance Criteria: Phonics Instructions

**Summary**: Defines how users add, preview, and manage phonetic spellings for words in podcasts.

**Sources**: `raw/38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf`

**Last updated**: 2026-05-25

---

## AC-PI-01: Add phonetic spelling of a word

GIVEN a user is in the podcast Edit Studio
WHEN they add a phonetic instruction
THEN they can enter the word and its phonetic spelling, which will override how that word is pronounced

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

## AC-PI-02: Global application across podcasts

GIVEN a phonetic instruction is saved for a word
WHEN any podcast containing that word is played
THEN the word is pronounced according to the saved instruction across all podcasts — not only the one being edited

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

## AC-PI-03: Preview before saving

GIVEN a user has entered a word and its phonetic spelling
WHEN they choose to preview
THEN the system plays back the pronunciation so the user can confirm it before saving

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

## AC-PI-04: Phonics guide for managing instructions

GIVEN a user has saved one or more phonetic instructions
WHEN they access the phonics guide
THEN all saved instructions are listed and can be deleted at any time

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

## AC-PI-05: Edit phonics button in Edit Studio

GIVEN a user is in the podcast Edit Studio
WHEN they look at the right side panel (next to the transcript tab)
THEN an "edit phonics" button is visible; clicking it opens the phonics instruction guide on the left side

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

## AC-PI-06: Instance count shown while adding

GIVEN a user is adding a phonetic instruction for a word
WHEN they type the word
THEN the system shows how many instances of that word appear across how many podcasts

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

## AC-PI-07: Pronunciation applied immediately after saving

GIVEN a user saves a phonetic instruction
WHEN they play any podcast containing that word
THEN the word is pronounced according to the instruction

(source: 38c38369-082f-47e8-865c-be38ac9ae87d_Phonics_Instructions.pdf)

---

## Related pages
- [[overview]]
- [[podcasts]]
