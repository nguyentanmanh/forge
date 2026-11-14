---
name: api-design
description: Thiết kế hoặc review REST API contract, idempotency, versioning và errors.
---

# Api Design

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$api-design`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định consumer và resource/use case.
2. Định nghĩa endpoints, authN/authZ, headers, schemas, response/error mapping.
3. Kiểm tra version compatibility, pagination, filtering, rate limits, validation.
4. Đánh giá idempotency/retry, signature, correlation IDs, audit và PII masking.
5. Tạo contract examples và contract tests.

## Đầu ra mong đợi
API contract outline, response examples, error catalog, compatibility risks.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
