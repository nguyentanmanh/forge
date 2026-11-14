# Secure SDLC & Software Supply Chain

## Từ requirements tới operations
Data classification -> security requirements -> threat model -> secure design -> SAST/SCA/secrets scanning -> test -> deploy controls -> monitor/incident response.

## Security requirements
OWASP ASVS v5.0, least privilege, secure defaults, authn vs authz, BOLA/tenant isolation, crypto/key rotation, input/output validation, audit/event integrity, data minimization.

## Supply chain
Dependency policy, SBOM, signed artifacts/provenance khi có hạ tầng, CI least privilege, immutable deploy artifacts, secret rotation.

## Khi audit
Ghi requirement, evidence, pass/fail/not assessed, owner, residual risk. Không đánh đồng 'đã review' với 'đạt compliance'.

## References
https://asvs.owasp.org/ ; https://contribute.cncf.io/projects/best-practices/security/supply-chain/supply-chain-best-practices/
