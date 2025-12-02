# Overview
This folder includes prompts that should be copy/pasted into your `docs/commands` folder and then used by tagging them in the chat (e.g. `@plan_feature.md`) and providing additional context.

These prompts are designed to simulate a full Software Development Life Cycle (SDLC) by assigning specific roles to the AI.

# Example Use

## Create Brief
**Role**: Product Manager
**Goal**: Create a comprehensive product brief (Project Overview, User Stories, etc.).
**Output**: `docs/PRODUCT_BRIEF.md`
```
@create_brief.md

We are building an application to help dungeon masters plan their D&D campaigns called Dragonroll. It will include tools like a random map generator, NPC generator, and loot generator.
```

## Plan Feature
**Role**: Tech Lead
**Goal**: Create a detailed technical plan (Files to change, Data Model, API changes).
**Output**: `docs/features/<N>_PLAN.md`
```
@plan_feature.md

We want to add a new page that is going to be our NPC generator. It should use the OpenAI API to generate descriptions and names, and DALL-E for images.
```

## Code Review
**Role**: Senior Code Reviewer
**Goal**: Review the implementation for correctness, quality, and security.
**Output**: `docs/features/<N>_REVIEW.md`
```
@code_review.md
@0001_PLAN.md
```

## Documentation Writing
**Role**: Technical Writer
**Goal**: Update the project documentation (README, Guides, JSDoc) to reflect changes.
**Output**: Updates to `docs/` or `README.md`.
```
@write_docs.md
@0001_PLAN.md
@0001_REVIEW.md
```