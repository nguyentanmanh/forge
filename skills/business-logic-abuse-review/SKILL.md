---
name: business-logic-abuse-review
description: >
  Đánh giá các abuse cases, workflow bypass, maker-checker, duplicate requests, race conditions và lạm dụng business rules khi thiết kế hoặc kiểm thử tính năng.
---

# Business Logic Abuse Review

## Khi dùng
Kích hoạt khi yêu cầu phù hợp, hoặc user gọi `$business-logic-abuse-review`. Không kích hoạt vì chỉ có tên skill trong repo.

## Workflow

1. Vẽ actor, resource, trust boundary và trạng thái nghiệp vụ; ghi invariants.
2. Dựng Happy/Failure/Abuse paths; kiểm tra bypass step, privilege, replay, concurrent submit, tampering, limit abuse.
3. Đánh giá likelihood, impact, control, residual risk; không đánh đồng policy với enforcement.
4. Đề xuất server-side authorization, state machine guards, atomicity, idempotency, audit/monitoring.
5. Viết abuse-case matrix (preconditions, action, expected denial, evidence) và negative tests.
6. Không chạy exploit hoặc thử trên hệ thống thật khi chưa được phép.

## Tài liệu tham khảo
`forge/knowledge/engineering/security/threat-model-and-abuse.md` — chỉ đọc khi có quyền và thật sự cần.

## Đầu ra
Bảng findings ưu tiên; observation/evidence; recommendation & trade-off; owner và tests; open questions.

## Quality gates
Không bịa production state/metrics; không thay đổi production, quyền hoặc dữ liệu khi chưa được phép; phân biệt mô phỏng với thực thi.
