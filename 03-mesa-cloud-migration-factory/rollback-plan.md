# Rollback Plan Template

## Scope

- Workload/wave:
- Cutover window:
- Rollback authority:
- Last responsible rollback point:
- Maximum acceptable reversal duration:

## Triggers

List measurable mission, functional, data, security, performance, dependency, and operational triggers.

## Source readiness

Describe retained source configuration, data authority, credentials, routes, licenses, staffing, and validation.

## Data reversal

Describe data created after cutover, reverse synchronization, duplicate prevention, queued events/messages, reconciliation, and accepted data-loss boundary.

## Technical steps

1. Declare rollback and freeze affected changes.
2. Stop or isolate target processing.
3. Reconcile or reverse post-cutover data according to authority rules.
4. Restore source routes, DNS, interfaces, schedules, and authoritative processing.
5. Validate identity, application, data, mission thread, monitoring, and operations.
6. Notify users, partners, leadership, security, and support.
7. Preserve evidence and initiate corrective-action review.

## Validation and closure

- Source mission-thread tests:
- Data reconciliation:
- Security/monitoring:
- User/operations acceptance:
- Follow-up decision date:
