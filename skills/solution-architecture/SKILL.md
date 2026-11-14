---
name: solution-architecture
description: Thiết kế phương án kiến trúc cho yêu cầu hoặc hệ thống mới. Dùng khi cần solution design, NFR và trade-off.
---

# Solution Architecture

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$solution-architecture`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
Đầu vào: mục tiêu, phạm vi, constraints, thành phần hiện hữu, NFR và dữ liệu được phép sử dụng.
1. Tóm tắt problem statement và giả định.
2. Xác định actors, trust boundaries, C4 context/container và luồng chính/phụ.
3. Phân tích NFR định lượng nếu có: availability, latency, throughput, RTO/RPO, security.
4. Đề xuất tối thiểu 2 lựa chọn tương xứng; trade-off xây dựng/vận hành/tính nhất quán.
5. Kiểm tra data ownership, consistency, idempotency, retries, timeouts, backpressure, observability.
6. Chọn phương án có lý do; ghi ADR, rủi ro tồn đọng và rollout/rollback.
7. Chỉ đưa số liệu định lượng khi có nguồn hoặc giả định ghi nhãn.

## Đầu ra mong đợi
Solution summary, sơ đồ, options matrix, NFR map, decision, rollout, validation plan.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/architecture/architecture-selection.md`
- `knowledge/engineering/architecture/architecture-selection-extended.md`
- `knowledge/engineering/design-patterns/pattern-selection.md`
- `knowledge/engineering/security/threat-model-and-abuse.md`
- `knowledge/engineering/reliability/resilience-and-dr.md`
Không tải toàn bộ Knowledge Base.
