# DevOps-Deployment Practice

## Overview
The **DevOps-Deployment Practice** (The SRE Paradigm) focuses on extreme reliability in infrastructure. It treats the environment as a managed, versioned product.

## Core Mechanism
- **Isolation**: Every service is context-isolated.
- **Verification**: No deployment proceeds without a Layer 3 "Health Check" pass.
- **Rollback**: Every action in `execution/` has a defined reverse path.

## Standardized 3-Layer Structure
- [x] **directives/**: `deployment_spec.md` (Blueprint)
- [x] **execution/**: `deploy.ps1`, `verify_health.py`
- [x] **.tmp/**: Build logs and run-state metadata
- [x] **AGENTS.md**: Tailored SRE instructions

## Best Practices
- Never store secrets in `directives/`; use `.env` and `execution/` for injection.
- Use the `observability-engineer` skill for log analysis.
- Maintain a "Stitch Roadmap" to track how backend/frontend/db services interconnect.
