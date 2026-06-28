# AI-Native Architecture Summary

PlotScope is designed as an AI-native application, not a normal writing app with an AI chat box added later.

The core design idea is that human edits and AI suggestions share a common review protocol.

## High-Level Flow

1. Read scoped state.
2. Create a snapshot.
3. Request an operation or candidate.
4. Validate the candidate.
5. Show it to the user.
6. Apply, reject, edit, or keep it as a suggestion.
7. Preserve provenance and review status.

## Why This Matters

Creative writing data is ambiguous. A character relationship, premise, plot point, or world rule can be useful even when it is not final. The product therefore separates:

- Draft text.
- AI candidate.
- User-edited value.
- User-approved canonical value.
- Locked value.

This avoids a common failure mode in AI writing tools: the model says something plausible, then the app silently treats it as truth.

## Model Boundary

The product is provider-agnostic by design.

The same frontend contract should work with:

- Deterministic fallback logic for demos.
- Local SLLM experiments.
- Fine-tuned open models.
- Remote API models.
- Future model routing or orchestration.

The frontend should not own provider secrets or call private provider endpoints directly.

