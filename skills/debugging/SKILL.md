---
name: debugging
description: Điều tra bug hoặc sự cố kỹ thuật từ log, lỗi, hành vi thực tế.
---

# Debugging

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$debugging`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định triệu chứng, impact, thời điểm, phiên bản, môi trường.
2. Tạo 2–4 giả thuyết phân biệt; chọn phép kiểm tra read-only trước.
3. Thu thập logs, metrics, traces, code paths một cách có mục tiêu.
4. Loại trừ giả thuyết bằng bằng chứng.
5. Đề xuất workaround/root fix/verification; không chạy destructive command tùy tiện.

## Đầu ra mong đợi
Timeline, hypothesis table, evidence, RCA confidence, remediation.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
