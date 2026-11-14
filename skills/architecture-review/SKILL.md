---
name: architecture-review
description: Thẩm định thiết kế kiến trúc có sẵn. Dùng khi review HLD/LLD, architecture diagrams hoặc technical proposals.
---

# Architecture Review

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$architecture-review`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định thiết kế được review và phạm vi.
2. Kiểm tra evidence: diagrams, APIs, code, deployment, NFR.
3. Review boundaries, coupling, resiliency, data flow, authN/authZ, secrets, audit, observability.
4. Nêu findings có severity P0–P3, tác động, bằng chứng và phương án xử lý.
5. Tách blocking issue với improvement.
6. Ghi rõ các phần không thể kết luận.

## Đầu ra mong đợi
Findings ưu tiên theo severity, câu hỏi làm rõ, recommendation và điều kiện accept.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/design-patterns/pattern-selection.md`
- `knowledge/engineering/reliability/resilience-and-dr.md`
- `knowledge/engineering/security/threat-model-and-abuse.md`
Không tải toàn bộ Knowledge Base.
