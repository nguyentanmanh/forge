# SOLID và GRASP — dùng đúng mức, không thần thánh hóa

## Mục tiêu
Giảm coupling, giữ invariants rõ, thay đổi an toàn và test dễ. Đây là heuristics, không phải checklist buộc mỗi class phải có interface.

## SOLID: tiêu chí và cảnh báo
| Nguyên tắc | Tín hiệu nên áp dụng | Lạm dụng thường gặp | Kiểm chứng |
|---|---|---|---|
| SRP | Một module đổi vì nhiều nhóm lý do độc lập | Chẻ class thành hàng chục lớp pass-through | Một thay đổi nghiệp vụ chỉ tác động nhóm module liên quan |
| OCP | Nhiều provider/variant mới, contract ổn định | Plugin hóa một logic chưa chắc biến đổi | Thêm variant mà không sửa lõi ổn định |
| LSP | Các implementation phải giữ cùng tiền/hậu điều kiện | Subclass ném UnsupportedOperationException | Contract tests trên mọi implementation |
| ISP | Client chỉ cần một tập hành vi nhỏ | Interface chia quá vụn | Consumer mock nhỏ và độc lập |
| DIP | Domain/application bị khóa vào external IO | Tạo interface cho mọi DTO/utility | Unit test domain không cần DB/network |

## GRASP
Information Expert: đặt trách nhiệm nơi có dữ liệu/invariant; Creator: tạo đối tượng ở vị trí hợp lý; Controller: nhận use case ở application boundary; Low Coupling/High Cohesion: đơn vị thay đổi gọn; Protected Variations: cách ly điểm thay đổi thực sự.

## Quy tắc lựa chọn
1. Chỉ trừu tượng hóa khi có bằng chứng thay đổi hoặc ranh giới cần test/isolate.
2. Giữ domain model rõ; đừng giấu logic quan trọng trong generic framework.
3. Prefer composition over inheritance khi reuse hành vi biến động.
4. Review bằng change scenario: thêm provider, đổi rules, đổi persistence cần sửa bao nhiêu nơi?

## Ví dụ
Payment processor có 3 provider khác contract: Adapter ở integration boundary; Strategy nếu routing/behavior thay đổi. Không cần Factory + AbstractFactory + ServiceLocator cùng lúc.

## Khi không dùng
CRUD mỏng, logic ổn định, interface chỉ có một implementation không có nhu cầu decoupling rõ rệt.
