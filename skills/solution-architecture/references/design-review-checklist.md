# Checklist đánh giá Solution Architecture

> Dùng để kiểm tra từng điểm có liên quan. **N/A** là hợp lệ nếu giải thích vì sao không áp dụng.

## 1. Business fit
- [ ] Business capability, success metrics, in-scope/out-of-scope rõ ràng.
- [ ] Các actors và critical journeys được mô tả.
- [ ] Có acceptance criteria đối chiếu được.

## 2. Ranh giới & ownership
- [ ] Biết system of record của từng dữ liệu.
- [ ] API/event producer, consumer và schema owner rõ ràng.
- [ ] Trust boundaries và external dependencies được xác định.

## 3. Functional correctness
- [ ] Happy path, rejection, retry, timeout và partial failure đều có cách xử lý.
- [ ] Idempotency key, deduplication scope, lifecycle và retention (nếu cần) rõ ràng.
- [ ] Error code mapping và correlation ID thống nhất.

## 4. Data
- [ ] Consistency, isolation và transaction boundary phù hợp.
- [ ] Schema evolution và migration/rollback có phương án.
- [ ] Data lineage, PII, audit và retention được xét.

## 5. Quality attributes
- [ ] NFR có scenario kiểm chứng được.
- [ ] Latency/throughput/capacity có số liệu hoặc được đánh dấu unknown.
- [ ] Failover, RTO/RPO, backup/restore theo mức độ quan trọng.
- [ ] Cost/complexity tương xứng với lợi ích.

## 6. Security
- [ ] AuthN/AuthZ, least privilege, secret rotation và encryption.
- [ ] Threat scenarios: spoofing, tampering, replay, privilege escalation.
- [ ] Audit log không lộ credentials/PII.

## 7. Operability
- [ ] Logs, metrics, traces, alert owner và on-call.
- [ ] Readiness/liveness, rollback, incident runbook, feature flag.
- [ ] Khả năng đo tác động và phát hiện regression.

## 8. Decision & proof
- [ ] Ít nhất một phương án thay thế được cân nhắc nếu có trade-off.
- [ ] Lý do chọn/loại phương án được ghi nhận.
- [ ] Có ADR cho quyết định khó đảo ngược.
- [ ] Có kế hoạch spike/POC/test để xác minh giả định rủi ro cao.
