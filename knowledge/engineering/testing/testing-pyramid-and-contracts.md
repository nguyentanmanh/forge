# Test Strategy — chứng minh hành vi, không chỉ coverage

## Levels
Unit (domain invariants), integration (DB/broker), API/contract (consumer/provider), end-to-end (critical journeys), non-functional (load, resilience, security).

## Test dimensions
Happy path, validation failure, authorization denial, state misuse, idempotency/replay, concurrency, timeout-after-commit, retries, ordering, version compatibility, disaster recovery.

## Contract testing
Backward/forward compatibility, schema registry/evolution, nullability, pagination, HTTP error model, API version lifecycle.

## Quality gate
Link each high-risk requirement to a deterministic test; include negative/abuse tests; report not-run and flaky tests separately.

## Risk-based
Không buộc E2E mọi trường hợp; ưu tiên critical money/data state, boundaries và regressions.
