# 13 — Interview Walkthrough

## 90-second opening

“I created MESA-CAP as a public-safe example of how I would lead cybersecurity architecture for a complex mission-system portfolio. The problem is not simply collecting vulnerabilities. It is connecting mission impact, system boundaries, threats, requirements, controls, evidence, and accountable decisions across embedded platforms, test environments, enterprise services, cloud capabilities, and suppliers.

I used my MESA method to start with the mission outcome and operational thread, then derive functions, logical services, interfaces, zero-trust policies, RMF artifacts, verification, and governance. The design is hybrid because isolated mission environments cannot be treated like ordinary enterprise endpoints. Segregated collectors use controlled store-and-forward, while central services provide consistent risk and evidence governance. Source systems remain authoritative.

The key architect contribution is decision quality: the platform makes inherited dependencies, evidence limitations, residual risk, and mission-cost-schedule tradeoffs explicit. Automation accelerates validation and routing, but a human authority retains risk and authorization accountability.”

## Five-minute discussion path

### 1. Frame the mission

Use `01-Mission-CONOPS.md`. Explain the mission outcome, excluded functions, and why assurance cannot sit in the embedded execution path.

### 2. Explain boundaries

Use `01-system-context.mmd` and `03-security-zones.mmd`. Identify enterprise/cloud, integration, evidence, management, and isolated enclave boundaries. State that network location never grants implicit trust.

### 3. Walk one risk thread

Use CYR-010 and the traceability example:

`provider control degrades → dependent boundaries identified → owners notified → mission impact reassessed → evidence requested → decision recorded → monitoring continues`

### 4. Defend the trade

Use the trade study. A centralized-only design improves consistency but fits isolated environments poorly. A federated-only model preserves autonomy but fragments evidence and dependency awareness. The hybrid design accepts integration complexity for better mission fit.

### 5. Show authorization rigor

Use the inheritance matrix, evidence rubric, SCTM, cyber test plan, and continuous-monitoring strategy. Emphasize that evidence quality and residual uncertainty are shown separately from implementation status.

### 6. Close as a lead architect

Explain governance: architecture decision records, clear decision rights, independent assessment, reusable patterns, mentoring, and trigger-based reassessment. The product is not a diagram; it is a governed decision system sustained through the lifecycle.

## Likely questions

**Why not put all evidence in one database?**  Because source authority, markings, data minimization, volume, and disconnected environments differ. Catalog provenance centrally; copy only when justified.

**What happens when the policy service fails?**  Protected writes fail closed. Approved read-only access may use a short-lived validated cache. The failure produces an alert and does not affect embedded mission execution.

**How do you keep the model current?**  Versioned contracts, source ownership, event-driven change, reconciliation, freshness rules, architecture gates, and monitoring triggers.

**How do you handle disagreement?**  Make assumptions, evidence, mission impact, alternatives, and decision authority explicit. Record the resolution in an ADR or risk decision with revisit triggers.

**What would you build first?**  Boundary, asset, dependency, identity, and evidence models—then prove one high-value mission risk thread end to end before scaling integrations.

## Portfolio safety note

Discuss the architecture patterns and your reasoning. Do not imply that this is a real customer system or use an interview to add operational details from current or former work.
