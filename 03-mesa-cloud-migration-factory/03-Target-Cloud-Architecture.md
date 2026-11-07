# 03 — Target Cloud Architecture

## Architecture position

The target is a secure, multi-account, regionally resilient AWS-like cloud platform. It separates organizational governance, security, infrastructure, shared services, nonproduction, and production workloads while providing consistent identity, policy, observability, automation, recovery, and cost allocation.

## Architecture layers

| Layer | Capabilities | AWS-like examples |
|---|---|---|
| Organization | Account lifecycle, OUs, guardrails, billing | Organizations, Control Tower |
| Identity | Federation, SSO, workload identity, privileged access | IAM Identity Center, IAM, STS |
| Network/edge | DNS, private connectivity, routing, inspection, WAF, CDN | Route 53, Direct Connect/VPN, Transit Gateway, WAF, CloudFront |
| Compute | Virtual machines, containers, functions, managed runtimes | EC2, ECS/EKS, Lambda, Elastic Beanstalk/App Runner-like |
| Integration | APIs, events, queues, workflows, file transfer | API Gateway, EventBridge, SNS/SQS, Step Functions, Transfer Family |
| Data | Object, relational, NoSQL, cache, search, catalog | S3, RDS/Aurora, DynamoDB, ElastiCache, OpenSearch, Glue Catalog |
| Security | Keys, secrets, posture, threat detection, audit | KMS, Secrets Manager, Security Hub, GuardDuty, CloudTrail, Config |
| Operations | Metrics, logs, traces, incidents, automation, backup | CloudWatch, X-Ray/OpenTelemetry, Systems Manager, Backup |
| Delivery | Source, build, artifacts, deploy, policy gates | Code pipeline equivalents or third-party CI/CD |
| Financial | Budgets, allocation, forecasts, optimization | Cost Explorer, Budgets, CUR-like exports |

Mappings are illustrative; the architecture is based on capabilities and interfaces rather than product names.

## Quality attributes

- **Operational excellence:** automated provisioning, observable services, tested runbooks, post-incident learning.
- **Security:** explicit identity, resource-level policy, encryption, least privilege, protected audit, supply-chain assurance.
- **Reliability:** multi-zone design, backups, failover, graceful degradation, quota and dependency management.
- **Performance efficiency:** measured sizing, elastic patterns, managed services, load and latency testing.
- **Cost optimization:** ownership tags, budgets, unit costs, right-sizing, lifecycle policies, decommissioning.
- **Sustainability:** efficient service selection, scaling, retention, and workload scheduling.

## Environment strategy

- Development, test, staging, and production are separated by accounts for critical workloads.
- Shared platform capabilities have dedicated accounts and clearly defined service interfaces.
- Production data is not copied to lower environments unless explicitly approved and protected.
- Sandbox accounts are time-bounded, budget-controlled, and denied connectivity to protected resources by default.

## Resilience tiers

| Tier | Mission expectation | Notional target pattern |
|---|---|---|
| Tier 1 | Critical, minimal interruption | Multi-zone; regional recovery prepared and exercised |
| Tier 2 | Important, bounded interruption | Multi-zone; backup-based or warm regional recovery |
| Tier 3 | Standard business support | Single-region resilient service; tested restore |
| Tier 4 | Development/experimental | Rebuild from code; limited recovery investment |

See `diagrams/02-target-cloud-architecture.mmd` and `diagrams/03-multi-account-landing-zone.mmd`.
