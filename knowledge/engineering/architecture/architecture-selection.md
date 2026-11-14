# Lựa chọn kiến trúc — Decision Guide

## 1. Trước khi chọn pattern
Ghi mục tiêu, yêu cầu chức năng, business invariants, dữ liệu, thành phần hiện hữu, SLA/SLO, throughput, latency, consistency, khả năng vận hành, năng lực team, deadline và constraints. Những thông tin chưa có phải ghi là *chưa xác minh*.

## 2. Heuristics
| Tình huống | Cân nhắc | Không nên mặc định |
|---|---|---|
| CRUD nhỏ, business rules ít | Modular monolith/layered architecture | DDD đầy đủ, microservices |
| Nghiệp vụ phức tạp, nhiều thuật ngữ dễ hiểu nhầm | DDD strategic design; bounded contexts | Mỗi entity DB thành một aggregate |
| Logic nghiệp vụ cần kiểm thử, framework thay đổi | Clean/Hexagonal ports-adapters | Tạo abstraction cho mọi class |
| Nhiều consumer cần phản ứng độc lập với sự kiện | Event-driven (pub/sub, outbox) | Giao dịch đồng bộ bằng hàng loạt event |
| Yêu cầu xác nhận tức thì và consistency mạnh | Synchronous request/response và transactional boundary | Eventual consistency bất kể nghiệp vụ |
| Giao dịch liên hệ nhiều dịch vụ | Transaction boundaries, saga khi có lý do; compensation | Distributed transaction giả định luôn có |

## 3. Ma trận kiểm tra quyết định
Đánh giá cho mỗi lựa chọn: business fit; correctness/consistency; coupling; security; NFR; observability; testability; vận hành; chi phí; migration; năng lực team. Ghi ưu/nhược, bằng chứng và giả định; không chấm điểm định lượng khi chưa có số liệu.

## 4. Các câu hỏi bắt buộc
- Điều gì thực sự cần consistency ngay lập tức? Boundary ở đâu?
- Những lỗi gì có thể xảy ra? Có thể retry an toàn không?
- Khi thông điệp bị lặp, mất, đảo thứ tự hoặc đến muộn, trạng thái có còn đúng?
- Nếu bỏ một tầng/pattern thì giải pháp có đơn giản và vẫn đáp ứng yêu cầu không?
- Team có triển khai, debug, deploy, vận hành và rollback được không?

## 5. Đầu ra khuyến nghị
1. Context và constraints.
2. Tối thiểu hai phương án tương xứng (kể cả phương án đơn giản).
3. Decision + trade-offs + NFR liên quan.
4. Điểm cần thử nghiệm/đo đạc.
5. ADR và kế hoạch migration khi quyết định có tác động đáng kể.
