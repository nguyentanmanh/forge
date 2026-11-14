---
name: architecture-decision
description: Ghi nhận hoặc cập nhật Architecture Decision Record cho một quyết định kỹ thuật.
---

# Architecture Decision

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$architecture-decision`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định bối cảnh, constraints và driver.
2. Liệt kê alternatives được xem xét.
3. Ghi decision, status, rationale và consequences.
4. Nêu trigger để revisit.
5. Không trình bày giả định như quyết định đã được phê duyệt.

## Đầu ra mong đợi
ADR versioned, dễ review, có alternatives và consequences.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
