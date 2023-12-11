
[> Home](../README.md)
| [< Back](../3.solution_architecture/README.md#architecture-decision-records-adrs)

---

# Stream processing engine selection for Customer Management Platform

* Status: Accepted
* Date:  07-12-2023

## Context and Problem Statement

Stream processing engine is required for building the customer 360 profile and building all the required relationships and also react to complex events patterns from various other operational system

## Decision Drivers

* Application being deployed on Azure
* Immediate insights required using key operational events like baggage handling
* Complex event processing and machine learning with larger data set 
  
## Considered Options

Below stream processing platforms are considered for 360/unified customer management stream processing use case 
* Azure Stream Analytics
* Confluent CEP
* AWS Kinesis Firehose
* Databricks 

## Pros and Cons of the Options

## Integration with Azure Ecosystem
- **Azure Stream Analytics**
  - Seamless integration with Azure services.
- **Confluent CEP**
  - Can integrate with Azure but requires additional setup.
- **AWS Kinesis Firehose**
  - Designed for AWS; complex integration with Azure.
- **Databricks**
  - Strong integration with Azure services.

## Performance and Scalability
- **Azure Stream Analytics**
  - High performance for real-time analytics.
- **Confluent CEP**
  - High throughput and scalability, Kafka-based.
- **AWS Kinesis Firehose**
  - High-throughput but best within AWS.
- **Databricks**
  - Excellent for big data processing and complex analytics.

## Ease of Use and Maintenance
- **Azure Stream Analytics**
  - User-friendly, especially with SQL knowledge.
- **Confluent CEP**
  - More complex setup and management.
- **AWS Kinesis Firehose**
  - More suited to AWS environments.
- **Databricks**
  - Easy-to-use interface, suitable for data scientists.

## Cost
- **Azure Stream Analytics**
  - Cost-effective for Azure-based applications.
- **Confluent CEP**
  - Costs vary based on cluster size and resources.
- **AWS Kinesis Firehose**
  - Charges for data ingested; additional costs in Azure.
- **Databricks**
  - Based on Databricks units consumed.

## Specific Use Cases
- **Azure Stream Analytics**
  - Ideal for real-time analytics and quick insights.
- **Confluent CEP**
  - Suited for high-volume event streaming and complex event processing.
- **AWS Kinesis Firehose**
  - Efficient for data streaming within AWS ecosystem.
- **Databricks**
  - Great for complex analytics, big data processing, and machine learning.

## Decision Outcome

For a unified customer management platform in Azure, **Azure Stream Analytics** and **Databricks** are recommended for their integration with Azure, ease of use, and specific strengths in streaming and data processing. Confluent CEP is a strong option for Kafka-based systems, while AWS Kinesis Firehose may be less suitable due to its AWS-centric design.

## Related Decision 

**Azure Event Hub** will be used since **Azure Stream Analytics** and **Databricks** has seamless integration capabilities with **Azure Event Hub** and also one of Azure managed service which simplifies the deployment

---

[> Home](../README.md)
| [< Back](../3.solution_architecture/README.md#architecture-decision-records-adrs)