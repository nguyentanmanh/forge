---
name: technical-writing
description: Soạn hoặc chỉnh sửa Developer Guide, HLD, ADR, runbook và tài liệu kỹ thuật.
---

# Technical Writing

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$technical-writing`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định độc giả, quyết định họ cần đưa ra và scope.
2. Đọc writing-style và nguồn thực tế cần thiết.
3. Chọn template thích hợp, không tự gò tất cả tài liệu chung một mẫu.
4. Mô tả overview→architecture→implementation→verification→troubleshooting khi phù hợp.
5. Rà terminology, code, command, link, tính xác minh; ghi unresolved points.
6. Giữ cấu trúc bản cũ khi nhiệm vụ chỉ là sửa.

## Đầu ra mong đợi
Tài liệu hoàn chỉnh có headings, ví dụ, verification và open questions.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
