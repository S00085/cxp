[> Home](../README.md)
| [< Prev](../1.context_and_motivation/README.md)  |  [Next >](../3.solution_architecture/README.md)

---

# Architecture Analysis
Below are the key capabilities or aspects of the envisioned comprehensive customer management platform (CMP)

1. Ability to deliver near real time view of the Customer Journey
2. Ability to deliver a comprehensive customer profile along with segmentation & audience attributes
3. Ability to track, view & manage Customer consent across different channels (including direct & service channels) in a consistent & centralized manner
4. Ability for Data analysts to enhance customer insights with new sources of customer data

## Expected Quality Attributes
Below are the key quality attributes identified for the proposed Customer Management Platform

| S.No. | Quality Attribute | Description / Remarks |
|---|---|---|
|1.| Time Behaviour | It is important that the Customer Management Platform provide a near real-time view of the Customer Journey status|
|2.| Confidentiality | It is important to protect sensitive information (customer personal details, transactions etc) from being disclosed to unauthorized parties. This includes protecting data at rest, in transit, and in use.|
|3.| Integrity | It is important to ensure that the customer personal / profile information has not been tampered with or modified in an unauthorized way. This includes protecting data from unauthorized modification, deletion, or addition|
|4.| Availability | It is important that the key parts of the Customer Management  Platform be available to ensure that Information & related systems are accessible to authorized users & systems when they need them.|
|5.| Authenticity | It is important to ensure that information and communication come from a trusted source. This includes protecting against impersonation, spoofing and other types of identity fraud. For e.g. Customer personal / profile information|
|6.| Non-Repudiation | Non-repudiation is important to ensure that a party (for e.g. Customer) cannot deny having sent or received a message or transaction. For e.g. Customer consents and withdrawals |
|7.| Configurability | The Customer management platform should be highly configurable to support flexibility from a Business standpoint. For e.g. Flexible business rules, workflows, dynamic configuration|
|8.| Interoperability | The system should be able to support multiple forms of integration for both internal & partner systems |
|9.| Scalability / Elasticity | AI / ML driven analytics and recommendations (for next best actions to customer service agents) require more resources on demand at different times |
|10.| Fault Tolerance | The Unified customer profile & near real time view of Customer journey are key capabilities in the Customer management platform which need to be highly fault tolerant|
|11.| Security | Security including Authentication, Authorization are important quality attributes especially since the CMP will maintain sensitive customer related information|
|12.| Maintainability  | Maintainability & evolution of the CMP is an important quality attribute since the system is the foundation of the customer centric organization|


## Key Non-Functional Requirements (Assumptions)

|  |   |
| ------- | --- |
|% Target Availability | 99.99% | 
| Recovery Time Objective within region | Nill (for key critical core components like customer 360 service) , 10 Minutes Non components like Process Modeler  | 
| Recovery Time Objective across region | 10 Minutes | 
| Recovery Point Objective  within region | Nil |
| Recovery Point Objective  across region | Nill (for key critical core components like customer 360 service) , < 1 Minute Non components like Process Modeler |
| Max. number of unplanned outages in a year | 2 | 
| Mean Time between failures | 6 Months | 
| Customer Profile update events (All Channels including Direct, Service channels & Partners)|  400 TPS |
| Customer Profile API Requests from channels & CMP UI| 500 TPS|
| Customer 360 Profile Page Request from CMP UI| 25 TPS |
| Case Management views from CMP UI| 5 TPS |
| Case Management create/updates from CMP & UI| 4 TPS |
| Case Management API requests | 7 TPS |
| Case Management create/updates API requests | 5 TPS |

---

[> Home](../README.md)
[< Prev](../1.context_and_motivation/README.md)  |  [Next >](../3.solution_architecture/README.md)

