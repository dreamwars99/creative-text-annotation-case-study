# Character Relationship AI Case Study

Character relationships are not just lines between names. In narrative work, a relationship can carry emotional debt, power imbalance, secret knowledge, dependency, guilt, rivalry, or unresolved obligation.

The relationship map MVP separates canonical relationship data from AI-generated candidate edges.

## Example Candidate Fields

- source character
- target character
- relationship label
- tone
- intensity
- evidence note
- confidence
- review status

## Why Candidate Review Matters

An AI model can infer a relationship that is useful but not fully true. For example, two characters may look hostile in one chapter but actually be hiding a mutual obligation.

PlotScope therefore treats relationship AI as a candidate generator, not an automatic graph mutator.

## MVP Boundary

The public case study describes:

- candidate data transfer shape
- deterministic fallback for demos
- review-first direction

It intentionally excludes:

- private production graph source code
- full internal taxonomy
- private prompt chain
- unpublished story material

