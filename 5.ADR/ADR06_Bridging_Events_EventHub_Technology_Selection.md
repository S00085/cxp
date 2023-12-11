# Bridging Events from On-Prem systems to CMP EventHub

* Status: Accepted
* Date: 2023-12-04 


## Context and Problem Statement

The CMP solution expects the all the events to be published to the Azure Event Hub. However the event sources are a mix of on-premise hosted & saas solutions. There needs to be an approach to have these event source publish to CMP and react to events from CMP in a consistent way.

## Decision Drivers <!-- optional -->

* Existing Eventing infrastructure on-premise & saas
* Scalability
* Interoperability

## Considered Options

* Event Bridging from Enterprise Message Broker to Azure Event Hub
* Replace Enterprise Message Broker with Azure Event Hub 


## Pros and Cons of the Options <!-- optional -->

### Event Bridging from Enterprise Message Broker to Azure Event Hub

In This approach, the events from the on-premise systems & saas solutions are published to Solace PubSub+ cloud solution which are then bridged to Azure EventHub through the Solace Azure Event Hub connector. 

| Pros | Cons |
|---|---|
| Existing systems using Solace event broker need not change | Published events need to go through another intermediate broker |
| Solace event pubsub is a mature solution supporting multiple protocols and many connectors for future evolution||

### Replace Enterprise Message Broker with Azure Event Hub

| Pros | Cons |
|---|---|
| No intermediary, events are directly published to Azure Event hub| Scale of change is high since existing systems need to change including on-premise & saas solutions |
||Existing systems become coupled to Event hub and CMP and technology changes at this layer impact existing systems|

## Decision Outcome

Chosen option: "Event Bridging from Enterprise Message Broker to Azure Event Hub", because this option reduces the scale of change in the existing on-premise & saas solutions as well as provides a consistent scalable approach to integrate new Event sources across on-premise & saas solutions.
