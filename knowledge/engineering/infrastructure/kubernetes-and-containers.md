# Containers & Kubernetes

## Nền tảng
Image/registry, immutable tags/digests, namespace, pod, deployment, service, ingress/gateway, configmap, secret, PVC, RBAC, network policy, service account.

## Runtime quality
Readiness vs liveness vs startup probes; requests/limits; resource throttling/OOMKill; graceful shutdown, terminationGracePeriod; HPA, PDB, scheduling, topology spread.

## Security
Least-privilege RBAC, non-root, read-only root filesystem khi phù hợp, seccomp, restricted pod policy, image scanning, signed provenance khi dùng.

## Debugging an toàn (read-only)
`kubectl config current-context`, `kubectl get ns`, `kubectl get pods -A`, `kubectl describe pod ... -n ...`, `kubectl logs ... -n ... --previous`; kiểm tra đúng namespace/container.

## Deployment risks
Misconfigured probes, single replica, failed secret rotation, exhausted quota, wrong image tag, service DNS failure, incompatible schema rollout.

## Verification
Rollout status, observed readiness, error rate, trace, resource saturation, rollback drill.
