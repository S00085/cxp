# Customer Profile Database Selection - Graph DB vs RDBMS vs Document DB)

* Status: Proposed
* Date:  06-12-2023

## Context and Problem Statement

Selection of the right type of database from Graph DB, RDBMS and Document DB. 

## Decision Drivers

* Data modelling efficiency
* Performance
* Ease of use
* Flexibility

## Considered Options

* Graph database
* Relational database (RDBMS)
* Document database

## Pros and Cons of the Options

### Graph database

* Good flexibility, the schema and structure of graph models can change with your applications. Data analysts can add or modify existing graph structures without impacting existing functions. There is no requirement to model domains in advance
* Good performance, graph database performance improves by several orders of magnitude when querying relationships. Performance stays constant even when graph data volume increases.
* Good efficiency, Graph technologies take advantage of linked nodes.Traversing the joins or relationships is a very fast process, as the relationships between nodes are not calculated at query times but are persisted in the database.

### Relational database (RDBMS)

* Good for data integrity, Relational databases use a set of constraints to enforce data integrity in the database.
* Good for transactions, database transaction is one or more SQL statements that are executed as a sequence of operations that form a single logical unit.
* Good for ACID compliance.
* Bad, Relational database models become less optimal as the volume and depth of relationships increase.
* Bad, Graph queries are shorter and more efficient at generating the same reports compared to relational databases.
* Bad, data domains has to be modelled in advance.

### Document database

* Good for handling semi-structured and unstructured data.
* Good, Document databases provide the ability to store and retrieve huge amounts of data rapidly and efficiently.
* Good, highly scalable - They provide automatic sharding, replication and other functionalities that help in scaling.
* Good, highly flexible - Document databases are highly flexible and can adapt to changes in data schemas, as they do not enforce the consistency rules.
* Good, Cost effective - Document databases can scale horizontally across multiple commodity servers.
* Bad, Document database are not used to handle relational data.

## Decision Outcome

* Chosen option - Graph database

Decision influenced by the following factors
* Customer 360 database ill hold customer details along with its relationship with various entities.
* Graph database is having better performance than RDBMS even when the volume and depth of relationship increases.
* Flexibility to save records as Nodes and its relationship as Edges, with no need to perform any advance modelling.
* Better performance in data traversal.