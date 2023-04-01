#command
- **To understand creation**  :`Kubectl explain <object>`
- service can be given as svc
- When you delete rs the associated po-s will also be deleted
- Rolling update stratagy : how the deployment updates pods

# Check out
- **Liveness and readiness** Give liveness probe so that k8s can know if pod is healthy
- **Volume** path depends on which node has volume path and which node has pod, while **Persistant Volume** this doesn't happen. Utilise **persistant claim**