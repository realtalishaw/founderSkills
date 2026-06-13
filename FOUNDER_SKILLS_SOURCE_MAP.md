# Founder Skills Source Map

Created: 2026-06-13

This repo turns MVP-builder style agent instructions into a harness-neutral Founder Skills instruction library.

## Repo Convention

Use this repo structure:

```text
instructions/
  {instruction-name}/
    instructions.md
    skills/
      {skill-name}/
        SKILL.md
```

Core loop steps are `instructions`. Reusable task-specific methods live under an instruction's `skills/` folder and should be loaded only when relevant.

## Source Pattern

The source inspiration came from an MVP-builder agent convention where each task had:

```text
instructions/{task}/instructions.md
instructions/{task}/skills/{skill-name}/SKILL.md
```

The important pattern to preserve is:

- `instructions.md` orchestrates the user/task flow.
- `skills/*/SKILL.md` contains reusable capability, methodology, scripts, or references.
- Skill indexes can be injected into instructions between `<!-- INJECT: skills_index -->` and `<!-- /INJECT: skills_index -->`.

## First Instruction

Start with onboarding:

`instructions/onboarding/instructions.md`

Current onboarding paths:

- Create a new company
- Grow my company, planned but not active

Current create-new-company branches:

- Come up with an idea for me
- Build my idea

When a founder commits to a generated idea or confirms their own idea, onboarding creates:

`IDEA.md`

Use the template:

`instructions/onboarding/templates/IDEA.md`

Do not create `COMPANY.md` during onboarding; the company has not been named or defined yet.

## First Skill

Startup idea discovery:

`instructions/onboarding/skills/startup-idea-discovery/SKILL.md`

This skill generates one research-backed startup idea card with:

- Title and description
- Opportunity, feasibility, problem, and why-now scores
- Keyword graph and insights
- Business fit
- Revenue potential
- Execution difficulty
- Go-to-market
- Community signals
- Top keywords
- Offer
- Proof and signals
- Market gap
- Result-based execution plan

The keyword graph should use sourced yearly time-series data. Try exact-volume sources first, including Semrush's free keyword volume checker, then fall back to Google Trends relative interest when exact volume is unavailable or blocked.

## Conversion Notes

- Do not turn every instruction into a skill.
- Use skills only for reusable capabilities that can support multiple instructions or branches.
- Keep instructions light and branch-oriented.
- Keep detailed methodology inside task-specific skills.
- Avoid time-based estimates in execution plans. Use result-based phases and proof milestones instead.
