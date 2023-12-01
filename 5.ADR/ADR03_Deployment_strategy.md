# ADR03 Deployment Strategy

## Title
Kubernetes for management of containerized applications

## Status
Proposed

## Context
The solution implemented has to be cheap to deploy, maintain, and scale. 
Currently, there are several options that we could take into consideration as deployment platforms such: on-premise servers, serverless solutions, container orchestrations such as Kubernetes (on-premise or as PaaS). 
Finally, we choose to use AKS (Azure Kubernetes Service) provided Azure.

## Decision
Horizontal scaling adheres to our architecture where we can scale individual components of our system according to the component's load.
We want a platform which is capable of autoscaling as per requirement. AKS is a fully flexible system that adapts to use only the resources you need. If you need more resources, it’s as simple as clicking a button and letting the elasticity of Azure container instances do the rest.
When you only use the resources you need, your software (and your business) enjoys the following benefits:
* Reduced cost
* Faster start-up speed
* Easier scaling

## Consequences
**Pros** : AKS takes care of patching, auto-upgrading, monitoring, scaling, and self-healing. This frees development teams from operational tasks and allows them to concentrate on building services.
**Cons** : Learning kubernetes and efforts in setting up the cluster.