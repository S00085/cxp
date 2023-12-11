
[< Back](../3.solution_architecture/README.md)

---
# Deployment_strategy - Azure Functions vs AKS vs ACI

* Status: Accepted
* Date:  07-12-2023

## Context and Problem Statement

Both serverless computing and containers enable developers to build applications with far less overhead and more flexibility than applications hosted on traditional servers or virtual machines.
There are multiple options we could take into consideration as deployment platforms such: on-premise servers, serverless solutions, container orchestrations such as Kubernetes (on-premise or as PaaS).

## Decision Drivers

* Cost
* Scalability
* Maintenance
* Testing
* Time of deployment  

## Considered Options

* Serverless - Azure functions
* Container orchestration services - Azure Kubernetes Service (AKS)
* Container services - Azure Container Instances (ACI)

## Pros and Cons of the Options

### Serverless - Azure functions

* Good, serverless can offer extremely low-cost systems
* Good, Azure Functions very quickly scales from 0 to dozens of servers under heavy load, and you're still only paying for the time your functions are actually running. In a serverless architecture, the backend inherently and automatically scales to meet demand.
* Good, serverless promotes rapid development by providing a simplified programming model that integrates easily with a selection of external services. For example, with Azure Functions, makes it trivial to connect to many Azure services such as Azure Service Bus, Cosmos DB and Key Vault. 
* Bad, with serverless you need to come up with your own strategy for how developers can test a microservice in the context of the overall application. It is difficult to test serverless web applications because the backend environment is hard to replicate on a local environment.
* Bad, with serverless you're typically exposing each microservice with a HTTP endpoint publicly on the internet. That means each service could potentially be attacked, and great care must be taken to ensure only trusted clients can call each service.
* Bad, single execution time limited to 10 minutes by default.


### Container services - Azure Kubernetes Service (AKS)

* Good, AKS is a free managed service. Customers only pay for agent nodes used by the clusters. There is no need to pay for any of the masters, which are configured and deployed by AKS.
* Good, for local development and easier testability in a microservice environment.
* Good, simplifies the security as its enforced as a cross-cutting concern. With AKS you don't need to expose all your microservices outside the cluster - only certain services are exposed by an ingress controller.
* Good, component has no vendor dependency hence could be shifted to any platform later if necessary.
* Good, AKS handles most of the complexity and operational tasks related to managing Kubernetes. AKS manages Kubernetes master nodes, while customers manage and maintain agent nodes.
* Good, Azure offers built in monitoring - Azure Monitor.
* Bad, slower startup and slower scale out compared to Azure functions.
* Bad, in a container-based architecture, the number of containers deployed is determined by the developer in advance
* Bad, complex setup.

### Container services - Azure Container Instances (ACI)

* Good, easy way to run containers in cloud eliminating the need for VM and complex orchestration services.
* Good, it is ideal for simple container-based workloads like smaller-scale apps, build jobs, and task automation.
* Good, component has no vendor dependency hence could be shifted to any platform later if necessary.
* Good , ACI scales using container groups — a collection of containers running on the same host.
* Bad, slower startup and slower scale out compared to Azure functions.
* Bad, ACI requires a manual installation and configuration of a monitoring solution.
* Bad, in a container-based architecture, the number of containers deployed is determined by the developer in advance

## Decision Outcome

Chosen option: Container services - Azure Kubernetes Service (AKS).

Decision influenced by the following factors
* Avoid vendor dependency.
* Ease of integrations with existing on-premise applications and legacy systems.
* Ease of testability and maintenance

---

[< Back](../3.solution_architecture/README.md)