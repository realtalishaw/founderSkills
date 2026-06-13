# Founder Skills

Founder Skills is an open-source instruction library for AI agent harnesses that help founders go from an initial company direction to a usable MVP.

The project separates:

- `instructions/`: orchestration steps in the founder/MVP-building loop
- `instructions/**/skills/`: reusable task-specific skills that an instruction can load only when needed

## Current Draft

The first instruction is onboarding:

- `instructions/onboarding/instructions.md`

It currently supports the `Create a new company` path and branches into:

- `Come up with an idea for me`
- `Build my idea`

The first reusable skill is:

- `instructions/onboarding/skills/startup-idea-discovery/SKILL.md`

## Design Principle

Core loop steps are instructions, not skills. Skills should be reusable capabilities that can support multiple instructions or be loaded conditionally inside an instruction.

## License

License TBD.
