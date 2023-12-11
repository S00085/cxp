# CaseManagement Component Repository Selection

* Status: Accepted
* Date: 2023-12-10


## Context and Problem Statement

Problem is to select appropriate database for case management repository : RDBM and Document DB  

## Considered Options

* RDBMS (Azure SQL)
* Document DB (Azure Cosmos)

## Pros and Cons of the Options

### RDBMS

#### Data Model
- Structured data with a predefined schema.
- Data stored in tables with rows and columns, emphasizing relations.

#### Query Language
- Utilizes SQL for data manipulation and querying.
- Supports complex queries with JOINs.

#### Scalability
- Typically scales vertically (increasing server capacity).
- Horizontal scaling is more complex.

### Consistency and Transactions
- Strong consistency with ACID transactions.
- Ideal for applications needing strict data integrity.

#### Use Cases
- Suited for well-structured data and relationships.
- Complex reporting and analytics.

#### Flexibility
- Schema changes can be rigid and challenging in rapidly evolving environments.


### Document DB

#### Data Model
- Flexible schema for semi-structured or unstructured data.
- Data stored in documents (e.g., JSON, XML).

#### Query Language
- Custom query languages, varies by database (e.g., BSON in MongoDB).
- Facilitates handling nested and hierarchical data.

#### Scalability
- Designed for horizontal scalability.
- Easily handles large volumes of data and traffic.

#### Consistency and Transactions
- Typically offers eventual consistency; some have tunable consistency models.
- ACID transactions are less common or implemented differently.

#### Use Cases
- Ideal for applications with changing data models.
- Real-time data processing, content management, IoT, etc.

#### Flexibility
- Easy to manage schema changes, accommodating evolving business needs.

## Decision Outcome

Azure Cosmos with Mongo DB API was selected for Case Management repository 

## Why Choose a Document DB

- **Flexibility and Agility**: Accommodates rapidly evolving data structures without costly schema modifications.

- **Ease of Scalability**: Inherently designed for horizontal scaling, essential for handling large data volumes and high throughput.

- **Simplified Data Modeling**: Aligns with developer perspectives on data and code, easing development and iteration.

- **Performance**: Offers faster performance for operations on complex, nested data.

- **Development Velocity**: Accelerates development and deployment cycles, enabling faster business response.

## Use Case Suitability

- Recommended for case management systems needing adaptability, scalability, and operational efficiency.
- Ideal for managing diverse data types and structures, and facilitating rapid application development.

This recommendation aligns with the need for a database that is adaptable, efficient in handling varied data sets, and supports rapid application development, making Document DB an optimal choice for a modern case management system.

## Why Choose a Azure Cosmos DB Mongo API (Related Decision)

- Application is hosted in Azure 
- Application already use Azure Cosmos (Graph) DB for Customer Profile
- Simplify the deplyment as it is managed platform service from Azure  
- Azure Cosmos DB is recommended for the case management system due to its scalability, global distribution capabilities, and flexibility in handling diverse data models. Its performance and cost-effectiveness make it a strong candidate for systems that require rapid access to large volumes of varied data types, especially in a globally distributed context.
- This recommendation aligns with the need for a robust, scalable, and flexible database solution, positioning Azure Cosmos DB as the preferred choice over Azure SQL Database (RDBMS) for the case management system in question.
- Cosmos DB’s multi-model capability allows it to handle various types of data, making it highly suitable for a case management system where data can be structured, semi-structured, or unstructured.
- Global Distribution and Scalability: Its ability to seamlessly scale and replicate data globally ensures high availability and performance, crucial for case management systems that may need to scale rapidly.
- Multiple Consistency Models: Offers a range of consistency models to balance between latency, throughput, and data correctness, which is beneficial in scenarios where these factors vary significantly.
- Performance: Fast access times and low latency in data retrieval are critical for case management systems, and Cosmos DB excels in this area.
- Cost-Effectiveness: While the pricing model is based on RUs, it can be more cost-effective at scale, especially for workloads with unpredictable traffic.

