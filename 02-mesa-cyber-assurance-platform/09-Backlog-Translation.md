# 09 — Architecture-to-Backlog Translation

## Translation pattern

`Mission outcome → Operational scenario → Architecture requirement → Epic → User story → Acceptance criteria → Verification → Evidence`

Architecture intent is not complete when an epic exists. The story must retain the originating risk, affected boundary, interface contract, security acceptance criteria, and verification method.

## Example

- **Mission outcome:** MO-01, timely and traceable risk decisions.
- **Scenario:** SC-03, a high-risk finding affects an inherited service.
- **Requirement:** CYR-010, notify all affected owners when inherited control status changes.
- **Epic:** EP-04, Authorization Dependency Management.
- **Story:** US-09, As a boundary owner, I need a verified impact notification when a provider control changes so that I can reassess mission risk.
- **Acceptance:** dependent boundaries are identified; duplicate notifications are suppressed; impact path and provider evidence are visible; failed delivery is retried and alerted.
- **Verification:** VT-014, simulated provider-status change across three consuming boundaries.
- **Evidence:** synthetic event log, dependency query, notification record, and reviewer result.

## Definition of ready

- Upstream mission/risk trace exists.
- Boundary, data marking, identity, and interface assumptions are known.
- Acceptance criteria include normal, negative, failure, and recovery behavior.
- Verification owner and evidence type are identified.
- Any required ADR is approved.

## Definition of done

- Functional and security criteria pass.
- Contract and regression tests pass.
- Traceability and threat model are updated.
- Evidence is cataloged with provenance.
- Operational monitoring and owner are established.
- Residual limitations are documented and accepted by the proper authority.

See `backlog/epics-and-stories.md`.
