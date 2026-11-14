---
name: integration-design
description: Thiết kế luồng tích hợp đồng bộ, bất đồng bộ, event hoặc file-based.
---

# Integration Design

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$integration-design`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định bên gửi/nhận, ownership, contract, SLA và trust boundaries.
2. Chọn sync/async/batch/file dựa trên latency và consistency.
3. Thiết kế message schema, correlation, retry, DLQ, deduplication, ordering, replay.
4. Kiểm tra network, timeout, partial failure, backpressure, reconciliation.
5. Lập observability và contract testing.

## Đầu ra mong đợi
Sequence, contract, failure/recovery matrix, operational runbook.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/design-patterns/distributed-patterns.md`
- `knowledge/engineering/reliability/resilience-and-dr.md`
Không tải toàn bộ Knowledge Base.
