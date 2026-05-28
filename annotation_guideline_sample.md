# Annotation Guideline Sample

This is a reduced sample guideline for creative text annotation. It is designed to show judgment, not to expose a full production taxonomy.

## Reviewer Objective

Given a short creative seed, identify whether it clearly supports one or more sample labels:

- `concept.core_premise`
- `concept.narrative_question`
- `concept.logline`

Every accepted label must include evidence from the source text.

## Label Definitions

### `concept.core_premise`

Use this label when the input expresses the smallest condition that makes the story possible.

Good signal:

- a central impossible / unusual / charged condition,
- a conflict that naturally generates story pressure,
- a premise that can guide later characters, plot, or theme.

Do not use when:

- the input is only a mood,
- the input is only a genre tag,
- the candidate invents a new world rule not present in the text.

### `concept.narrative_question`

Use this label when the input implies a question the story can keep testing.

Good signal:

- moral uncertainty,
- relationship tension,
- unresolved pressure,
- a question that could guide scenes or plot turns.

Do not use when:

- the question is too generic,
- the question is only a restatement of the genre,
- the candidate adds a new theme with no evidence.

### `concept.logline`

Use this label only when the input contains enough information to form a compact story direction.

Good signal:

- a protagonist or central force,
- a pressure or obstacle,
- a visible direction of action.

Do not use when:

- there is no actor,
- there is no pressure,
- the sentence would require inventing a plot.

## Evidence Rules

Each candidate should include at least one evidence quote.

Evidence should be:

- short,
- directly tied to the candidate,
- copied from the source text,
- not a summary written by the annotator.

If the source text is too vague, mark the candidate as low confidence or reject it.

## Multi-Label Rule

Multi-label annotation is allowed when one source sentence clearly supports more than one label.

Example:

> A created life asks its creator to take responsibility.

Possible labels:

- `concept.core_premise`
- `concept.narrative_question`

Avoid forcing a single label when the text genuinely contains multiple functions.

## Rejection Rules

Reject or request rewrite when the input is:

- meaningless filler,
- only profanity,
- targeted harassment,
- real-person mockery,
- explicit celebration of real harm,
- or too vague to support any useful annotation.

Dark fictional subject matter is not automatically rejected. The key question is whether the input can be transformed into a safe, fictional creative premise.

## Reviewer Actions

| Action | Meaning |
| --- | --- |
| `apply` | Candidate is accurate enough to use. |
| `edit` | Candidate is useful but needs human wording. |
| `reject` | Candidate is unsupported or unsafe. |
| `lock` | Approved value should not be overwritten by future AI output. |

## Quality Bar

A good candidate should be:

- faithful to the source,
- specific enough to guide future writing,
- not overloaded with plot invention,
- supported by evidence,
- and understandable to another reviewer.
