# Validation Process

This document describes how I would evaluate the quality of a creative text annotation workflow.

## 1. Schema Validation

Every candidate should pass a strict schema check.

Required checks:

- known `factorId`,
- known `subelementId`,
- non-empty candidate text,
- at least one evidence quote,
- valid review state,
- no extra unknown fields.

## 2. Evidence Quality

A candidate is weak if it cannot point back to source text.

Suggested reviewer questions:

- Does the quote directly support the candidate?
- Is the quote too broad?
- Is the candidate inventing information not present in the quote?
- Would another reviewer understand the same label from this evidence?

## 3. Label Boundary Review

Some labels overlap. For example, a sentence can imply both a core premise and a narrative question.

The review process should track:

- common confusion pairs,
- multi-label acceptance cases,
- rejected over-labeling,
- and examples that require guideline updates.

## 4. Human Review Metrics

Useful metrics:

- schema valid rate,
- evidence hit rate,
- human acceptance rate,
- edit rate,
- rejection rate,
- disagreement rate between reviewers,
- locked value overwrite attempts.

## 5. Safety Review

Inputs should be checked for:

- meaningless text,
- pure profanity,
- targeted harassment,
- real-person mockery,
- real victim mockery,
- illegal instruction requests,
- and unsafe transformation into a creative premise.

Dark fictional material should be reviewed by context, not rejected automatically.

## 6. Regression Examples

Maintain a small set of examples that should not change behavior unexpectedly.

Example regression set:

| Input Type | Expected Behavior |
| --- | --- |
| Clear premise | Create `concept.core_premise` candidate |
| Moral tension | May create `concept.narrative_question` candidate |
| Mood only | Low confidence or reject |
| Plot invented by model | Reject |
| No evidence quote | Reject |

## 7. Why This Matters

For creative AI tools, annotation is not just classification. It is a product-quality layer.

Good annotation should help the system suggest better options while keeping the human creator in control.
