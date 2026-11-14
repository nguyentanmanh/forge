---
name: database-design
description: Thiết kế schema, migration, indexing hoặc transaction boundaries.
---

# Database Design

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$database-design`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Xác định domain invariants và data ownership.
2. Thiết kế entities, constraints, relationships và access patterns.
3. Xem indexing, query plans, isolation, locking, optimistic concurrency.
4. Đánh giá migration backward compatibility, backfill, rollback.
5. Xây test cho tính toàn vẹn và hiệu năng.

## Đầu ra mong đợi
ERD, schema decisions, indexes, migration/rollback, test plan.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/data/database-engineering.md`
Không tải toàn bộ Knowledge Base.
