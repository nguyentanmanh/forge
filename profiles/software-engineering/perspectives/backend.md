# Góc nhìn — Backend Engineering

## Khi sử dụng
Thiết kế, triển khai hoặc đánh giá API, xử lý nghiệp vụ backend, database, messaging và tính ổn định của dịch vụ.

## Trọng tâm đánh giá
- Domain boundaries, contracts, validation và versioning.
- Transaction boundary, consistency, concurrency, isolation, idempotency.
- Retry, backoff, timeout, duplicate messages, ordering, DLQ, partial failure.
- Schema migration, indexing, query plan, caching, khả năng khôi phục.
- Authentication, authorization, secrets, audit, PII.
- Metrics, logs, tracing, SLO, deploy và rollback.

## Các câu hỏi then chốt
1. Dữ liệu nào là nguồn sự thật; ai sở hữu cập nhật?
2. Khi request bị timeout nhưng downstream đã xử lý thì sao?
3. Khi retry/duplicate/concurrent requests xảy ra, trạng thái có còn đúng?
4. Làm thế nào kiểm thử và quan sát lỗi trong môi trường thực tế?

## Skills phù hợp (chọn theo task)
`api-design`, `database-design`, `integration-design`, `code-review`, `test-strategy`, `debugging`, `performance-review`, `security-review`.

> Đây là **góc nhìn review**, không phải quy trình thay thế SKILL.md.
