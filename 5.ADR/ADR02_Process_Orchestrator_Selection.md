# Process Orchestrator Selection to extend Journey Orchestrator Capability

* Status: Accepted 
* Date: 10-12-2023


## Context and Problem Statement

For orchestrating customer journeys, we will use a Journey Orchestrator Microservice. Complex orchestrations requiring greater flexibility will be handled by the external Process Orchestration Engine as extension to Journey Orchestrator Microservice.

## Decision Drivers

* Usabilty targeting non techinical user
* Cost optimal solution 
* Strong Community Support 

## Considered Options

Some of the widely recognized process orchestration engines are: Camunda, JBoss jBPM, Kestra , Apache Airflow, AWS Step Functions Microsoft Power Automate, IBM Business Process Manager, Pega BPM etc 
In our context of Customer Management platform due to cost contraints IBM Business Process Manager is excluded

## Pros and Cons of the Options 

### 1. Camunda
- **Functionality**: Strong BPMN, CMMN, and DMN support.
- **Integration**: Good with Java and Spring applications.
- **User Interface**: User-friendly modeler and management console.
- **Use Cases**: Versatile for detailed workflow and decision automation.
- **Community and Support**: Strong community and documentation.

### 2. JBoss jBPM
- **Functionality**: Integrates BPMN with Drools for business rules.
- **Integration**: Good for Java EE and Spring applications.
- **User Interface**: More technical, less intuitive than Camunda.
- **Use Cases**: Suitable for complex rule-based automation.
- **Community and Support**: Good, especially in Red Hat ecosystem.

### 3. Kestra
- **Functionality**: Focuses on data pipelines.
- **Integration**: Strong with data services.
- **User Interface**: Developer-focused.
- **Use Cases**: Best for data-driven workflows and ETL.
- **Community and Support**: Growing community.

### 4. Apache Airflow
- **Functionality**: For scheduling and monitoring data pipelines.
- **Integration**: Strong with data processing tools, Python-centric.
- **User Interface**: Code-based DAGs.
- **Use Cases**: Ideal for data engineering and batch processing.
- **Community and Support**: Large community and plugins.

### 5. AWS Step Functions
- **Functionality**: Serverless orchestration, AWS integration.
- **Integration**: Best within AWS ecosystem.
- **User Interface**: JSON-based state machines, visual designer.
- **Use Cases**: Serverless workflows and microservices.
- **Community and Support**: AWS support.

### 6. Microsoft Power Automate
- **Functionality**: Low-code, routine business task automation.
- **Integration**: Strong with Microsoft and third-party apps.
- **User Interface**: User-friendly, low-code.
- **Use Cases**: Office automation, simple integrations.
- **Community and Support**: Microsoft support.

## Shorlist Outcome

 Camunda & Microsoft Power Automate is shorlisted for further detailed analysis for factors like User-friendly UI, Azure ecosystem etc  

 # Detailed Comparison: Camunda vs Microsoft Power Automate

An in-depth look at the features, integration capabilities, usability, and organizational suitability of Camunda and Microsoft Power Automate.

## Option #1 - Camunda 

### Functionality
- Comprehensive support for BPMN, CMMN, and DMN.
- Ideal for complex workflow automation and decision-making processes.
- Wide-ranging capabilities in business process modeling and execution.

### Integration
- Strong in Java-based environments.
- Embeddable in existing applications or usable as a standalone.

### User Interface
- Robust modeler for designing workflows.
- More technical interface, offering extensive control.

### Scalability
- Highly scalable for both small and large enterprises.
- Capable of handling complex and high-volume processes.

### Use Cases
- Suited for detailed process modeling and automation.
- Applicable in industries with complex workflows.

### Community and Support
- Strong community, extensive documentation, and professional support.

## Option #2 - Microsoft Power Automate

### Functionality
- Low-code platform for automating routine tasks.
- Strong in workflows between Microsoft and third-party services.
- Less suited for complex process modeling.

### Integration
- Excellent with Microsoft 365 and various third-party apps.
- Focus on office automation and simple integrations.

### User Interface
- User-friendly, designed for non-technical users.
- Drag-and-drop interface for quick workflow creation.

### Scalability
- Suitable for small to medium-sized processes.
- May struggle with very complex/high-volume workflows.

### Use Cases
- Ideal for automating office tasks and simple integrations.
- Preferred for ease of use and quick deployment scenarios.

### Community and Support
- Backed by Microsoft’s support network and documentation.

## Decision Outcome

- **Advanced Process Modeling**: Superior BPMN, CMMN, and DMN support for detailed and complex process modeling.

- **Technical Control and Integration**: Greater technical control and better integration, especially in Java-based ecosystems.

- **Scalability**: Excellently suited for complex and high-volume workflows.

- **Versatility in Use Cases**: Appropriate for a range of industries with complex workflows and decision automation.

- **Strong Community and Professional Support**: Ensures long-term viability and ease of troubleshooting.

Camunda is preferred over Microsoft Power Automate for the need of sophisticated business process management, scalability, and technical depth and also provide deployment portability to any cloud providers. 

### Reference 
https://camunda.com/blog/2014/01/benchmarking-camunda-process-engine/

