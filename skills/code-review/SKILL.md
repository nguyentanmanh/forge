---
name: code-review
description: Review patch, pull request hoặc thay đổi mã nguồn để tìm bug, regression và security issues.
---

# Code Review

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$code-review`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Đọc diff và contract liên quan, không review lan man ngoài scope.
2. Ưu tiên correctness, data loss, race condition, null handling, authorization, error handling.
3. Tái dựng đường đi lỗi và điều kiện kích hoạt.
4. Mỗi finding ghi path/line hoặc location, severity, ảnh hưởng và sửa đề xuất.
5. Không tạo finding không có bằng chứng.
6. Nêu testing gaps và rủi ro còn lại.

## Đầu ra mong đợi
Findings theo mức ưu tiên; tóm tắt ngắn; test thiếu.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/fundamentals/solid-and-grasp.md`
- `knowledge/engineering/fundamentals/code-quality.md`
- `knowledge/engineering/data/transactions-and-concurrency.md`
Không tải toàn bộ Knowledge Base.
