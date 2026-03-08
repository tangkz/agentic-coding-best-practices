# ATOMIC SOP: [Task Name]

## 1. The Atomic Goal
Define the single, smallest unit of work to be performed.
- **Objective:** [e.g., Update a single DB column]
- **Verification:** [How to prove it worked?]

## 2. Pre-Flight Checklist
- [ ] Read current state using `view_file` or `execution/check_state.py`.
- [ ] Verify environment variables in `.env`.

## 3. The Execution Step (Layer 3)
Define the exact script and parameters.
- **Tools:** `execution/run_atomic_task.py --task update_col`

## 4. Post-Flight Verification
- [ ] Run `execution/verify_output.py`.
- [ ] Log status to `.tmp/atomic_log.json`.

## 5. Self-Annealing Strategy
If verification fails:
- **Action:** Re-read state -> Patch script -> Re-run.
- **Update:** If failure was due to environment, update this SOP's Pre-Flight checklist.
