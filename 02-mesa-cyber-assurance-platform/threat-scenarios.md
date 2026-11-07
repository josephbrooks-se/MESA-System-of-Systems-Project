# Threat and Failure Scenarios

| ID | Scenario | Mission effect | Architecture treatment | Residual concern |
|---|---|---|---|---|
| TS-01 | Stolen privileged identity attempts evidence export | Unauthorized disclosure and loss of trust | Phishing-resistant auth, device/workload policy, purpose binding, export approval, audit | Authorized insider misuse |
| TS-02 | Compromised source submits fabricated evidence | False assurance and unsafe decision | Workload identity, signed package, provenance, configuration binding, independent corroboration | Trusted source can still be wrong |
| TS-03 | Finding event is duplicated or reordered | Incorrect status or missed remediation | Idempotency, source versions, sequence metadata, reconciliation | Long partitions complicate conflict resolution |
| TS-04 | Common-control provider silently degrades | Multiple boundaries inherit unrecognized risk | Provider status events, daily reconcile, dependency graph, reopen rules | Provider evidence latency |
| TS-05 | Collector is compromised in an isolated enclave | Manipulated observations or attempted pivot | Least-function design, no inbound command path, signing identity, constrained transfer, revocation | Local physical/admin compromise |
| TS-06 | Evidence store is unavailable | Authorization review delay | Metadata separation, replication, recovery, last validated read-only posture | Current binary evidence unavailable |
| TS-07 | Policy service is unavailable | Access decisions cannot be evaluated | Fail-closed writes, narrowly scoped cached read policy, alerting | Availability versus strict enforcement trade |
| TS-08 | Supplier component vulnerability emerges | Cross-portfolio exposure and schedule disruption | SBOM linkage, supplier identity, affected-asset query, mission prioritization | Incomplete supplier transparency |
| TS-09 | Malicious schema change breaks consumers | Loss or misinterpretation of findings | Contract registry, compatibility tests, approval, version pinning, quarantine | Semantic changes can evade syntax checks |
| TS-10 | Analyst over-trusts dashboard score | Poor residual-risk decision | Display freshness, confidence, limitations, and evidence gaps separately | Human cognitive bias |
| TS-11 | Administrator alters audit data | Loss of accountability | Separation of duties, append-protected ledger, independent export/monitoring | Privileged collusion |
| TS-12 | Cross-boundary transfer releases excess data | Unauthorized disclosure | Minimized export package, markings, policy, approved transfer, review | Incorrect source markings |

## Analysis method

For each scenario, identify threatened assets, preconditions, attack/failure path, mission consequence, existing controls, verification evidence, uncertainty, and residual-risk owner. Scenario priority is mission-informed; source severity alone does not determine response.
