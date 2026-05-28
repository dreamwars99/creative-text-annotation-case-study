# Creative Text Annotation Case Study

This repository is a sanitized portfolio case study about structuring ambiguous creative text into reviewable AI data.

It does not contain the full product source code, production prompts, private taxonomy, model routing logic, provider settings, or user data. The goal is to show how I think about annotation design, evidence tracking, human review, and AI-assisted writing tools without exposing the unpublished product itself.

## What This Demonstrates

- Turning free-form creative input into structured labels.
- Designing a small factor / subelement taxonomy for narrative data.
- Separating AI candidates from human-approved canonical values.
- Tracking evidence, provenance, review status, and lock state.
- Writing annotation guidelines that reduce ambiguity.
- Defining validation checks for schema quality and human review quality.

## Portfolio Context

The case study is based on a private personal project about creative writing workflows. This public version is intentionally reduced to a small annotation slice:

- `concept.core_premise`
- `concept.narrative_question`
- `concept.logline`

The complete product design, full taxonomy, implementation details, and roadmap are private.

## Repository Map

- [case_study.md](./case_study.md): Product and annotation problem framing.
- [annotation_guideline_sample.md](./annotation_guideline_sample.md): Sample reviewer guideline.
- [candidate_schema_sample.json](./candidate_schema_sample.json): Minimal candidate JSON shape.
- [demo_flow.md](./demo_flow.md): End-to-end annotation flow.
- [validation_process.md](./validation_process.md): Suggested QA and validation checks.
- [screenshots/README.md](./screenshots/README.md): Placeholder for sanitized images only.

## Safety Boundary

This repo intentionally excludes:

- Full source code.
- Internal prompts.
- Full factor taxonomy.
- Agent/orchestrator architecture.
- Provider, API, RunPod, or model deployment details.
- Real user content.
- Product roadmap details.

## Rights

Copyright (c) 2026 dreamwars99. All rights reserved.

This repository is public for portfolio review only. No license is granted to copy, modify, redistribute, or use this material in another product.
