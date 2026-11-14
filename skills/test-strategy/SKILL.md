---
name: test-strategy
description: Thiết kế chiến lược kiểm thử cho tính năng, API hoặc thay đổi hệ thống.
---

# Test Strategy

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$test-strategy`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định expected behavior, invariants, failure modes.
2. Phân tầng unit, integration, contract, e2e, performance/security nếu phù hợp.
3. Bao phủ positive, negative, boundary, concurrency, retry, timeout, duplicate.
4. Định nghĩa test data, môi trường, mocks, expected evidence.
5. Xếp ưu tiên theo rủi ro.

## Đầu ra mong đợi
Test matrix, critical cases, entry/exit criteria, test gaps.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/testing/testing-pyramid-and-contracts.md`
- `knowledge/engineering/security/threat-model-and-abuse.md`
Không tải toàn bộ Knowledge Base.
