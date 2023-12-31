
[> Home](../README.md)
| [< Back](../3.solution_architecture/README.md#architecture-decision-records-adrs)

---

# Bridging Events from On-Prem systems to CMP EventHub

* Status: Accepted
* Date:  07-12-2023

## Context and Problem Statement

The CMP solution expects the all the events to be published to the Azure Event Hub. However the event sources are a mix of on-premise hosted & SaaS solutions. There needs to be an approach to have these event source publish to CMP and react to events from CMP in a consistent way.

## Decision Drivers <!-- optional -->

* Existing Eventing infrastructure on-premise & SaaS
* Scalability
* Interoperability

## Considered Options

* Event Bridging from Enterprise Message Broker to Azure Event Hub
* Replace Enterprise Message Broker with Azure Event Hub 


## Pros and Cons of the Options <!-- optional -->

### Event Bridging from Enterprise Message Broker to Azure Event Hub

In This approach, the events from the on-premise systems & SaaS solutions are published to Solace PubSub+ cloud solution which are then bridged to Azure EventHub through the Solace Azure Event Hub connector. 

| Pros | Cons |
|---|---|
| Existing systems using Solace event broker need not change | Published events need to go through another intermediate broker |
| Solace event pubsub is a mature solution supporting multiple protocols and many connectors for future evolution||

### Replace Enterprise Message Broker with Azure Event Hub

| Pros | Cons |
|---|---|
| No intermediary, events are directly published to Azure Event hub| Scale of change is high since existing systems need to change including on-premise & SaaS solutions |
||Existing systems become coupled to Event hub and CMP and technology changes at this layer impact existing systems|

## Decision Outcome

Chosen option: "Event Bridging from Enterprise Message Broker to Azure Event Hub", because this option reduces the scale of change in the existing on-premise & SaaS solutions as well as provides a consistent scalable approach to integrate new Event sources across on-premise & SaaS solutions.

---

[> Home](../README.md)
| [< Back](../3.solution_architecture/README.md#architecture-decision-records-adrs)