# Spec-Driven Rules

## Architectural Integrity
- All new features MUST be added to `architecture.md` first.
- If the agent discovers a better implementation method than the spec, it must request a spec update before proceeding.

## Implementation Standards
- Use modular architecture patterns (MVC, Hexagonal, etc.) as defined in the spec.
- Variable naming and file structure must follow the conventions specified in `architecture.md`.

## Mandatory Checkpoints
- Require human review for any change that deviates from the approved `implementation_plan.md`.
- Implementation plans MUST include a "Spec Alignment" section.
