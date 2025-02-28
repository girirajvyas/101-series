# Micro-services Architecture

# Overview
This section is not for someone who is starting with microservices and want to get started.  
This is for some one who might have some knowledge and want to revalidate the things or see topics he might have missed

# Contents

 - Introduction
   - Overview
   - Advantages
   - Challenges
   - Why micro-services fail?
   - Building SaaS Micro-Services (12 Factor App)
 - Basics
   - CAP Theorem
   - Scale Cube
   - Sharding
   - Polyglot Programming
   - Polyglot DB
 - Implementation
   - Frameworks/Languages
 - Database
 - NFRs for Microservices
   - Scaling

## Summary Topics
Microservices Intro
 - Monolith vs microservices
 - 12 factor app
 - challenges                  
  - Service discovery          : Spring cloud netflix eureka : https://spring.io/guides/gs/service-registration-and-discovery/
  - Load balancing             : Spring cloud load balancer
  - Security                   : Spring cloud API gateway, Spring security
  - Configuration management   : Spring cloud config server
  - Logging and debugging      : Spring cloud sleuth and zipkin
  - Testing                    : Spring cloud contract
  - Communication              : Kafka, MQs
  - Data Consistency           : SAGA Patterns
  - Deployment, Scaling        : Docker, Kubernetes
 - Typical MSA
 
 - RestFul Services
 - Representational State Transfer
 - Building micro-services with spring boot
 - Testing
 - Architecture patterns

# Introduction 

## 1. Overview

**"Micro-services are:  
  - Variant of SOA (Service Oriented Architecture)  
  - Structures application as a collection of loosely coupled services  
  - Services are fine-grained and protocols are lightweight  
  - Single DB per Micro-services (Recommended)  
  - Easy to develop, deploy, test and enables continous delivery  
  - It is divided on the basis of domains (Account, Cart..)
  - Owned by a small team
  - Can be written in different programming languages and use different data storage technologies

**Must reads before proceeding**  
 - https://martinfowler.com/articles/microservices.html (This is an older article before they wrote the below)
 - https://martinfowler.com/microservices/

**Good reads**  
 - https://www.atlassian.com/continuous-delivery/microservices/building-microservices
 - https://microservices.io/

## Advantages

Polyglot programming is the practice of writing code in multiple languages to capture additional functionality and efficiency not available in a single language. The use of domain specific languages (DSLs) has become a standard practice for enterprise application development.

**Advantages:**  
 - **Independent Scaling (Refer ScaleCube)**– Each module in microservices can scale independently through
    - X-axis scaling – by cloning with more memory Or CPU
    - Y-Axis scaling - by deploying multiple instances
    - Z-axis scaling – by size using sharding
 - **Modular** – As the application is broken into smaller chunks, it is easy for developers to develop and maintain.
 - **Adaptive** – Adapting new technology along with process is easy due to loose coupling.
 - **DURS** - Each service in microservices architecture can be independently DURS (Deployed, Updated, Replaced & Scaled)
 - **Resilient** - Even the failure of a single module won’t affect the remaining part of applications.(Highly dependent on modularity)
 - **Microservices guarantee increased the autonomy of development teams (speed to market), better fault isolation (reliability), re-usability and scalability.**
 - Continuous delivery through **DevOps**
 - **Decentralized governance**
 - Availability
 - Auto-Provisioning in case deployed on cloud

## Challenges

 - Communication between services is complex/overhead
 - Since there are more no of services, effiecient Intercommunication is a challenging task.
 - Testing complete system is more complicated.
 - Deployment challenges
 - Monitoring challenges (See sleuth/Zipkin for solution)
 - Multiple point of failures

