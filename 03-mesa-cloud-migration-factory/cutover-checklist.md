# Cutover Checklist

## Decision and coordination

- [ ] Cutover authority, technical lead, operations lead, security lead, data lead, and communications lead confirmed
- [ ] Change window, decision times, contact bridge, escalation, and stop conditions confirmed
- [ ] Mission/business users and external partners notified
- [ ] Risks, exceptions, evidence limitations, and residual decisions current

## Target readiness

- [ ] Approved infrastructure and policy baseline deployed through automation
- [ ] Identity, access, keys, secrets, certificates, DNS, network, and quotas validated
- [ ] Security logs, metrics, traces, alerts, dashboards, and incident routing verified
- [ ] Backup, restore, failover, and recovery prerequisites verified
- [ ] Capacity and performance tests meet the approved baseline

## Application, interfaces, and data

- [ ] Release artifact identity, integrity, configuration, and rollback version recorded
- [ ] Critical interfaces and dependencies pass contract tests
- [ ] Source freeze or coordinated-write plan activated
- [ ] Final synchronization completed
- [ ] Counts, digests, referential integrity, semantic rules, and business totals reconciled

## Cutover and validation

- [ ] Traffic/authority shift executed through the approved mechanism
- [ ] Smoke and priority mission-thread tests pass
- [ ] Security, performance, data, recovery, and monitoring checks pass
- [ ] User and operations acceptance recorded
- [ ] Authority selects accept, observe, remediate, or rollback

## Stabilization

- [ ] SLOs, incidents, defects, findings, capacity, user outcomes, and costs monitored
- [ ] Rollback deadline and data-reversal conditions remain visible
- [ ] Stabilization evidence reviewed
- [ ] Rollback window formally closed by the named authority
- [ ] Legacy decommission plan activated
