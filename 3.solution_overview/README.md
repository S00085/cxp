# Solution Overview
The below diagram provides a conceptual view of the proposed solution - Customer Management Platform (CMP).

![Solution Conceptual View](Customer_Mgmt_Platform_Arch_Katas-CMP_Simplified_Conceptual.svg)

The CMP will provide the below key functions for the Airline

- **Collect** customer related transactions, past journeys, interaction logs etc from Direct channels, Service channels, Airline transactional systems, Partner / service provider systems and other relevant systems
- **Unify** the disparate customer profiles into a unified customer identity & profile along with past journeys, interactions etc. and serve as the single source of truth for a Customer 360 degree view.
- **Protect** the customer personal / profile information by tracking the Customer consent, revocations across the entire Airline system landscape as well as provide data protection capabilities aligning with Regional Data privacy regulations related to handling, processing and disposing of customer personal data
- **Orchestrate** intelligent automated actions to provide a proactive and seamless digital experience for the Customers & Service Agents
- **Publish** the unified Customer 360 degree view of the customer, real-time journey status as well as recommendations / actions for helping service channels to provide a personalized experience for the customers during their interactions

## Key capabilities of proposed solution

The customer management platform (CMP) is envisioned to provide the below key capabilities for the Airline

### Customer Management
The Customer Managment capability provides the core function of building and exposing a unified customer profile along with a near real-time 360 degree view of their preferences, choices, journey status, feedback / complaints. This capability also provides the necessary contextual recommended next steps / actions for Customer service agents to provide a personalized experience for the customer during their interactions. The consents provided by the customers through the various interaction channels (Direct & Service) and necessary revocation capabilities are some of the other key features provided by this capability.

### Case Management
The CMP also provides the ability to create, amend & resolve Cases which are raised through out the customer journey. This capability provides the ability for the airline to Design & implement complex workflow & rules driven case flows within the Customer centric organization

### Journey Orchestration
The Journey orchestration capability provides the ability to intelligently and proactively orchestrate automated actions (compensation, raising cases etc) which are useful during disruption schenarios such as flight cancellation, baggage mishandling etc. 

### Integrate & Publish
The CMP allows integrating data (bulk & streaming) from the channels, backend transactional systems and partner systems to build a unified customer profile with past transactions, journey status using operational events etc. The Customer profile & other cusotmer insights gleaned from this data is exposed as APIs and events which can be consumed by Channels. The solution will also publish anonymized customer segment information for partners aligning to consent & regulatory constraints.
