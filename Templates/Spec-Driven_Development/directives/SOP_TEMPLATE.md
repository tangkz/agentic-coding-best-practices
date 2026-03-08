# SOP: [Feature/System Name]

## 1. Goal Description
Clearly define what this system or feature is intended to achieve.

## 2. Architecture & Data Model
- **Entities:** [List the main data objects]
- **API Spec:** [Define the inputs/outputs]
- **Constraints:** [List technical limitations or requirements]

## 3. Automation Flow (Layer 3)
Define which scripts in `execution/` are used for this SOP.
- `execution/validate_architecture.py`: Verifies current state.
- `execution/deploy_change.py`: Implements the change.

## 4. Verification Plan
- [ ] Unit Test Coverage >= 80%
- [ ] API Documentation updated
- [ ] Health-check pass

## 5. Drift Detection & Self-Annealing
Identify common failure points for this spec and define recovery triggers.
