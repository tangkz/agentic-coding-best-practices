# Orchestration Rules

## Task Delegation
- Every delegated task MUST have a clear input and expected output artifact.
- Agents must not modify the same file concurrently without a synchronization plan.

## Milestone Management
- Update the global `roadmap.md` after every successful agent task completion.
- Significant roadblocks in one work stream must be reported to the orchestrator immediately.

## Review Policy
- Use the "Agent-Driven" review policy for non-critical parallel tasks.
- Critical integrations require "Human-in-the-Loop" approval.
