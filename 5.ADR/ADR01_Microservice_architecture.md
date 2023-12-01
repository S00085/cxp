# ADR01 Microservice Architecture

## Title
Use the microservice architecture style

## Status
Proposed

## Context
Microservice architectures are commonplace nowadays. By itself, this is not a good enough reason to choose
a microservice architecture. Below, we list some pros and cons of such a decision and why microservice architecture is the way to go.

## Decision
We will use the microservice architecture style for backend systems.

## Consequences

### Flexibility
Micro architectures come with the great benefit of flexibility. When implemented correctly, teams can work
independently on their respective services. All that is needed for inter-service communication
are clean service interfaces.

Deploying microservices also can be done independently, increasing flexibility.

For a startup with limited resources, flexibility to allocate these resources where the need is the greatest comes as
a great benefit.

### Scalability
The other big selling point of microservice architectures is of course scalability. Different services scale at
different speeds and predicting which ones will scale by how much is a hard task. With a microservice architecture,
services can be scaled reactively.

### Improved fault isolation
Under a monolithic architecture structure, when developers experience a failure in one element of the architecture, it will collapse all architecture components. With a microservices architecture, if one service fails, it’s much less likely that other parts of the application will fail because each microservice runs independently. 
However, businesses need to be careful, because large volumes of traffic can still be overwhelming in some cases. The benefit of a microservice architecture is that developers can deploy features that prevent cascading failures. 
A variety of tools are also available, to build fault-tolerant microservices that help improve the resilience of the infrastructure

### Simpler to deploy
A microservices architecture lets teams deploy independent applications without affecting other services in the architecture. This feature, one of the pros of microservices, will enable developers to add new modules without redesigning the system's complete structure. 
Businesses can efficiently add new features as needed under a microservices architecture.

### Program language and technology agnostic
A microservice application can be programmed in any language, so dev teams can choose the best language for the job. The fact that microservices architectures are language agnostic also allows the developers to use their existing skill sets to maximum advantage – no need to learn a new programming language just get the work done. 
Using cloud-based microservices gives developers another advantage, as they can access an application from any internet-connected device, regardless of its platform

### Reusability
Some microservice applications may be shareable across a business, the same microservice application can be used in each instance

### Referential Integrity
One of the big drawbacks of microservice architectures is the loss of referential integrity. Since each
microservice owns their own storage, references carried across services can get out of sync. Here is where
clean interfaces and processes come back into the picture. Good communication between teams can help alleviate
these problems. In a startup environment, this can be as simple as a Slack channel.

### Complexity
Debugging can be more challenging with a microservices architecture. Each microservice will have its own set of logs. 
This provides a minor headache when tracing the source of a problem in the code.

### Interface control
Since each microservice has its own API, any application using that service will be affected if you change the API, and that change is not backward compatible. 
Any large operation using a microservices architecture will have hundreds, even thousands, of APIs so controlling those interfaces becomes critical to the business's operation, which can be a disadvantage to microservices architecture.

### Duplication Overhead
It is inevitable that some code will get duplicated over time since each team operates independently. Finding the
right balance is where the challenge resides. A good reference architecture can help alleviate lots of these concerns.