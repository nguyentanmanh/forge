---
name: delivery-planning
description: Lập kế hoạch triển khai kỹ thuật qua milestones, dependencies và rollout.
---

# Delivery Planning

## Khi dùng
Chỉ dùng khi yêu cầu phù hợp với mô tả phía trên hoặc người dùng gọi rõ `$delivery-planning`.

## Đầu vào và phạm vi
Xác định mục tiêu, ngữ cảnh thực tế, ràng buộc, nguồn evidence và quyền truy cập. Nếu thiếu một thông tin ảnh hưởng quyết định, ghi giả định hoặc hỏi có trọng tâm.

## Workflow
1. Chia scope thành deliverables có acceptance criteria.
2. Xác định critical dependencies, owners, milestones, risk.
3. Thiết kế cutover, feature flag, rollback, communication plan.
4. Không cam kết timeline khi chưa có capacity và constraint.

## Đầu ra mong đợi
Phased delivery plan, risks, release checklist, blockers.

## Quality gates
Tuân thủ evidence, scope, safety và context budget của FORGE. Không bịa trạng thái hệ thống hoặc thực hiện thay đổi nhạy cảm khi chưa được phép.

## Khi nào dừng
Dừng trước thay đổi production, quyền truy cập vượt phạm vi, thao tác phá hủy hoặc yêu cầu dữ liệu mật không được phép.

## Knowledge routing bổ sung
Chỉ đọc tài liệu liên quan, từ `forge/`:
- `knowledge/engineering/devops/ci-cd-and-gitops.md`
Không tải toàn bộ Knowledge Base.
