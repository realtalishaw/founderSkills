# Onboarding Task

## Overview

Route the founder into the right company-building path while keeping context light. This is an orchestration instruction, not a reusable skill. Ask only the questions needed for the selected branch, then hand off to the relevant next instruction or skill.

## Current Scope

The full onboarding flow starts with two paths:

1. Create a new company
2. Grow my company

For now, only continue the `Create a new company` path. If the user chooses `Grow my company`, say that path is planned but not active yet, then offer to help them create a new company.

## Skills for this task

The following skills can help. Read the file at the path when the skill is relevant.

<!-- INJECT: skills_index -->
**Task-specific skills:**

- **startup-idea-discovery**: Research-backed startup idea discovery for generating one specific, current, evidence-backed company idea with opportunity scoring, sourced keyword time-series graph, community signals, offer, market gap, and execution plan. Use when the founder chooses "come up with an idea for me" during onboarding, or when an agent needs to generate a fresh startup opportunity rather than evaluate a user's existing idea. — `instructions/onboarding/skills/startup-idea-discovery/SKILL.md`
<!-- /INJECT: skills_index -->

## Instructions

### Step 1: Choose Company Path

Ask the user:

1. Create a new company
2. Grow my company

If the user chooses `Create a new company`, continue to Step 2.

If the user chooses `Grow my company`, tell them that path is planned but not active yet, then offer to route them through the new-company path.

### Step 2: Choose Idea Path

Ask the user:

1. Come up with an idea for me
2. Build my idea

Use the answer to route the session.

### Step 3A: Come Up With An Idea For Me

Read `instructions/onboarding/skills/startup-idea-discovery/SKILL.md`.

Use that skill to research and present one startup idea card. The idea must be grounded in fresh market, keyword, community, competitor, and why-now signals.

After presenting the idea, ask whether the user wants to:

1. Use this idea
2. See another idea
3. Bring their own idea

If the user asks for another idea, use the same skill again. Do enough fresh research to avoid merely rewording the previous idea. Keep track of previously shown ideas and do not repeat the same market wedge unless the user asks to go deeper.

If the user chooses to use the idea, create `IDEA.md` using `instructions/onboarding/templates/IDEA.md`. Save the selected idea as an idea artifact, not a company artifact. Do not create `COMPANY.md` yet because the user has not named or defined the company.

### Step 3B: Build My Idea

Do not read the startup idea discovery skill for this branch.

Ask for:

- Idea summary
- Target customer
- Problem being solved
- Business model, if known
- Constraints such as budget, launch goals, geography, preferred tech, or founder skills

Then write a concise idea draft and ask the user to confirm or revise it. This branch will later hand off to market research, PRD, design, engineering, launch, and growth instructions.

When the user confirms their idea, create `IDEA.md` using `instructions/onboarding/templates/IDEA.md`. For user-provided ideas, fill unknown research fields as `TBD` and route the next instruction toward research/validation rather than inventing evidence.

## IDEA.md Artifact

Create `IDEA.md` only after the user commits to a generated idea or confirms their own idea. This artifact is the canonical idea snapshot for the next instructions in the MVP-building loop.

Use `instructions/onboarding/templates/IDEA.md` as the structure. Fill every section with either:

- confirmed user-provided information
- evidence from the startup idea discovery skill
- `TBD` for unknowns that need market research, validation, or user input

Do not treat `IDEA.md` as final company strategy. It is the bridge between onboarding and the deeper research/specification loop.

## Output Rules

- Keep onboarding conversational and decisive.
- Ask one routing question at a time.
- Do not overload the user with methodology.
- Use exact sources and dates when making research claims.
- Mark unknowns clearly instead of inventing metrics.
- Treat idea generation as live research, not prior-knowledge brainstorming.
