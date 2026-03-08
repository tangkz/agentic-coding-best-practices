---
description: Deploy services and verify health
---

// turbo
1. Run `execution/validate_config.py` to check YAML/ENV integrity.
2. Execute `execution/deploy.ps1 --env=dev`.
3. Monitor `.tmp/deploy_logs.txt`.
4. Run `execution/verify_health.py` to check cross-service connectivity.
5. Signal success to the human once all services report "Ready".
