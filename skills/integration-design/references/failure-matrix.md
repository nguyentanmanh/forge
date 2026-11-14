# Integration Failure Matrix

| Failure | Biểu hiện | Phương án xử lý | Kiểm chứng |
|---|---|---|---|
| Timeout trước response | Không rõ downstream đã xử lý chưa | Idempotency key, status lookup, reconciliation | Retry không tạo giao dịch đôi |
| Duplicate event | Cùng event được giao lại | Dedup/consumer idempotency | Exactly-once business effect (nếu đảm bảo) |
| Out-of-order | Event mới tới trước | Sequence/version/ordering guard | Replay mixed order |
| Poison message | Parse/validate fail liên tục | DLQ và điều tra | Có thể replay có kiểm soát |
| Partial commit | DB đã ghi nhưng publish lỗi | Outbox hoặc equivalent | Recovery không mất event |
