# Code Quality — nguyên tắc chọn mức phức tạp

## Tiêu chí
Correctness, readability, cohesion, coupling, testability, changeability, runtime cost, operational clarity.

## Heuristics
- KISS: giải pháp đơn giản nhất đáp ứng yêu cầu và NFR, không phải ít dòng nhất.
- YAGNI: chưa thêm cấu trúc cho nhu cầu chưa chứng minh; không áp dụng mù quáng với security, audit, recovery.
- DRY: tránh trùng **tri thức/logic**; đôi khi duplication code nhỏ an toàn hơn abstraction sai.
- Explicit over clever: business invariants và authorization cần rõ.
- Boy Scout Rule: cải thiện vừa đủ trong scope, không refactor unrelated.

## Review
- Những gì thay đổi khi thêm use case/provider? Có regression tests?
- Naming nói đúng domain? Nullability/error model rõ?
- Có hidden I/O, shared mutable state, N+1 query, global state?
- Có đo đạc trước khi tối ưu?

## Anti-patterns
God service, anemic domain model trong nghiệp vụ phức tạp, over-abstraction, framework leakage, exception swallowing, premature caching, distributed monolith.
