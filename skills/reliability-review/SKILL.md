---
name: reliability-review
description: >
  Thiết kế hoặc review SLI/SLO, observability, resilience, retry/timeout, incident readiness và disaster recovery cho service production.
---

# Reliability Review

## Khi dùng
Kích hoạt khi yêu cầu phù hợp, hoặc user gọi `$reliability-review`. Không kích hoạt vì chỉ có tên skill trong repo.

## Workflow

1. Xác định user journey quan trọng và failure budget; phân biệt SLO với SLA.
2. Định nghĩa measurable SLI, alert threshold, owner và runbook.
3. Phân tích failure matrix: timeout after commit, broker outage, queue lag, DB failover, bad deploy.
4. Kiểm tra retry budget, idempotency, circuit breaker, backpressure và reconciliation.
5. Xác định RTO/RPO, backup/restore evidence, game-day và rollback.
6. Báo cáo known/assumed/unverified thay vì mặc định 'HA'.

## Tài liệu tham khảo
`forge/knowledge/engineering/reliability/resilience-and-dr.md` — chỉ đọc khi có quyền và thật sự cần.

## Đầu ra
Bảng findings ưu tiên; observation/evidence; recommendation & trade-off; owner và tests; open questions.

## Quality gates
Không bịa production state/metrics; không thay đổi production, quyền hoặc dữ liệu khi chưa được phép; phân biệt mô phỏng với thực thi.
