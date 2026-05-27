# Acceptance Criteria: Microlearning

**Summary**: Defines how microlearning articles are created, what inputs are accepted, and what the output looks like.

**Sources**: `raw/4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf`

**Last updated**: 2026-05-25

---

## AC-ML-01: Normal users can create microlearnings

GIVEN a normal user (rep, not just admin) is logged in
WHEN they navigate to the microlearning creation area
THEN they have the ability to create a new microlearning article (creation is not restricted to admins)

(source: 4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf)

## AC-ML-02: Input is text document plus learning objective query

GIVEN a user is creating a microlearning
WHEN they provide inputs
THEN they supply a text document (the source material) and a learning objective query describing what the microlearning should focus on

(source: 4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf)

## AC-ML-03: Output is a 1-pager article in sections

GIVEN valid inputs are submitted
WHEN the system generates the microlearning
THEN the output is a concise 1-page article structured in labelled sections

(source: 4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf)

## AC-ML-04: Irrelevant query results in failure with error

GIVEN a user submits a learning objective query that is irrelevant to the provided document
WHEN the system processes the request
THEN generation fails and an error message is shown (not a generic article)

(source: 4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf)

## AC-ML-05: No Seek-style AI queries supported

GIVEN a user is in the microlearning creation flow
WHEN they interact with the learning objective field
THEN open-ended AI "Seek" queries (like those in scorecard generation) are not supported; the field is a direct text input only

(source: 4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf)

## AC-ML-06: No strict word count limit

GIVEN the system generates a microlearning article
WHEN determining article length
THEN there is no strict word count ceiling; the article length is determined by the content and learning objective

(source: 4f204d17-1744-4378-a64c-232450c14e66_Microlearning_-_Phase_1.pdf)

---

## Related pages
- [[overview]]
- [[test-coverage]]
- [[microlearning-podcast]]
