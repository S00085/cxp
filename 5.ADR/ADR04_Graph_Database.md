# ADR04_Graph database - Azure Cosmos for Apache Gremlin vs Neo4j

* Status: Proposed
* Date:  06-12-2023

## Context and Problem Statement

Selection of the graph database for storing Customer profile and relationships

## Decision Drivers

* Data modelling
* Scalability
* Indexing
* Deployment options
* Query language

## Considered Options

* Azure Cosmos for Apache Gremlin
* Neo4j

## Decision Outcome

* Chosen option - Azure Cosmos for Apache Gremlin.

Decision influenced by the following factors
* Azure Cosmos DB is offered as a fully-managed service.

## Pros and Cons of the Options

### Azure Cosmos

*  Good, managed service - Azure Cosmos DB is offered as a fully-managed service in the cloud, providing high availability, automatic backups, and seamless scaling without infrastructure management. It can be integrated with other Azure services and deployed across multiple regions globally.
*  Good, scalability - With a click of a button, Cosmos DB enables you to elastically and independently scale throughput and storage across any number of Azure regions worldwide.

### Neo4j

* Bad, additional management responsibility - Can be deployed in various ways, including on-premises, virtual machines, containers, or in the cloud, offering more deployment flexibility, albeit with additional management responsibilities.
* Bad, limited scalability - Neo4j does support clustering to distribute the graph database over multiple machines, its scalability is comparatively limited.
