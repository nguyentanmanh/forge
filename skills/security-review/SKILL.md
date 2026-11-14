---
name: security-review
description: Đánh giá bảo mật luồng ứng dụng, API hoặc kiến trúc trước khi triển khai.
---

# Security Review

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$security-review`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định tài sản, actors, trust boundaries và attack surfaces.
2. Kiểm tra authentication, authorization object-level, secrets, TLS, validation, injection.
3. Kiểm tra PII, logs, audit, data retention, least privilege.
4. Phân loại rủi ro và đề xuất mitigations/test.
5. Không khẳng định tuân thủ chính sách khi chưa có evidence.

## Đầu ra mong đợi
Threats, risk severity, mitigations, validation evidence.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/security/threat-model-and-abuse.md`
- `knowledge/engineering/security/secure-sdlc.md`
Không tải toàn bộ Knowledge Base.
