# Threat Modeling & Business Logic Abuse

## Threat model
Actors, assets, entry points, trust boundaries, attacker capabilities, misuse/abuse cases, security invariants, controls và residual risk. Dùng STRIDE như checklist, không thay thế hiểu nghiệp vụ.

## Abuse cases
Bypass approval; self-approval (maker-checker); change amount after approval; horizontal privilege escalation/BOLA; IDOR; split transaction to evade limits; replay/duplicate submit; race condition; stale consent; cross-tenant access; parameter tampering; automated enumeration.

## Required controls
Server-side authorization/object ownership; atomic state machine; immutable approval binding; idempotency; rate/velocity rules nếu nghiệp vụ đòi hỏi; audit trail; anomaly monitoring; fraud review/human approval khi phù hợp.

## Validation
Negative tests, role/ownership matrix, concurrent requests, timeout/replay, stale tokens, tampered payload; kiểm thử chỉ trong môi trường được phép.

## Source
OWASP ASVS v5.0 V2: https://github.com/OWASP/ASVS/blob/master/5.0/en/0x11-V2-Validation-and-Business-Logic.md
