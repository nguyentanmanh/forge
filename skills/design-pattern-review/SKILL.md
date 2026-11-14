---
name: design-pattern-review
description: >
  Đánh giá lựa chọn GoF, enterprise hoặc distributed design patterns dựa trên use case, tránh overengineering và xác minh trade-offs.
---

# Design Pattern Review

## Khi dùng
Kích hoạt khi yêu cầu phù hợp, hoặc user gọi `$design-pattern-review`. Không kích hoạt vì chỉ có tên skill trong repo.

## Workflow

1. Viết problem statement và change scenarios.
2. Đề xuất baseline đơn giản không pattern nếu khả thi.
3. Đối chiếu pattern-selection.md và chỉ đọc nhóm pattern liên quan.
4. Kiểm tra coupling, consistency, performance, failure modes và testability.
5. So sánh 2 options khi có quyết định quan trọng; đề xuất tối thiểu và migration path.
6. Ghi anti-patterns và test validation.

## Tài liệu tham khảo
`forge/knowledge/engineering/design-patterns/pattern-selection.md` — chỉ đọc khi có quyền và thật sự cần.

## Đầu ra
Bảng findings ưu tiên; observation/evidence; recommendation & trade-off; owner và tests; open questions.

## Quality gates
Không bịa production state/metrics; không thay đổi production, quyền hoặc dữ liệu khi chưa được phép; phân biệt mô phỏng với thực thi.
