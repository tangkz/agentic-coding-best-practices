# ORCHESTRATION PLAN: [Complex Workflow]

## 1. Goal & Throughput Targets
Describe the mission and the performance requirements.
- **Workflow Goal:** [e.g., Process 100 research papers]
- **Target Parallelism:** [e.g., 5 concurrent agents]

## 2. Agent Fleet Definition
- **Agent A (The Scout):** [Role & Skills]
- **Agent B (The Analyst):** [Role & Skills]
- **Agent C (The Editor):** [Role & Skills]

## 3. Communication Protocol (Layer 3)
Define how agents pass data between each other.
- **Shared Memory:** [e.g., .tmp/workspace.json]
- **Hand-off Scripts:**
  - `execution/spawn_agent.py`: Triggers sub-agents.
  - `execution/consolidate_results.py`: Merges outputs.

## 4. Error Handling & Race Conditions
- [ ] Implement file locking for shared resources.
- [ ] Define retry logic for API timeout.
- [ ] Staggered start to avoid rate limits.

## 5. Self-Annealing Triggers
Identify when the "fleet" is drifting and how to re-sync.
- Trigger: Multiple sub-agent failures -> Action: Re-initialize parent orchestration script.
