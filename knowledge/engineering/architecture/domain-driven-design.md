# Domain-Driven Design (DDD)

## 1. DDD giải quyết gì?
Ưu tiên mô hình hóa nghiệp vụ phức tạp, tạo *ubiquitous language* giữa chuyên gia nghiệp vụ và kỹ thuật. Tách *strategic design* (subdomains, bounded contexts, context mapping) khỏi *tactical design* (entities, value objects, aggregates, domain events, repositories, domain services).

## 2. Khi nên dùng
- Nghiệp vụ có nhiều quy tắc, ngoại lệ, bất biến (*invariants*) và từ vựng dễ mâu thuẫn.
- Nhiều luồng xử lý có ownership và ranh giới khác nhau; code nghiệp vụ khó duy trì.
- Có sự tham gia đều đặn của domain experts để xác minh mô hình.

## 3. Khi không nên dùng đầy đủ
- CRUD đơn giản, mapping DB gần như 1–1, không có business rules đặc biệt.
- Team chưa hiểu domain nhưng lại bắt đầu tạo nhiều aggregate/repository abstract.
- Chỉ muốn chia microservices (DDD không đồng nghĩa microservices).

## 4. Quy trình áp dụng
1. Ghi use cases, thuật ngữ và invariants với domain experts.
2. Xác định subdomains và bounded contexts; không mặc định mỗi service là một bounded context.
3. Vẽ context map: upstream/downstream, translation, integration contracts.
4. Chọn aggregate boundary theo invariant cần bảo vệ trong transaction.
5. Phân biệt entity, value object, domain service và application service.
6. Kiểm chứng model qua examples và các trạng thái lỗi, cạnh tranh đồng thời.

## 5. Ví dụ khái niệm: Payment
- `Payment` có thể là aggregate root nếu các cập nhật trạng thái và giới hạn cần nhất quán trong một boundary.
- Bất biến ví dụ: một payment không được chuyển từ trạng thái hoàn tất sang trạng thái khởi tạo tùy tiện.
- `PaymentCompleted` có thể là domain event **nội bộ**; phát hành ra broker cần thiết kế integration event, schema, idempotency và transaction outbox riêng.
- Không mặc định payment aggregate sở hữu Ledger hoặc Account: ownership phải xác định bằng nghiệp vụ thực tế.

## 6. Anti-patterns
- DDD = tạo thư mục `domain/` và nhiều interface.
- Aggregate quá lớn, khóa đồng thời không cần thiết.
- Trùng business logic giữa application service, aggregate và database triggers.
- Dùng tên hệ thống kỹ thuật làm bounded context mà không hiểu ngôn ngữ nghiệp vụ.

## 7. Verification
Có glossary được thống nhất? Invariants có test? Aggregate có transaction boundary rõ? Bounded contexts có contract, owner và failure cases?
