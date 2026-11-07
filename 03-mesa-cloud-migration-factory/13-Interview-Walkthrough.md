# 13 — Interview Walkthrough

## 90-second opening

“I created the MESA Cloud Migration Factory as a public-safe example of how I would architect a portfolio-scale transformation into an AWS-like cloud. The key challenge is not moving servers. It is preserving mission outcomes while changing identity, network, data authority, interfaces, operations, recovery, cost, and organizational responsibility.

I used MESA to start with the mission outcome and operational threads, then discover every workload and dependency, select an accountable 7R disposition, establish a secure multi-account landing zone, and sequence migrations by dependency and risk. Each wave passes architecture, security, data, operational, cutover, and recovery gates.

The architecture uses federated identity, resource-level zero trust, governed hybrid networking, infrastructure as code, centralized security and observability, workload-level ownership, and explicit FinOps. The result is a traceable decision system that moves eligible workloads, proves mission behavior, supports rollback, and actually closes the legacy environment.”

## Five-minute path

1. **Mission:** explain why every system needs a disposition but not every system should be rehosted.
2. **Landing zone:** show multi-account isolation, identity, network, security, shared services, and workload ownership.
3. **One workload:** trace discovery → 7R decision → dependencies → target pattern → wave → rehearsal → cutover → stabilization → decommission.
4. **Tradeoff:** defend migration-first/modernize-by-value, including when refactoring before migration is justified.
5. **Leadership:** close with decision gates, evidence, rollback authority, operating model, cost accountability, and mentoring/reuse.

## Likely questions

**Why not move all systems at once?** Dependencies, team capacity, platform readiness, data authority, and mission risk require sequenced waves. The program still dispositions the entire portfolio.

**Why multi-account?** It creates clear isolation, ownership, policy, billing, and blast-radius boundaries while allowing governed shared services.

**How do you prevent cloud sprawl?** Account vending, approved products, IaC, policy guardrails, budgets, tagging, drift detection, and expiration.

**When would you refactor before migrating?** When rehosting is infeasible, the legacy condition is unsafe/unsupported, or a mission deadline/value case justifies the added complexity.

**How do you know cutover succeeded?** Mission-thread, data, security, performance, resilience, operations, and cost evidence meet thresholds, and the authority accepts remaining limitations.

**What is the architect’s hardest decision?** Balancing migration tempo against dependency uncertainty, mission continuity, technical debt, evidence quality, and the organization’s ability to operate the target state.
