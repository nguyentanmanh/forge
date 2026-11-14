# Clean Architecture

## 1. Mục đích
Giảm coupling giữa business policy và chi tiết hạ tầng. Dependencies trong source đi từ adapter/framework bên ngoài vào các policy cốt lõi; dependency inversion qua interfaces/ports khi có giá trị.

## 2. Khi hữu ích
- Business logic có tuổi thọ dài và cần unit test độc lập DB/HTTP/broker.
- Nhiều entry points/adapters (REST, batch, Kafka) sử dụng cùng use case.
- Framework hoặc hạ tầng có khả năng đổi hoặc việc thay đổi cần giảm tác động.

## 3. Khi không cần áp dụng cứng nhắc
- Service nhỏ, thao tác CRUD đơn giản, ít logic độc lập.
- Chi phí abstraction, mapping layers, boilerplate lớn hơn lợi ích.
- Không nên mặc định cứ có Clean Architecture là phải có 4 module build riêng.

## 4. Các lớp khái niệm
- Domain: entities, value objects, invariants không phụ thuộc framework.
- Application: use cases, orchestration, ports.
- Adapters: HTTP controllers, DB repositories implementation, Kafka consumers/producers.
- Infrastructure/bootstrap: cấu hình, framework wiring, runtime.

## 5. Kiểm tra dependency
- Domain có import Spring/JPA/Kafka/HTTP không? Nếu có, cần lý giải.
- Application có dùng trực tiếp HTTP request/response hoặc câu SQL không?
- Mapping DTO/entity thực sự cần ở boundary nào?
- Business rule có test được với fake/in-memory ports không?

## 6. Trade-offs
Ưu: testability, change isolation, rõ ranh giới. Nhược: thêm interface, mapping, complexity, chi phí onboarding. Chỉ tạo abstraction khi có boundary thực sự; không tạo một port cho mỗi phương thức mà thiếu lý do.

## 7. Ví dụ use case Payment
`PaymentController → CreatePaymentUseCase → PaymentRepositoryPort`; adapter JPA implements port. Transaction management đặt ở boundary phù hợp; consistency và idempotency không tự được giải quyết chỉ vì chia layer.
