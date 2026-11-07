# AWS-Like Service Capability Map

This map is illustrative and intentionally avoids prescribing a specific provider implementation.

| Capability | Provider-neutral component | AWS-like example |
|---|---|---|
| Organization/account governance | Cloud organization and landing zone | Organizations and Control Tower |
| Workforce access | Federated single sign-on | IAM Identity Center |
| Workload identity | Role and short-lived token service | IAM roles and STS |
| Private connectivity | Dedicated/private and encrypted network links | Direct Connect and Site-to-Site VPN |
| Network hub | Central transit routing | Transit Gateway |
| Edge protection | CDN, WAF, load balancer, DDoS protection | CloudFront, WAF, ALB, Shield-like |
| Virtual compute | Elastic virtual machines | EC2 |
| Containers | Managed container orchestration | ECS/EKS/Fargate-like |
| Serverless | Event-driven functions | Lambda |
| API management | Governed API edge | API Gateway |
| Events and messaging | Event bus, topics, queues | EventBridge, SNS, SQS |
| Workflow | Managed state orchestration | Step Functions |
| Object storage | Durable object service | S3 |
| Relational database | Managed relational service | RDS/Aurora |
| NoSQL | Managed key/document database | DynamoDB |
| Catalog/lineage | Data catalog and metadata | Glue Data Catalog-like |
| Keys and secrets | Managed cryptography and secret lifecycle | KMS and Secrets Manager |
| Audit and configuration | API audit and configuration history | CloudTrail and Config |
| Detection/posture | Threat detection and findings aggregation | GuardDuty and Security Hub |
| Observability | Metrics, logs, traces, alarms | CloudWatch and OpenTelemetry/X-Ray |
| Backup | Policy-based backup and restore | AWS Backup-like |
| Cost governance | Budgets, allocation, reports | Budgets, Cost Explorer, CUR-like |
