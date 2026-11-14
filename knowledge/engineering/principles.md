# Nguyên tắc kỹ thuật tái sử dụng

## Design for change
Tách interface khỏi implementation, ưu tiên testability và giảm coupling; tránh abstractions không có use case.

## Data consistency
Rõ transaction boundary; với distributed systems, không ngụy nhận local ACID là end-to-end exactly-once.

## APIs
Có explicit contract, error model, authentication/authorization và compatibility plan.

## Operational readiness
Mọi flow quan trọng cần khả năng truy vết, alert, runbook, recovery và rollback khi thích hợp.

## Security by design
Least privilege, secure defaults, dữ liệu nhạy cảm không xuất hiện trong code/log/docs không được phép.
