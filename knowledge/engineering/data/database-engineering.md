# Database Engineering — từ data ownership tới production

## Design
Schema ownership, keys/indexes, normalized vs denormalized, constraints, transaction boundaries, schema versioning, data classification.

## Performance
EXPLAIN/EXPLAIN ANALYZE khi được phép, selectivity, cardinality, compound indexes, covering indexes, lock/contention, N+1, connection pool, query timeout, partitioning theo evidence.

## Migration
Expand -> dual-read/write chỉ khi cần -> backfill có checkpoint -> contract; rollback/forward-fix và compatibility; không xoá cột trong cùng release khi consumer còn dùng.

## Operations
Backup restore test, retention, PII handling, replication lag, failover, hot partitions, capacity projection và access audit.

## Anti-patterns
Thêm index vô tội vạ; JSONB cho mọi field; SELECT *; coi read replica là read-your-writes; migration không đo lock time.
