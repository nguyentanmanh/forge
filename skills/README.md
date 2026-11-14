# Skills Catalog

Skills là workflow theo nhiệm vụ, không phải đơn vị phân loại kiến thức. Codex đọc `name` và `description` trước; chỉ tải toàn bộ skill khi cần.

| Nhóm | Skills |
|---|---|
| Architecture | solution-architecture, architecture-review, architecture-decision |
| Delivery | delivery-planning, incident-analysis, release-readiness |
| Engineering | system-analysis, code-review, test-strategy, debugging, troubleshooting, api-design, integration-design, database-design, performance-review, design-pattern-review |
| Security & Reliability | security-review, business-logic-abuse-review, reliability-review, infrastructure-review |
| Documentation | technical-writing, stakeholder-report |
| Business | requirements-analysis, research-brief |
| Career | career-review |

Tổng cộng: 25 skills. Chỉ bật những skills thường dùng; mục tiêu là chọn đúng skill, không phải số lượng.

## Chọn skill chính

| Tình huống | Skill chính | Không dùng thay cho |
|---|---|---|
| Thiết kế hệ thống/flow mới | `solution-architecture` | Review một thiết kế đã có |
| Review kiến trúc hiện hữu | `architecture-review` | Viết ADR hoặc thiết kế từ đầu |
| Ghi nhận quyết định và trade-off | `architecture-decision` | Phân tích toàn hệ thống |
| Phân tích boundary, actor, data flow | `system-analysis` | Thiết kế implementation chi tiết |
| Review diff/code | `code-review` | Review kiến trúc tổng thể |
| Lỗi đã khoanh vùng trong code | `debugging` | Sự cố xuyên nhiều thành phần |
| Sự cố runtime/dependency chưa khoanh vùng | `troubleshooting` | Post-incident review |
| Phân tích sự cố đã xảy ra | `incident-analysis` | Debug lỗi đang diễn ra |
| Thiết kế HTTP/event contract | `api-design` | Failure flow xuyên hệ thống |
| Thiết kế tích hợp và failure handling | `integration-design` | Thiết kế schema nội bộ |
| Schema, transaction, migration | `database-design` | API contract |
| Threat, authorization, control | `security-review` | Lạm dụng workflow nghiệp vụ |
| Bypass, replay, race, limit abuse | `business-logic-abuse-review` | Security review tổng quát |
| SLO, retry, resilience, DR | `reliability-review` | Topology/RBAC/capacity |
| Topology, Kubernetes, RBAC, capacity | `infrastructure-review` | Release gate |
| Kiểm tra trước production | `release-readiness` | Delivery plan dài hạn |

Mặc định dùng một skill chính. Chỉ thêm skill thứ hai khi task có hai workflow độc lập và nêu rõ lý do.
