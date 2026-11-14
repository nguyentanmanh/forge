---
name: incident-analysis
description: Phân tích sự cố, viết postmortem và hành động phòng ngừa.
---

# Incident Analysis

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$incident-analysis`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Ghi timeline và customer impact có bằng chứng.
2. Tách trigger, contributing factors và systemic causes.
3. Không đổ lỗi cá nhân, không giả định RCA.
4. Đề xuất corrective/preventive actions có owner, priority, verification.

## Đầu ra mong đợi
Incident report, causes/confidence, actions, follow-up.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
