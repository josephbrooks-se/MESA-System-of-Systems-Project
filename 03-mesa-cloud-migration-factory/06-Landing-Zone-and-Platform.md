# 06 — Landing Zone and Platform Services

## Landing-zone responsibilities

- Organization and account lifecycle
- Organizational units and policy guardrails
- Federated identity and privileged-access patterns
- Network segmentation, routing, DNS, ingress, egress, and inspection
- Central security services, audit, and protected log archive
- Approved regions, services, images, configurations, and encryption
- Standard observability, backup, recovery, patching, and incident hooks
- Infrastructure-as-code modules and self-service products
- Cost allocation, budgets, quotas, and lifecycle controls

## Organizational units

| OU | Purpose | Example accounts |
|---|---|---|
| Security | Independent security and evidence services | Audit, security tooling, log archive |
| Infrastructure | Enterprise connectivity and edge | Network hub, DNS, ingress/egress |
| Shared Services | Reusable enterprise/platform services | Identity bridge, CI/CD, observability, backup |
| Nonproduction | Development, integration, test, staging | Product-specific accounts |
| Production | Production workloads with stricter guardrails | Product/domain accounts |
| Sandbox | Controlled experimentation | Time-bounded individual/team accounts |
| Suspended | Quarantine and closure | Disabled or investigation accounts |

## Account principles

- Accounts are isolation, policy, ownership, and cost boundaries—not user identities.
- The organization management account contains no workloads and has tightly restricted access.
- Security/audit roles are separate from workload administration.
- Production and nonproduction are separated for critical workloads.
- Network reachability is explicitly approved; account membership does not grant connectivity.
- Standard account vending applies guardrails, logging, identity, budgets, and baseline monitoring automatically.

## Platform products

- Governed account and environment provisioning
- Standard network attachment and private DNS
- Approved compute, container, serverless, database, object, and messaging patterns
- CI/CD pipeline and artifact provenance
- Secrets, keys, certificates, and workload identity
- Observability and incident-management integration
- Backup, restore, and recovery orchestration
- Data catalog, classification, and lifecycle policy

## Platform SLOs

Platform services publish availability, response, support, recovery, maintenance, and dependency commitments. Consumers document the effect of a platform-service failure instead of assuming the service is always available.

See `diagrams/03-multi-account-landing-zone.mmd`.
