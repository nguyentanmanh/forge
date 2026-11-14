---
name: troubleshooting
description: Chẩn đoán sự cố vận hành nhiều thành phần bằng evidence, hypothesis và các kiểm tra an toàn.
---

# Troubleshooting

## Khi dùng
Dùng khi triệu chứng có thể nằm ở nhiều thành phần như network, runtime, database, queue, dependency hoặc configuration. Nếu đã khoanh vùng lỗi trong code và cần tìm root cause ở code path, dùng `debugging`.

## Đầu vào và phạm vi
Xác định triệu chứng, impact, thời điểm, environment, thay đổi gần nhất, expected behavior và quyền truy cập. Ghi rõ dữ liệu nào đã quan sát, dữ liệu nào do người dùng cung cấp và điều gì chưa xác minh.

## Workflow
1. Lập timeline và khoanh blast radius: ai bị ảnh hưởng, thành phần nào và từ khi nào.
2. Trace request/data flow qua các dependency; xác định trust boundary và failure boundary.
3. Tạo 2–4 giả thuyết có thể bác bỏ, xếp theo khả năng, impact và chi phí kiểm tra.
4. Chọn phép kiểm tra read-only, an toàn và có sức phân biệt cao; ghi expected result trước khi chạy.
5. Đối chiếu logs, metrics, traces, configuration và thay đổi gần nhất; không thu thập tràn lan.
6. Kết luận với confidence; tách mitigation tạm thời, root fix, verification và rollback.
7. Nếu chưa đủ evidence, ghi `chưa xác minh` và nêu phép kiểm tra tiếp theo.

## Đầu ra mong đợi
Tóm tắt impact; timeline; bảng hypothesis/evidence/status; root cause và confidence; mitigation; root fix; verification; rollback; unknowns và owner.

## Quality gates
- Không bịa log, metrics, topology, production state hoặc quan hệ nhân quả.
- Correlation không tự động là causation; mỗi kết luận phải trỏ tới evidence.
- Không restart, flush cache, replay message, sửa dữ liệu hoặc thay đổi production khi chưa có yêu cầu và quyền phù hợp.
- Không ghi secret hoặc dữ liệu nhạy cảm vào báo cáo.

## Khi nào dừng
Dừng trước thao tác phá hủy, thay đổi production, truy cập vượt phạm vi hoặc khi bước tiếp theo cần approval/owner quyết định.
