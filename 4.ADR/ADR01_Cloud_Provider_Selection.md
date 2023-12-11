# Cloud Provider - Azure vs AWS vs OnPremises

* Status: Accepted
* Date:  07-12-2023

## Context and Problem Statement

Selection of the Cloud provider for hosting the Customer Management platform.

## Decision Drivers

* Cloud-first strategy.
* Microservice architecture
* Event driven architecture
* Micro frontend UI 
* Cloud-agnostic application architecture
* Scalability
* AI / ML capabilities

## Assumption
* Azure is getting used for the Enterprise data platform capabilities.

## Considered Options

* Azure
* AWS
* OnPremises


## Pros and Cons of the Options

### Azure

* **Availability** - Azure provided high availability with Azure availability zones as a part of comprehensive business continuity and disaster recovery strategy with 99.99% uptime SLA.
* **Affordability** - Azure offers cost-savings compared to other clouds through discounts on licensing for Azure. 
    - Azure also allows organization to get more value from their existing Microsoft investment through full integration with Office 365 and Active Directory.
* **Compatibility**: Advantage of Azure is its compatibility with all possible frameworks.
* **Security** - Azure environment is automatically added to Azure Security Center. This offers some protection against attacks by default, as it monitors the resources, alerts you to any potential issues and provides recommendations to improve security.
* **Monitoring** - Collect and analyze the logs and act on telementry data from the cloud environments. 
    - Azure Monitor supports operations at scale by helping you maximize the performance and availability of resources and proactively identify problems.
* **Data Science & Analytics** - Azure provides limitless scale and query data for various data science use case and discover powerful insights across it. 
    - Able to build analytics solutions with various Azure cloud service like Stream Analytics, Steam processing, Machine learning as a Service and many more. 
    - Due to its close integration with data bricks, the Azure data warehouse provides optimal performance in the cloud.


### AWS

* **Availability** - AWS has a global infrastructure to provide high availability for cloud workloads, which includes 21 geographical zones each containing at least three availability zones.
* **Affordability** - In comparison to other cloud service and managed platform providers, AWS is somewhat more costly than Azure.
* **security** - AWS is architected to be the most secure global cloud infrastructure on which to build, migrate, and manage applications and workloads.
* **Monitoring & observability** - AWS provided Full stack observability which includes AWS-native, APM and oper-source solutions. 
    - Provide capability to collect, correlate, aggregate and anlyze telemetry of network, infrastructure and applications.
* **Data Science & Analytics** - AWS also offers data analytics services such as AWS Snowball, direct connect, kinesis data firhose, Data Pipeline Glue, and so on, however it is difficult to handle end-to-end analytics workloads.
 

### On Premises

* **Security** - you store data locally, allowing you greater control.
* **Data Privacy** - Don't need to worry about sensitive data leaving your company.
* **Cost** - Setting up an on-premises can be expensive.
* **Scalability** - All resources must meet recommended hardware requirements, which can be a problem, especially for complex programs.
* **Data backup** - Need to acquire servers, builds a network, and purchase backup hardware for addition data backup when required.

## Decision Outcome

* Chosen option - Azure.

### Decision influenced by the following factors:
* **Data Platform** - The application is dependent on the data platform, which is hosted in the Azure.
* **Data Science** - Manage End to End analytics workloads and advantage to have close integration with data bricks, the Azure data warehouse provides optimal performance in the cloud.
* **Integration** - Application integration with Microsoft components like Microsoft Entra ID, OpenAI and Power BI Analytics.
* **Cost**: In terms of cost, Azure is less expensive than AWS and OnPremises based on application deployable components.
