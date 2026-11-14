# Infrastructure Foundations — knowledge cho software engineer

## Core
DNS, TLS, HTTP/2/3, TCP, load balancer L4/L7, reverse proxy, routing, NAT, firewall, service discovery, network segmentation, egress policies.

## Compute / storage
VM vs container vs managed service, horizontal/vertical scaling, stateful vs stateless, persistent storage, object storage, cache, queue, failure domains.

## Design questions
- Request đi qua hop nào? Trust boundary ở đâu? TLS terminate tại đâu?
- Timeout mỗi hop là bao nhiêu; retry budget do ai chịu?
- Private/public network, DNS, certificate rotation và outbound access?
- Multi-AZ/region có thực sự cần không? RTO/RPO? Chi phí?

## Troubleshooting
DNS resolve -> TCP connectivity -> TLS handshake -> HTTP status -> application logs -> dependency trace. Không nhầm kubectl exec là 'SSH vào pod'.

## Không mặc định
Một developer không nhất thiết phải tự quản cluster/infra; trách nhiệm cần phân biệt DevOps/Platform/Infra và quyền truy cập được cấp.
