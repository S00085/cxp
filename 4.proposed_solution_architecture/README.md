# Proposed Solution Architecture
The proposed solution architecture for CMP is organized around Architecture views and diagrams. Each view may be composed of one or more diagrams illustrating a specific area from a specific perspective.


## Architecture Vision

blah blah

## Guiding Principles

blah blah...

## Architecture Styles & Patterns

blah blah...

## Architecture Views

### Logical View
![Logical Architecture View](Customer_Mgmt_Platform_Arch_Katas-CMP_Logical_View.svg)

##### CMP Portal
blah blah...
##### Gateway Services
blah blah...
##### Customer Mgmt. Services
blah blah..
##### Platform Services
blah blah..
##### Integration Services
blah blah..
##### Identity & Access Mgmt. 
blah blah..
##### Management & Monitoring
blah blah..

##### Data sources & sinks
blah blah...


### Architecture Context
![Architecture Context](CMP_System_Context_View.png)

### Container Diagram
![Container Diagram](CMP_C4_Container_View.png)

### Information Architecture
![Information Architecture](CMP_Information_flow.png)

### Deployment Architecture
![Deployment Architecture](CMP_Deployment_View.png)

* New solution will be hosted on Azure cloud and the region will be chosen closer to the area of operation.
* Azure Express route exist between current on-premise data center and cloud provider.
* Azure eventhub will be used for eventing.
* Azure Open AI will be used for self-service, personalized recommendations and resolution options.

## Key Assumptions & Constraints

* Most of the Key operations systems can publish the requried events in realtime
* Customer Identity is managed in one central IDP (Okta)
* Customer Notification is managed through a central Notification Platform considering Corporate Communciation Standards
* Customer interactions will remain with the existing channels like Contact center, Booking Engine
* Enterprise Data Platform will own the data cleansing and dedupliction of the customer profile sources from various system
* DPO aggremement is available to capture & process social profile informaiton based on optional customer consent **
* Existing systems could either be on-premise or on cloud.
* Consent management notification from Customer Management Platform is expected to be respected and processed by all the systems in the landscape 
* New solution will be use existing enterprise logging solution
* New solution will follow the current monitoring and observability defined by enterprise.
* Existing enterprise defined security standards will be followed by the new solution.
* Compensation management will be handled by an existing system in the landscape.



