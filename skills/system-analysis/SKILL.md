---
name: system-analysis
description: Phân tích và truy vết hệ thống hiện tại. Dùng khi cần reverse engineering luồng xử lý và dependency.
---

# System Analysis

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$system-analysis`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác nhận entrypoint và use case.
2. Tìm routes, caller/callee, services, storage, message/queue, batch jobs.
3. Theo dõi input→validation→processing→output, error paths, state changes.
4. Đối chiếu docs với implementation; đánh dấu unknowns.
5. Lập impact map và điểm cần test.

## Đầu ra mong đợi
System map, data flow, dependencies, known/unknown, impact analysis.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
