# Resilience, High Availability & Disaster Recovery

## Failure assumptions
Network partition, partial outages, slow dependencies, broker backlog, stale cache, failover lag, region/AZ outage, certificate expiry, disk full, operator mistakes.

## Controls
Timeout budgets, bounded retry + exponential backoff/jitter, circuit breaker, bulkhead, backpressure, load shedding, queue DLQ/replay, idempotency, graceful degradation.

## Recovery
RTO/RPO phải gắn với use case; backup + restore drills; runbook, ownership, failover/failback plan, reconcile transactions; phân biệt HA với DR.

## Review
What happens if response is lost after commit? Do we know whether payment succeeded? Can we safely retry? Who reconciles stuck PENDING states?

## Cấm suy diễn
Có 3 replicas không đồng nghĩa HA; multi-AZ không đồng nghĩa DR; retries không thể bảo đảm exactly-once.
