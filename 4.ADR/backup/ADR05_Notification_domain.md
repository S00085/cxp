# Notification Domain

## Status
Accepted

## Context
The Notification domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. 

## Decision

Notification-Sending will be split into SMS, Email and a Notification Orchestrator (Notification Preference)

## Consequences

**Positive:**

- Functionality split with no overlap
- Scalability managed separately
- Faults in SMS and Email do not bring unrelated functionality down

**Risks:**

- SMS and Email depend on the orchestrator and would be taken down by a fault in the orchestrator. This would be mitigated by having multiple instances of the orchestrator (scalability is managed independently) and so faults would be managed by e.g. Kubernetes.
