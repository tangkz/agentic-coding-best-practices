# DEPLOYMENT SOP: [Service Name]

## 1. Goal Description
Define the deployment target and specific version/branch.
- **Target Env:** [e.g., Staging / Production]
- **Services affected:** [List Docker services]

## 2. Pre-Deployment Validation (Layer 3)
- [ ] Run `execution/validate_config.ps1` to check syntax.
- [ ] Verify `.env` secrets are present and non-empty.
- [ ] Docker image integrity check.

## 3. The Deployment Step
- **Action:** `docker-compose up -d --build [service]`
- **Log Location:** `.tmp/deploy_[timestamp].log`

## 4. Post-Deployment Wellness (Layer 3)
- [ ] Run `execution/health_check.py` against the service endpoint.
- [ ] Monitor CPU/Memory spikes for 60 seconds.
- [ ] Verify logs for 5xx errors.

## 5. Rollback Strategy
If Wellness check fails:
- **Action:** `docker-compose rollback` or revert to previous tag.
- **Trigger:** Health-check timeout > 30s.
- **Update:** Update this SOP with the root cause of the failure.
