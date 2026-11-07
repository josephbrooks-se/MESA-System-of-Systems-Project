# ADR-001 — Multi-Account Landing Zone

- **Status:** Accepted for the reference architecture
- **Decision:** Separate organization management, security, infrastructure, shared services, nonproduction, production, sandbox, and suspended workloads through governed organizational units and accounts.
- **Drivers:** Isolation, ownership, policy scope, billing, reduced blast radius, lifecycle management.
- **Alternatives:** One enterprise account; account per team only; separate organizations per workload.
- **Consequences:** Stronger boundaries and accountability; greater account, identity, network, and automation complexity.
- **Controls:** Automated account vending, baseline guardrails, centralized logs, federated identity, cost allocation, closure workflow.
- **Revisit when:** organizational/legal separation, scale, provider constraints, or authorization strategy changes materially.
