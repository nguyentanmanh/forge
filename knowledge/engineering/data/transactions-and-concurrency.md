# Transactions & Concurrency

## Kiến thức cần vận dụng
ACID cục bộ, isolation levels, optimistic/pessimistic locking, compare-and-set, uniqueness constraint, lost update, write skew, deadlock, retry boundaries, pagination race, outbox.

## Use cases
- Approve payment: atomic transition PENDING -> APPROVED dựa trên expected version, quyền và nội dung đã duyệt.
- Double submit: unique business key + idempotency record trước external call.
- Reserve inventory: atomic decrement/conditional update.
- Balance transfer: không giả định distributed ACID xuyên các hệ thống.

## Failure matrix
Concurrent requests cùng key; request retry sau network timeout; DB commit thành công nhưng response mất; worker xử lý lại; reorder; stale read; deadlock retry; outbox lag.

## Proof
Định nghĩa invariant rồi chứng minh bằng DB constraints + atomicity + deterministic tests + concurrent integration test.
