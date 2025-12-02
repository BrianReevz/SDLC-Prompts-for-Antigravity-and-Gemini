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

We are building an application to help people quickly gather opinions from a group called QuickPoll. It will include tools like a Simple Poll Creation Form, a Unique Shareable Voting Link Generator, and a Basic Real-Time Results Display.
```

## Plan Feature
**Role**: Tech Lead
**Goal**: Create a detailed technical plan (Files to change, Data Model, API changes).
**Output**: `docs/features/<N>_PLAN.md`
```
@plan_feature.md

We want to add a feature to prevent users from voting multiple times on the same poll. It should track votes based on the user's IP address. When a user tries to vote, the system should check if that IP has already submitted a vote for this specific poll ID. If they have, display a message saying 'You have already voted on this poll' instead of recording the vote.
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