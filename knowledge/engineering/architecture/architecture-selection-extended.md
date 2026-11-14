# Architecture Choices — phân tích theo vòng đời

## Chọn gì trước?
Bắt đầu với requirements + constraints + NFR. Monolith modular là baseline hợp lệ; chỉ chọn microservices nếu độc lập triển khai/scale/ownership đủ lớn để bù distributed complexity.

## Lựa chọn
Layered/Hexagonal/Clean; domain boundaries & DDD; sync request-response vs async/event-driven; messaging vs DB; stateful vs stateless; CQRS/event sourcing chỉ khi benefit đo được.

## Quality gates
Correctness, security/abuse, latency/cost, consistency, operability, migration, disaster recovery, team ownership, delivery and rollback.

## Trade-off template
Option | Motivation | Benefits | Costs | Risk | Fit with constraints | Evidence | Exit criteria.

## Tránh
Architecture astronautics; chọn công nghệ theo trend; tạo distributed transaction không có reconciliation; tối ưu hiệu năng bằng suy đoán.
