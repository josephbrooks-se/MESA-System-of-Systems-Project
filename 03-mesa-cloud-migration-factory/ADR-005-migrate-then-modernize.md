# ADR-005 — Migrate First, Modernize by Value

- **Status:** Accepted with exceptions
- **Decision:** For large-scale waves, prefer rehost/relocate/replatform when feasible, then modernize according to mission value, risk, cost, and technical debt.
- **Drivers:** Portfolio scale, schedule, testing capacity, dependency risk, change saturation.
- **Alternatives:** Refactor every system before migration; rehost permanently; replace all applications.
- **Consequences:** Faster hosting exit and clearer modernization backlog; temporary technical debt and duplicated transition cost may remain.
- **Exceptions:** Refactor or replace before migration when current technology is unsafe/unsupported, rehosting is infeasible, or the mission value justifies complexity.
- **Revisit when:** pilot evidence, provider cost, licensing, performance, or legacy-exit deadline changes.
