# Tiêu chuẩn viết và trình bày tài liệu

## Mục đích trước nội dung
Mỗi tài liệu phải trả lời: viết cho ai, để quyết định/thực hiện điều gì, phạm vi đến đâu, điều gì chưa xác minh.

## Ngôn ngữ
Dùng tiếng Việt; giữ tên class, method, API, header, field, command bằng tiếng Anh chính xác. Không dịch sai tên kỹ thuật.

## Cấu trúc
Tài liệu kỹ thuật thường gồm: Summary → Context → Architecture/Flow → Contract/Data → Implementation → Verification → Troubleshooting → Risks/Open Questions. Điều chỉnh theo mục đích, không máy móc.

## Độ chính xác
- Phân biệt hướng dẫn khuyến nghị, thực hành local và bước đã kiểm chứng ở môi trường thật.
- Mỗi command ghi rõ môi trường, điều kiện chạy và tác động nếu có.
- Không tạo output log hoặc số liệu giả như thật.

## Sơ đồ và bảng
Dùng Mermaid hoặc C4 khi giúp hiểu hệ thống; mỗi sơ đồ phải có nhãn, hướng dòng và giả định cần thiết. Bảng chỉ dùng khi có cột so sánh hữu ích.

## Review chỉnh sửa
Khi sửa tài liệu có sẵn: giữ cấu trúc phù hợp, không rewrite những phần ngoài scope; có thể giải thích thay đổi lớn trong changelog.

## Ví dụ chuẩn
Chưa có tài liệu đã duyệt trong `examples/approved/`; không tự chọn một tài liệu làm chuẩn khi chưa được review.

## Quy tắc có thể kiểm tra
- Summary phải cho biết kết luận hoặc quyết định, không chỉ giới thiệu chủ đề.
- Mọi số liệu, trạng thái môi trường và tuyên bố production phải có nguồn hoặc được đánh dấu `chưa xác minh`.
- Command có khả năng thay đổi state phải nêu impact, precondition và rollback nếu có.
- Link nội bộ phải trỏ tới file tồn tại; không để placeholder link trong tài liệu phát hành.
