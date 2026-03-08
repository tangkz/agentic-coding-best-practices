---
description: Delegate a specific task to a sub-agent
---

// turbo
1. Define the task in `directives/tasks/[task_id].md`.
2. Use an `execution/` script to initialize a new workspace context.
3. Dispatch the specialized agent with the task directive.
4. Monitor logs in `.tmp/` for completion artifacts.
