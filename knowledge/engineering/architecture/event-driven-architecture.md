# Event-Driven Architecture (EDA)

## 1. Mục đích
Các thành phần giao tiếp bằng sự kiện/thông điệp bất đồng bộ để giảm coupling về thời điểm thực thi, cho phép nhiều consumer và mở rộng độc lập. EDA không mặc định đem lại consistency mạnh hoặc exactly-once end-to-end.

## 2. Khi nên dùng
- Một sự kiện nghiệp vụ cần được nhiều hệ thống tiêu thụ độc lập.
- Tác vụ có thể xử lý bất đồng bộ và chấp nhận eventual consistency.
- Cần decouple producer/consumer, xử lý tải không đồng đều và retry có kiểm soát.

## 3. Khi tránh
- Người dùng cần câu trả lời xác nhận tức thì về giao dịch quan trọng.
- Chuỗi sự kiện dài khiến trace/debug/compensation khó hơn giá trị đem lại.
- Nhiệm vụ chỉ là request/response đơn giản, không có ích lợi thật từ broker.

## 4. Thiết kế cần làm rõ
1. Event taxonomy: domain event, integration event, command, notification (không đánh đồng).
2. Event ownership, schema/versioning, compatibility, PII/data minimization.
3. Delivery semantics: at-least-once thường yêu cầu idempotent consumer; không giả định exactly-once business effect.
4. Ordering, partition key, replay, late/out-of-order delivery.
5. Database-to-broker atomicity: transactional outbox hoặc lựa chọn có bằng chứng.
6. Retry/backoff, DLQ, poison messages, max attempts, deduplication.
7. Observability: correlation ID, trace, consumer lag, failure metrics, reconciliation.
8. Security, retention, access control, data deletion obligations.

## 5. Ví dụ Payment
`Payment Service` commit transaction và bản ghi outbox trong cùng database transaction. Publisher chuyển outbox thành `PaymentCompleted` integration event. Consumer cập nhật read model/notifies partner bằng handler idempotent. Cần thiết kế rõ trạng thái eventual consistency và reconciliation khi callback thất bại.

## 6. Trade-offs
Ưu: temporal decoupling, fan-out, resilience khi thiết kế đúng. Nhược: ordering, duplicates, debugging, contract evolution, data consistency và vận hành broker.

## 7. Verification
Thử ít nhất: duplicate event, crash sau commit trước publish, crash sau xử lý trước ack, delay/out-of-order, consumer down, replay, schema evolution, DLQ recovery.
