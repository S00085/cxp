
[> Home](../README.md)
| [< Back](../3.solution_architecture/README.md#architecture-decision-records-adrs)

---

# Consent change handling approach - decision

* Status: Accepted
* Date:  07-12-2023

## Context and Problem Statement

At present the Customer consent management sprawls across disparate operational systems. Going forward , since CMP will be the single source of truth for Customer consent management, a consistent approach to capture and propagate Consent updates / changes (like revocation) needs to be defined and agreed

## Decision Drivers <!-- optional -->

* Simplicity
* Availability
* Scalability

## Considered Options

* Synchronous approach 
* Asynchronous Event driven approach

## Pros and Cons of the Options <!-- optional -->

### [Synchronous approach]

In this approach the CMP needs to keep track of the consent information across all the operational systems and is also responsible for keeping the operational system in synch with the consents it maintains through synchronous APIs exposed by the operational systems

| Pros | Cons |
|---|---|
| Consent information in CMP is always in synch with the operational systems| Tight coupling since the operational systems need to be available whenever CMP updates the consent |
| | This approach makes the CMP more complex and dependent on the availability of the Operational systems|
| | Since conflict resoultion is CMP's responsibility, Operational system specific concerns seep into CMP which impacts flexibility & maintainability in the long run|
| | All the operational systems need to expose the APIs for CMP to consume|

### [Asynchronous Event driven approach]


In this approach the CMP is responsible only for capturing consent changes and publishing the necessary events. The operational systems are expected to subscribe for the relevent events and react accordingly. 

| Pros | Cons |
|---|---|
| Overall solution is loosely coupled | Consent information will be eventually consistent |
| CMP's consent mgmt. becomes simpler | |
| Conflict resolution lies with operational systems which does not seep into CMP improves scalability, availability & extensibility of the CMP & Consent management as a whole||

## Decision Outcome

Chosen option: "[Asynchronous Event driven approach]", because the approach allows loose coupling with the CMP & the exiting operational systems. This approach also has comparatively high availability & scalabilty characteristics. 

### Implications / Consequences (both +ve & -ve) <!-- optional -->
Below are the key implications of this decision

1. The Operational system's handling the consent needs to ensure that they respect the consent updates / changes and have the necessary capability to ensure that the consent is in synch with CMP
2. Any mismatch with the CMP , the information in CMP wins and the Operational system needs to handle conflict resolution at their end

---

[> Home](../README.md)
| [< Back](../3.solution_architecture/README.md#architecture-decision-records-adrs)