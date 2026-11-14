# Design Pattern Selection — quyết định từ problem, không từ tên pattern

## Decision flow
1. Viết rõ vấn đề hiện tại và nguyên nhân; lưu evidence.
2. Xác định điểm thay đổi, lifecycle, ownership, NFR.
3. So sánh cách đơn giản trước khi đưa pattern.
4. Chọn pattern theo trade-off; đưa failure mode và test kiểm chứng.
5. Không giới thiệu quá 1–2 pattern nếu chưa có nhu cầu.

| Problem | Pattern cân nhắc | Khi KHÔNG nên | Rủi ro |
|---|---|---|---|
| 2+ provider khác protocol | Adapter / ACL | Chỉ một provider có contract ổn định | Mapping lỗi và version drift |
| Chính sách routing thay đổi | Strategy | Chỉ một if đơn giản | Quá nhiều implementation |
| Đối tượng khởi tạo phức tạp | Builder / Factory Method | Constructor/record đủ rõ | Ẩn invariant |
| Pipeline validation linh hoạt | Chain of Responsibility | Thứ tự cố định, ít bước | Khó debug thứ tự |
| Decorate behavior cross-cutting | Decorator | AOP sẵn và đơn giản hơn | Side effects khó thấy |
| Observer in-process | Observer | Giao dịch liên hệ chặt | Events chạy trước commit |
| Sync DB + publish event | Transactional Outbox | Không có reliability requirement | Duplicate publish, relay backlog |
| Call lặp lại | Idempotency Key | Pure read không side effect | Scope key/TTL không đúng |
| Multi-step distributed workflow | Saga / process manager | Local transaction đủ | Compensation không đảo ngược hoàn toàn |
| Read/write scale khác nhau | CQRS | CRUD nhỏ, cùng model đủ | Consistency, vận hành phức tạp |
| Dependency lỗi liên tục | Circuit Breaker | Không có đo đạc lỗi/phục hồi | Open quá lâu, fail-open sai |

## Review questions
Pattern giải quyết vấn đề đo được nào? Ai sở hữu state? Tính nhất quán nào được đảm bảo? Có giản lược được không? Plan gỡ pattern nếu không còn phù hợp?
