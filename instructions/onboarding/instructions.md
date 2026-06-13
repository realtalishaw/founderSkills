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

- **startup-idea-discovery**: Research-backed startup idea discovery for generating one specific, current, evidence-backed company idea with opportunity scoring, keyword/community signals, offer, market gap, and execution plan. Use when the founder chooses "come up with an idea for me" during onboarding, or when an agent needs to generate a fresh startup opportunity rather than evaluate a user's existing idea. — `instructions/onboarding/skills/startup-idea-discovery/SKILL.md`
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

1. Explore this idea
2. See another idea
3. Bring their own idea

If the user asks for another idea, use the same skill again. Do enough fresh research to avoid merely rewording the previous idea. Keep track of previously shown ideas and do not repeat the same market wedge unless the user asks to go deeper.

If the user chooses to explore the idea, create a concise project brief draft and prepare to hand off to the next instruction in the MVP-building loop.

### Step 3B: Build My Idea

Do not read the startup idea discovery skill for this branch.

Ask for:

- Idea summary
- Target customer
- Problem being solved
- Business model, if known
- Constraints such as budget, launch goals, geography, preferred tech, or founder skills

Then write a concise project brief draft and ask the user to confirm or revise it. This branch will later hand off to market research, PRD, design, engineering, launch, and growth instructions.

## Output Rules

- Keep onboarding conversational and decisive.
- Ask one routing question at a time.
- Do not overload the user with methodology.
- Use exact sources and dates when making research claims.
- Mark unknowns clearly instead of inventing metrics.
- Treat idea generation as live research, not prior-knowledge brainstorming.
