# CI/CD, GitOps & Supply Chain

## Pipeline
Commit -> lint/static analysis -> unit/integration/contract tests -> security/dependency scan -> build reproducible artifact -> deploy -> verify -> promote/rollback.

## Release discipline
Branching policy theo team, PR review, protected branches, merge strategy, semantic/compatibility versioning, feature flags, approvals, artifact promotion.

## Infrastructure as Code
Terraform plan/review/state security; drift detection; GitOps desired state vs actual state; secret management và environment separation.

## Supply chain
Pin dependencies/images, SBOM, provenance/signing khi chính sách hỗ trợ, hạn chế pipeline tokens, bảo vệ release workflow. Không tuyên bố compliance nếu chưa có evidence.

## Anti-patterns
Build lại artifact cho production thay vì promote; secret trong CI logs; deployment script không idempotent; database migration không xét rollback; phát hành vào production không có release gate.

## Verification
Pipeline logs, test report, scan findings triaged, deployment health, audit trail, rollback readiness.
