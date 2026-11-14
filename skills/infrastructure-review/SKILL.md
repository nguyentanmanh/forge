---
name: infrastructure-review
description: >
  Rà soát topology, networking, Kubernetes, compute, storage, capacity, RBAC và deployment risks của hệ thống trước release hoặc khi cần đánh giá infra.
---

# Infrastructure Review

## Khi dùng
Kích hoạt khi yêu cầu phù hợp, hoặc user gọi `$infrastructure-review`. Không kích hoạt vì chỉ có tên skill trong repo.

## Workflow

1. Thu thập sơ đồ deployment, environment, RTO/RPO và danh sách dependencies.
2. Trace DNS/TLS/network path, ingress, egress, trust boundaries, runtime identity.
3. Review requests/limits, probes, replicas, topology, PDB, autoscale, stateful storage và secret lifecycle.
4. Review permissions, cluster policies, CI deployment identity, cost/capacity; so sánh constraints.
5. Lập risk register, verification commands READ-ONLY, rollback và owners; không tự sửa infra.

## Tài liệu tham khảo
`forge/knowledge/engineering/infrastructure/kubernetes-and-containers.md` — chỉ đọc khi có quyền và thật sự cần.

## Đầu ra
Bảng findings ưu tiên; observation/evidence; recommendation & trade-off; owner và tests; open questions.

## Quality gates
Không bịa production state/metrics; không thay đổi production, quyền hoặc dữ liệu khi chưa được phép; phân biệt mô phỏng với thực thi.
