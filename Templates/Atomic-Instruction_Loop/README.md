# Practice 4: Atomic-Instruction Loop (The Incremental Paradigm)

## Overview
The atomic-instruction approach is a discipline-heavy practice where the developer breaks tasks into the smallest possible units of work to minimize agent error. It is ideal for critical production systems where regressions must be avoided at all costs.

## Core Mechanism
1. **Micro-Instruction Numbering:** Provide numbered, directly executable micro-instructions.
2. **Incremental Implementation:** Each step is implemented, tested, and staged before the next is initiated.
3. **Meticulous Context Management:** Moving inactive files out of the agent's reach to maintain peak performance and avoid "drift."

## Efficiency Gains
- Prevents "instruction drift" as the scope remains extremely narrow.
- Enables easy debugging when a single step fails.
- Maintains a high level of code quality and consistency.

## Template Steps

### Step 1: Sequential Task Decomposition
Break down the overall goal into a sequence of atomic units.
1. [Sub-task 1: e.g., Create database migration script]
2. [Sub-task 2: e.g., Update the schema]
3. [Sub-task 3: e.g., Implement the repository method]
4. [Sub-task 4: e.g., Write the unit test for the method]

### Step 2: Single-Unit Execution
Prompt the agent for ONLY the first step:
> "Complete Task #1: [Task Description]. Do not proceed to Task #2 until I have reviewed and approved the results."

### Step 3: Verification & Staging
Review the agent's implementation of the first step. Run relevant tests.
> "Task #1 is complete. Now proceed to Task #2: [Task Description]."

### Step 4: Iterative Loop
Repeat steps 2 and 3 until all sub-tasks are complete.

## Best Practices
- Never give the agent more than 3-5 sub-tasks at a time.
- Stage (e.g., git commit) after each successful sub-task.
- Reset the agent's context frequently to avoid historical interference.
