# Observability, SLI/SLO & Capacity

## Telemetry
Structured logs với correlation/request id; metrics (latency, traffic, errors, saturation); distributed tracing; RED và USE theo loại service.

## SLI/SLO
Định nghĩa user-facing SLI bằng cách đo được; chọn SLO theo impact và khả năng vận hành; error budget là công cụ cân bằng reliability và tốc độ thay đổi, không phải SLA mặc định.

## Alerting
Alert symptoms ảnh hưởng người dùng thay vì chỉ CPU; actionable alerts; xác định owner, runbook, severity và routing.

## Capacity
Baseline RPS/TPS, p95/p99, queue depth/lag, DB pool, memory/CPU, headroom, load shape; benchmark trước khi tối ưu.

## Verification
Truy tìm một giao dịch qua nhiều service; kiểm tra alert noisy/silent; kiểm thử degrade dependency và backlog recovery.

## Reference
Google SRE Workbook — Error Budget Policy: https://sre.google/workbook/error-budget-policy/
