# Góc nhìn — Solution Architecture

## Khi sử dụng
Khi cần đưa ra quyết định giải pháp ở cấp hệ thống, xác định boundaries, phụ thuộc tích hợp và NFR.

## Trọng tâm đánh giá
- Business capability, current/target state, constraints và assumptions.
- System context, ownership, trust boundaries, interface contracts, C4/sequence khi hữu ích.
- NFR: availability, latency, throughput, scalability, consistency, recoverability, security, observability.
- Build vs buy, coupling, operational complexity, cost, vendor lock-in.
- Organizational fit, team capability, ecosystem/support lifecycle, license và total cost of ownership.
- Failure modes, migration, compatibility, deployment và rollback.
- Adoption path, observability, rollback và exit strategy cho công nghệ mới.
- ADR: lựa chọn, phương án bị loại, hậu quả và điều kiện xem xét lại.

## Các câu hỏi then chốt
1. Thiết kế này giải quyết business outcome nào?
2. Có phương án đơn giản hơn nhưng vẫn đáp ứng NFR không?
3. Hệ thống thất bại ở đâu, ai sở hữu lỗi và dữ liệu?
4. Bằng chứng nào chứng minh các giả định kiến trúc?
5. Đâu là technology constraint bắt buộc, đâu chỉ là preference?

## Skills phù hợp (chọn theo task)
`solution-architecture`, `architecture-review`, `system-analysis`, `integration-design`, `architecture-decision`, `security-review`, `performance-review`.

> Không áp đặt kiến trúc phân tán/microservices nếu bài toán không yêu cầu.
