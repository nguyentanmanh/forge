# GoF & OO Patterns — Use cases

## Creational
Factory Method: provider/type chọn lúc runtime; Abstract Factory: tạo **nhóm** object phải tương thích; Builder: cấu hình nhiều tham số có invariant; Prototype: clone object phức tạp với semantics rõ; Singleton: cân nhắc kỹ vì global state/test coupling.

## Structural
Adapter: mapping interface bên ngoài; Facade: API đơn giản phía trước subsystem; Decorator: mở rộng hành vi mà không sửa class; Composite: cấu trúc cây; Proxy: lazy/remote/access control rõ; Bridge: hai chiều biến đổi độc lập; Flyweight: tối ưu shared immutable data khi đã đo memory.

## Behavioral
Strategy: thay policy; State: transition với guards; Command: biểu diễn request và undo/log (không mặc nhiên rollback); Chain of Responsibility: pipeline; Template Method: skeletal algorithm nhưng inheritance coupling; Observer: notification in-process; Mediator: phối hợp components; Specification: predicate/business criteria composable; Visitor: operation khác nhau trên cấu trúc loại ổn định.

## Ví dụ code review
Một enum + switch 3 case cố định có thể đơn giản hơn tạo hệ phân cấp strategy. Chọn State khi transition logic phức tạp và phải enforce guards; không chọn chỉ vì có cột status.

## Verification
Contract tests, mutation/branch coverage có trọng tâm; test invalid transitions và behavior parity trước/sau refactor.
