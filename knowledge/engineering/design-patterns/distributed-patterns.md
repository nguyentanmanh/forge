# Distributed Patterns — giới hạn bảo đảm

## Patterns
Transactional Outbox, Inbox/deduplication, Saga, CQRS, Event Sourcing, Bulkhead, Circuit Breaker, Retry with jitter, Timeout budget, Rate limiting, Cache-aside, Anti-corruption Layer.

## Cảnh báo quan trọng
- At-least-once delivery nghĩa là consumer cần idempotent, không có end-to-end exactly-once mặc định.
- Idempotency key phải gắn với requester, operation và semantic payload; request cùng key khác payload => conflict.
- Retry chỉ khi biết operation idempotent hoặc có cơ chế reconciliation; không retry vô hạn.
- Saga compensation là business action, không phải database rollback nguyên tử.
- Event Sourcing tăng complexity: replay, schema evolution, GDPR/retention, snapshots.

## Validation
Duplicate delivery, out-of-order, timeout after commit, broker outage, slow consumer, poison message, partial failure và reprocessing phải được kiểm thử.
