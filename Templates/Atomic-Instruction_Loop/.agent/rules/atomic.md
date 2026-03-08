# Atomic Rules

## Step Precision
- Do NOT proceed to step `N+1` until step `N` is verified and marked as `[x]` in `task.md`.
- Changes to multiple files in a single tool call are discouraged unless strictly necessary.

## Context Control
- Move inactive files out of the active workspace or ignore them to keep token usage efficient.
- Reset the agent session if the conversation history exceeds 20 messages.

## Error Handling
- On any error, the agent must "Self-Anneal": Fix, Test, and then Update the instructions if needed.