## Micro-services fails because of below points
Even though we have seen the advantages above, we should know that it can fail because of the reasons below
Source: [10 Tips for failing badly at Microservices by David Schmitz](https://www.youtube.com/watch?v=X0tjziAQfNQ)
  
  10. Go Full scale polyglot
  9. The Monolith database
  8. The event monolith 
  7. Home grown monolith
  6. Think of meat cloud - do everything yourself and dont automate ci/cd
    - Optimize your revenue
      - WKPT? Who wants it to be done, who knows to do it, Who has the required privileges, who has Time to actually do it?
  5. Distributed monolith (Combine the complexity of a microservice architecture with the rigidity and fragility of a monolith)
     - Avoid circuit breakers
  4. SPA Monolith
  3. Decision monolith
  2. Monolithic business
  1. Use HR driven architecture

**Good Reads/Watch:**
 - https://www.youtube.com/watch?v=X0tjziAQfNQ
 - https://medium.com/xebia-engineering/11-reasons-why-you-are-going-to-fail-with-microservices-29b93876268b


## SOA vs Microservices
|Sr. no| Micro-services                                              | Service Oriented Architecture (SOA)               |
|-----:| -------------                                               |:-------------:                                    |
|  1   | Designed to host services which can function independently. | Designed to share resources across services |
|  2   | Fine-grained services                                       | Larger, more modular services |
|  3   | Each service can have an independent data storage           | Involves sharing data storage between services   |
|  4   | Communicates through an API layer                           | Communicates through an ESB |
|  5   | Uses REST and JMS                                           | Uses protocols like SOAP and AMQP |
|  6   | Better for smaller and web-based applications               | Better for large scale integrations|

# Basics

## Scale Cube

To scale microservices we can use [scale cube](https://microservices.io/articles/scalecube.html) reference.

[Wiki](https://en.wikipedia.org/wiki/Scale_cube): "The scale cube is a technology model that indicates three methods by which technology platforms may be scaled to meet increasing levels of demand upon the system in question."  

For Scaling Database, you use Database Sharding i.e Z-axis
 - https://medium.com/@jeeyoungk/how-sharding-works-b4dec46b3f6


## CAP Theorem

It states that it is impossible for a distributed data store to simultaneously provide more than two out of the following three guarantees
  1. **Consistency:** Every read receives the most recent write or an error.
  2. **Availability:** Every request receives a (non-error) response – without guarantee that it contains the most recent write.
  3. **Partition tolerance:** the system continues to operate despite arbitrary partitioning due to
network failures.

**Good Reads:**  
 - https://robertgreiner.com/cap-theorem-revisited/
 - https://searchapparchitecture.techtarget.com/tip/The-CAP-theorem-and-how-it-applies-to-microservices

## Best Practices and naming conventions
 - Naming conventions will be same as the technology being used for communication, for instance in case of REST it will be resource based endpoints

### REST API Documentation  
  - **Swagger ( OpenAPI Specification ):** From January 1st 2016 the Swagger Specification has been donated to to the Open API Initiative (OAI) and has been renamed to the OpenAPI Specification. The Open API specification is backed by the likes of Google, Microsft and IBM.
  - **RAML  (RESTful API Modeling Language)**    
  - **API Blue Print**   

### Database:  

Sure. Here are two separate tables, one focusing on SQL databases and another on NoSQL databases.

**SQL Databases**

| Database | License | Description | Use case | Advantages | Limitations |
|---|---|---|---|---|---|
| MySQL | GPL License | Open-source relational database | Web-based applications | Popular, widely used, supports structured data | Scalability issues, may be slower with large data volumes |
| PostgreSQL | PostgreSQL License | Advanced, open-source object-relational database | Complex queries, heavy transaction load | Extensible, supports large amount of data types | Can be slower than other databases |
| Oracle Database | Commercial | Multimodel database management system | Large scale enterprise systems | Reliable, robust, supports large databases | Expensive, complex to learn |
| SQL Server | Commercial | Relational database management system by Microsoft | Large scale enterprise systems | High performance, good support | Licensing costs, requires regular maintenance |
| MariaDB | GPL License | Open-source fork of MySQL | Web-based applications | High compatibility with MySQL, more advanced features | Can be slower than MySQL, requires more storage space |
| SQLite | Public Domain | Self-contained, serverless and zero-configuration database system | Embedded applications | Lightweight, easy to use | Not suitable for large scale applications, multi-user environments |

**NoSQL Databases**

| Database | License | Description | Use case | Advantages | Limitations |
|---|---|---|---|---|---|
| MongoDB | Server Side Public License | Document database designed for ease of development and scaling | Big data, content management | High performance, easily scales | Data size generally larger than equivalent in SQL |
| CouchDB | Apache 2.0 | Open source NoSQL database | Web applications | Easy replication, convenient web interface | Limited query options, slower than SQL databases |
| Cassandra | Apache 2.0 | Highly scalable, distributed NoSQL database | High velocity applications, IoT | Highly scalable, replicated across many servers | Complex to set up, steep learning curve |
| Redis | BSD 3-clause | Open source, in-memory data structure store | Caching, messaging systems | Extremely fast, supports various data types | Data size limited by memory size, persistence can be complicated |
| HBase | Apache 2.0 | Open-source, distributed, versioned, column-oriented store | Big Data, real-time read/write access to your big data | Linear and modular scalability, strictly consistent reads and writes | High complexity, may need manual optimization |
| DynamoDB | AWS Service (commercial) | Fully managed NoSQL database service by Amazon | Serverless Web applications, mobile backends | Seamless scalability, built-in security  | Not open source, costs can scale with usage |

**Good Reads:**  
 - https://towardsdatascience.com/how-to-choose-the-right-database-afcf95541741
 - https://blog.cloud66.com/3-tips-for-selecting-the-right-database-for-your-app/

### CICD  
 GitHUb, Travis CI/ Jenkins, VSTS, JIRA   
 https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment


### Data Infrastructure:  
 AWS Kinesis, Spark and AWS Redshift  

### UI:  
 React/Angular  

### Micro-services Testing
Strangler Application strategy.
Synchronicity
Independence
Resiliency --
Simplicity

Event sourcing
Choreography-based Saga instead of Orchestration-based
microservices architecture that makes use of remote procedure calls

# Micro-services architecture styles

## Different Communication mechanisms
 - Request/Response based
   - Http 
     - REST
     - RPC
     - https://www.smashingmagazine.com/2016/09/understanding-rest-and-rpc-for-http-apis/
     - https://apihandyman.io/do-you-really-know-why-you-prefer-rest-over-rpc/
 - Event based 
 - Hybrid (has both characterstics)

Note: Hybrid above means that it has characterstics of both Request/Response based services and Event based services. There is a concept of Hybrid microservices model which means use what you like of microservices architecture and leave the rest. More details can be found at https://dzone.com/articles/hybrid-microservices-an-insight

## Inter Micro-Service Communication

 - Mesh  
   - Service mesh
   - Event mesh (https://solace.com/blog/event-mesh)
 - API Gateway pattern

Good Read:
 - https://dzone.com/articles/design-patterns-for-microservice-communication

###  API Gateway Vs Service Mesh

Consider below points while deciding which one to use, moreover it is quite possible to use both in your application
 - API gateway is preferrable for outside world communication
 - Service mesh is useful when you have micro-services in multiple technologies (Sidecar pattern)

![Microservices_vs Mesh](https://github.com/girirajvyas/101-series/blob/master/resources/images/microservices/API_Gateway_Vs_Service_Mesh.PNG)

**Good Reads:**  
 - https://dzone.com/articles/api-gateway-vs-service-mesh

# API communication protocols

| Protocol Type | Description                                                       | Use Case                                                | Advantages                                                    | Disadvantages                            |
|---------------|-------------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------------|-----------------------------------------|
| SOAP          | XML-Based messaging over HTTP or HTTPS                            | Used in web services, where the client applications communicates with services using HTTP and XML.|Highly extensible and navigable,Works well in distributed enterprise environments, Language, platform, and transport independent|Complex, requires extensive processing power|
| REST          | Building Scalable APIs using standard HTTP Methods                | Used in web services, mobile services and any public API that needs to handle CRUD operations (Create, Read, Update, Delete).|Scalable, lightweight, easy to use, stateless|Cannot handle real-time communication like WebSockets can, not as robust as SOAP|
| gRPC          | Query Language for APIs, Allowing Clients to Request Specific data| Used in microservices architectures to enable services to communicate with each other efficiently. |Supports various data formats, efficient communication, works over HTTP/2|Lacks browser support, complex error handling|
| GraphQL       | High Performance framework for Remote Procedure Calls using HTTP/2| Used in complex applications where a client needs to aggregate data from different sources in a single request.|Reduced data usage, faster responses, wide adoption in industry|Development overhead, added complexity|
| WebSocket     | Bi-Directional Real time communication protocol                  | Used in real-time applications such as chat applications, real-time financial data display, etc.|Full duplex communication, real-time data transfer|Lacks built-in security features, consumed more resources|
| WebHook       | Event-Driven, Server side mechanism that sends HTTP callbacks     | Used in distributed event notification scenarios, like notifying a user about change in a database or updates on a website.|Real-time data pusher, no need for polling|Requires manual handling of HTTP calls, high latency|
| MQTT          | LightWeight messaging protocol for constrained devices           | Used in Internet of Things (IoT) scenarios where a large number of devices need to communicate efficiently.|Lightweight, Reduced network bandwidth, ideal for IoT devices|Messaging model can be complex to implement, lack of formal service contract|
| AMQP          | Open Messaging protocol for reliable communication                | Used in business messaging scenarios where reliability, delivery guarantees and message ordering are important.|Reliable and guaranteed delivery, Supports multiple messaging patterns|Complex protocols and difficult to implement, more resource-consumptive compared to other messaging protocols|


# Implementation

## Building SaaS Micro-Services (12 Factor App)

In case you are planning to build a **'Software as a Service' (SaaS) application**, Your application must adhere to **[12 factor apps](https://12factor.net/)** that outlines and describes them in detail.  

**I. Codebase:** One codebase tracked in revision control, many deploys  
**II. Dependencies:** Explicitly declare and isolate dependencies  
**III. Config:** Store config in the environment  
**IV. Backing services:** Treat backing services as attached resources  
**V. Build, release, run:** Strictly separate build and run stages  
**VI. Processes:** Execute the app as one or more stateless processes  
**VII. Port binding:** Export services via port binding  
**VIII. Concurrency:** Scale out via the process model  
**IX. Disposability:** Maximize robustness with fast startup and graceful shutdown  
**X. Dev/prod parity:** Keep development, staging, and production as similar as possible  
**XI. Logs:** Treat logs as event streams  
**XII. Admin processes:** Run admin/management tasks as one-off processes  

**Good read:** 
 - https://12factor.net/
 - https://medium.com/hashmapinc/how-i-use-the-twelve-factor-app-methodology-for-building-saas-applications-with-java-scala-4cdb668cc908

## 3 factor App
 - https://3factor.app/

## Frameworks Languages

Micro-services can be written in below frameworks:  

 - Spring boot
 - Play-Framework(written in scala)
 - Grails
 - [AWS](https://blog.thundra.io/microservices-on-aws-an-in-depth-look)

**Good Read:**
 - https://www.clariontech.com/blog/5-best-technologies-to-build-microservices-architecture
 - https://dzone.com/articles/3-popular-frameworks-to-build-microservices?fromrel=true
 - https://medium.com/microservices-architecture/top-10-microservices-framework-for-2020-eefb5e66d1a2#:~:text=Spring%20Boot%20is%20popular%20Java%20framework%20for%20writing%20Microservices.&text=Spring%20Boot%20allow%20large%20scale,well%20as%20large%20scale%20system.

 - Spring boot
 - Netflix OSS (Netflix open source software)
    - ZUUL Gateway
    - Hystrix circuit breaker
    - Ribbon Load balancer
    - Eureka Service registry

 Different dependencies solving similar problem  
 e.g. you can have service registry with the Eureka Server( in Netflix OSS) and same can be achieved with Zookeper and Consul.
 You have to determine based on the requirement which will fit your requirement better

 Eureka/Ribbon/Feign/Hystrix  
 Testing: JUnit, Mockito  
 OAuth: Gluu
 Repo to store artifacts (npm, mvn): Jfrog

 **B. Play Framework**  
 Java/Scala and Akka  
 Testing: JUnit, ScalaTest, FrisbyJS, Calabash Selenium  

## Micro-services with Netflix OSS

![Microservices_Architecture](https://github.com/girirajvyas/101-series/blob/master/resources/images/microservices/Microservices_Architecture.PNG)

```java
                                            Zuul
          ____________________________________|_________________________________
         |                                                                     |
       Eureka                                                     Same as left hand side
         |
     Appserver (registered with spring boot app name in Eureka)
         |
Mongo            httpd - > tibco load balancer
```

### Architecture can be designed in below way

Common Components

1. msparentpom
   Common dependencies across all micro-services created **on the same platform**
   update dependencies at one place and it will be available everywhere   

2. CCCLib (Cross cutting concerns like logging, auditing)

3. MSLib (Archetype, security)

Common Infrastructure that these microservice will use

 - Discovery/Naming Server
 - API gateway
 - Centralized logging


Flow:
```
@Produces(value=MediaType.APPLICATION_JSON)
@Consumes(value=MediaType.APPLICATION_JSON)
@Path(“/”)
Public  interface DummyEP {
      @Post
     @Path(value = “/insert”)
     Response insertEmployee(InsertEmployeeRequest req);
}
```

```
@EnableZuulGateway
```

```
@EnableEurekaServer
```

## Testing 

Levels of testing is explained in very detail at https://martinfowler.com/articles/microservice-testing/

Consider you have Micro-Service Project that is dependent on the local DB for fetching data for few of the services whereas some services also calls other services to get the data.  
 
 **Local DB** - data can be inserted in embedded Mongo of @Before method so that the data is available when the tests are ran and can be validated.  
 **Other services** - Mock the response via WireMock and validate the tests  

 You can find the same demonstrated below. 

![Microservices_Test](https://github.com/girirajvyas/101-series/blob/master/resources/images/microservices/Microservices_Testing.PNG)

Steps to enable the above testing  

**1. Add dependencies in POM**

```mvn
    <!-- Test -->
    <!-- https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-test -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>

    <!-- https://mvnrepository.com/artifact/de.flapdoodle.embed/de.flapdoodle.embed.mongo -->
    <dependency>
        <groupId>de.flapdoodle.embed</groupId>
        <artifactId>de.flapdoodle.embed.mongo</artifactId>
        <scope>test</scope>
    </dependency>

    <!-- https://mvnrepository.com/artifact/cz.jirutka.spring/embedmongo-spring -->
    <dependency>
        <groupId>cz.jirutka.spring</groupId>
        <artifactId>embedmongo-spring</artifactId>
        <version>1.3.1</version>
        <scope>test</scope>
    </dependency>

    <!-- https://mvnrepository.com/artifact/com.github.tomakehurst/wiremock -->
    <dependency>
        <groupId>com.github.tomakehurst</groupId>
        <artifactId>wiremock</artifactId>
        <version>2.20.0</version>
        <scope>test</scope>
    </dependency>
        
```

Contract testing

**Good Reads:**
 - https://dzone.com/articles/using-wiremock-to-test-against-3rd-party-services

# NFRs for Microservices

## 1. Scaling microservices

 - Read ScaleCube in Basics section
 - 2 ways:  
   - Vertical(Y-Axis): increase hardware capability
   - Horizontal(X-Axis): deploy multiple application instances (redundancy), application should be modular is mandatory requirement
   - Z-axis: For Scaling Database, you use Database Sharding
 - Architecture level:
   - Improve modularity
   - Improve caching 
     - for inter service communication
     - caches within each service to reduce number of db calls
     - Distributed caching where first we check in distributed cache and then to db

## 2. Resilient Microservices

 - https://dzone.com/articles/libraries-for-microservices-development

## 3. Performance
Time to respond and load up for a user (ex. within 2 secs)
 
**How to improve:**  
 - `Code level:` Ensure java best practices
   - Ensure unnecessary objects are not created
   - Ensure correct data structure/algo is used according to the scenarios
 - `Database(datastores):`
   - db are tune for the type of queries
   - proper indexes, properly normalized
 - `Caching`
   - cache all the redundant data for static fields
   - distributed caching is required if you have scaled your application and there are 10 instances
 - `Capacity`
   - before redundancy see vertical scaling option by increasing CPUs
 - `Redundancy`
   - Build redundancy (horizaontal scaling), 
 - `Modularity:`
   - Make sure you app is modular so that it can be scaled

**Best practices:**  
 - Define performance requirements defined before dev starts:
    - peak load
    - users
    - response time
 - Start testing early (it should be included in your scrum)
 - Profiling
   - frequently profiling
   - tune your code regularly
 - Visibility
   - you should have overall visibility so that you know where to start instead of doing it overall
   - how much time is spent at each microservice
   - how much time it is taking to return data from a database

## 4. Availability
 - measure of how often the system is providing the availability

 - Diff availability needs: 
   - internal application: low
   - available on internet: very high

 - multiple components are deployed and hence no single point of failure
 - reduced bottlenects like single monolith db or application

 - https://en.wikipedia.org/wiki/Reliability,_availability_and_serviceability

## 5. Consistency
 - BASE
 - https://en.wikipedia.org/wiki/Eventual_consistency

## 6. Security
 - https://dzone.com/articles/how-do-you-secure-microservices
 - https://owasp.org/www-project-top-ten/

# Architectural Patterns for Micro-services

 - **Decomposition Patterns**
   - Decompose by business capability 
   - Decompose by subdomain
   - Strangler pattern
 - **Integration Patterns**
   - API Gateway pattern
   - Aggregator pattern
   - Client-Side UI composition pattern
 - **Database Patterns**
   - Database per service
   - Shared database per Service
   - Command Query Responsibility Saggregation
   - SAGA Pattern
 - **Observer Patterns**
   - Log Aggregation Pattern
   - Performance Metrics
   - Distributed tracing
   - Health check
 - **Cross cutting concerns Patterns**
   - External Configuration
   - Service Discovery pattern
   - Circuit breaker pattern
   - Blue green deployment

# Anti-patterns
 - Multiple services from the start:
 - Relying on a single Interservice communication mechanism:
 - Complex Interservice dependency and Circular Service dependency:
 - Idea of not considering Serverless, Kubernetes from the beginning:
 - Inability of Monitoring and Performance Testing in place:
 - Poor Versioning Strategy

**Good reads:**  
 - https://blog.aspiresys.com/software-product-engineering/microservices-antipatterns-avoiding-pitfalls-and-driving-stability/

## Frequent Questions

## References

 - https://en.wikipedia.org/wiki/Microservices
 - https://medium.com/microservices-in-practice/microservices-in-practice-7a3e85b6624c
 - https://dzone.com/articles/design-patterns-for-microservices
 - Best: https://medium.com/@madhukaudantha/microservice-architecture-and-design-patterns-for-microservices-e0e5013fd58a

NFR: 
 - https://www.youtube.com/watch?v=R3j0Z1c-0qY&list=PLBBog2r6uMCTB4bYedn-WMW2MoYWk_sgf&index=19
 - https://www.springboottutorial.com/availability-non-functional-requirement-in-microservices
 
Best practices: 
 - https://github.com/in28minutes/java-best-practices#should-i-be-an-expert-at-all-design-patterns
 - http://progressivecoder.com/spring-cloud-microservices-a-detailed-guide/
 - https://dzone.com/articles/design-patterns-for-microservices
 - https://www.edureka.co/blog/microservices-design-patterns#Chained

Books to read(TODO):
 - Building Microservices by Sam Newman
