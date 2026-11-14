---
name: performance-review
description: Đánh giá bottleneck, capacity và khả năng đáp ứng NFR hiệu năng.
---

# Performance Review

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$performance-review`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Chốt SLO/SLI và traffic profile đã xác nhận.
2. Tách CPU/memory/IO/DB/latency/network/queue saturation.
3. Đề nghị đo benchmark, p95/p99, load distribution, query plans.
4. Đánh giá cache, batching, pool, backpressure, scaling trade-offs.
5. Không dự đoán throughput bằng con số vô căn cứ.

## Đầu ra mong đợi
Performance hypothesis, measurement plan, constraints, options.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.
