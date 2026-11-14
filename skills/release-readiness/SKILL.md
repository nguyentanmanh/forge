---
name: release-readiness
description: >
  Kiểm tra mức sẵn sàng triển khai production: quality gates, DB migrations, rollback, security, observability, CI/CD, runbook, approvals.
---

# Release Readiness

## Khi dùng
Kích hoạt khi yêu cầu phù hợp, hoặc user gọi `$release-readiness`. Không kích hoạt vì chỉ có tên skill trong repo.

## Workflow

1. Xác định release scope, affected services và backward-compatibility window.
2. Chạy checklist tests, contract/migration, image/dependency scan, configuration/secrets; đọc evidence có sẵn.
3. Kiểm tra rollout (canary/blue-green khi phù hợp), readiness, monitoring, feature flags, rollback.
4. Xác định release owner, change approval, on-call, incident bridge, reconciliation.
5. Ghi GO / NO-GO / CONDITIONAL với gaps; không tự deploy.

## Tài liệu tham khảo
`forge/knowledge/engineering/devops/ci-cd-and-gitops.md` — chỉ đọc khi có quyền và thật sự cần.

## Đầu ra
Bảng findings ưu tiên; observation/evidence; recommendation & trade-off; owner và tests; open questions.

## Quality gates
Không bịa production state/metrics; không thay đổi production, quyền hoặc dữ liệu khi chưa được phép; phân biệt mô phỏng với thực thi.
