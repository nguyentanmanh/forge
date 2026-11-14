---
name: requirements-analysis
description: Phân tích yêu cầu kinh doanh, use cases và acceptance criteria.
---

# Requirements Analysis

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$requirements-analysis`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định stakeholders, business objective và boundaries.
2. Ghi AS-IS/TO-BE, scenarios, edge cases, exceptions.
3. Truy vết business rule → requirement → acceptance test.
4. Liệt kê decision pending, ambiguity, assumptions.

## Đầu ra mong đợi
Requirements matrix, questions, use-case flow, testable acceptance criteria.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
