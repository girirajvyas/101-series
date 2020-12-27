## Micro-services Architecture

This does not have any standard definition, but have different versions that can be summarized as below:

Version 1: 
Quoting the definition from https://microservices.io/
"Microservices - also known as the microservice architecture - is an architectural style that structures an application as a collection of services that are:  
 - Highly maintainable and testable
 - Loosely coupled
 - Independently deployable
 - Organized around business capabilities
 - Owned by a small team
The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications. It also enables an organization to evolve its technology stack."

Version 2:
In short, the microservice architectural style is an approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API. These services are built around business capabilities and independently deployable by fully automated deployment machinery. There is a bare minimum of centralized management of these services, which may be written in different programming languages and use different data storage technologies.
-- James Lewis and Martin Fowler (2014)

Version 3: 
"Micro-services are:  
      - Variant of SOA (Service Oriented Architecture)  
      - Structures application as a collection of loosely coupled services  
      - Services are fine-grained and protocols are lightweight  
      - Single DB per Micro-services (Recommended)  
      - Easy to develop, deploy, test and enables continous delivery  
      - It is divided on the basis of domains (Account, Cart..)

In summary MSA follows below principles:  

 - Scalability
 - Availability
 - Resiliency - the capacity to recover quickly from difficulties/failure (Highly dependent on modularity)
 - Independent, autonomous
 - Decentralized governance
 - Failure isolation
 - Auto-Provisioning
 - Continuous delivery through DevOps

## Building SaaS Micro-Services

In case you are planning to build a 'Software as a Service' (SaaS) application, You application must adhere to 12 factor apps that outlines and describes them in detail.  

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

**Reference:** https://12factor.net/

## Why

Polyglot programming is the practice of writing code in multiple languages to capture additional functionality and efficiency not available in a single language. The use of domain specific languages (DSLs) has become a standard practice for enterprise application development.


## How
Micro-services can be written in below three frameworks:  
 **A. Spring boot**  
 **B. Play-Framework(written in scala)**  
 **C. Grails**  
 
 **A. Spring boot**  
 Different dependencies solving similar problem  
 e.g. you can have service registry with the Eureka Server( in Netflix OSS) and same can be achieved with Zookeper and Consul.
 You have to determine based on the requirement which will fit your requirement better
  
 Eureka/Ribbon/Feign/Hystrix  
 Testing: JUnit  
 
 **B. Play Framework**  
 Java/Scala and Akka  
 Testing: JUnit, ScalaTest, FrisbyJS, Calabash Selenium  
 
 **C. Grails**


## Important points
 SOA VS Micro-services  
 Best Practices and naming conventions  
 Deployment  
 Principles of Micro-services (https://12factor.net/)
 
 
## REST API Documentation  
   **Swagger ( OpenAPI Specification ):** From January 1st 2016 the Swagger Specification has been donated to to the Open API Initiative (OAI) and has been renamed to the OpenAPI Specification. The Open API specification is backed by the likes of Google, Microsft and IBM.
   **RAML  (RESTful API Modeling Language)**    
   **API Blue Print**   
 
## Database:  
 NoSql(Mongo DB)  
 RDBMS(Oracle, SQL Server/Sybase)  
 
## CICD  
 GitHUb, Travis CI/ Jenkins, VSTS, JIRA   
 
## Data Infrastructure:  
 AWS Kinesis, Spark and AWS Redshift  
 
## UI:  
 React/Angular  

## Micro-services with Netflix OSS
![Microservices_Architecture](https://github.com/girirajvyas/resources/blob/main/Images/Microservices_Architecture.PNG)

## Micro-services Testing
 Consider you have Micro-Service Project that is dependent on the local DB for fetching data for few of the services whereas some services also calls other services to get the data.  
 
 **Local DB** - data can be inserted in embedded Mongo of @Before method so that the data is available when the tests are ran and can be validated.  
 **Other services** - Mock the response via WireMock and validate the tests  

 You can find the same demonstrated below. 
![Microservices_Test](https://github.com/girirajvyas/resources/blob/main/Images/Microservices_Testing.PNG)

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

## API Gateway Vs Service Mesh

![Microservices_vs Mesh](https://github.com/girirajvyas/resources/blob/main/Images/API_Gateway_Vs_Service_Mesh.PNG)
 

Micro-services fails because of below points:
10. 
9. The Monolith database
8. The event monolith 
7. 



Two types of micro-services architecture
https://dzone.com/articles/api-gateway-vs-service-mesh

1. Gateway based (in Spring cloud it is ZUUL)
   Netflix OSS (Netflix open source software)
     - ZUUL Gateway
     - Hystrix circuit breaker
     - Ribbon Load balancer
     - Eureka Service registry
     - 

2. Service mesh (useful when you have micro-services in multiple technologies)
   

## Architecture can be designed in below way

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
@Produces(value=MediaType.APPLICATION_JSON)
@Consumes(value=MediaType.APPLICATION_JSON)
@Path(“/”)
Public  interface DummyEP {
      @Post
     @Path(value = “/insert”)
     Response insertEmployee(InsertEmployeeRequest req);
}


@EnableZuulGateway

@EnableEurekaServer

https://dzone.com/articles/using-wiremock-to-test-against-3rd-party-services
Wiremock (com.github.tomakehurst)
Embed.mongo (de.flapdoodle.embed)


Strangler Application strategy.
Synchronicity
Independence
Resiliency --
Simplicity

Event sourcing
Choreography-based Saga instead of Orchestration-based
microservices architecture that makes use of remote procedure calls


                                                                       Zuul
             __________________________________________________________|____________________________________                                                                                                         
            |                                                                                                |
          Eureka                                                                                Same as left hand side        
            |
        Appserver (registered with spring boot app name in Eureka)
            |
Mongo                    httpsd - > tibco load balancer


## Scaling microservices

To scale microservices we can use scale cube reference.

Wiki: "The scale cube is a technology model that indicates three methods by which technology platforms may be scaled to meet increasing levels of demand upon the system in question."  

2 ways:
 - increase hardware capability
 - deploy multiple instances (redundancy), application should be modular is mandatory requirement

 - Improve modularity
 - Improve caching 
     - for inter service communication
     - caches within each service to reduce number of db calls
     - Distributed caching where first we check in distributed cache and then to db

For Scaling Database, you use Database Sharding i.e Z-axis
https://medium.com/@jeeyoungk/how-sharding-works-b4dec46b3f6

## Resilient Microservices

https://dzone.com/articles/libraries-for-microservices-development


## Performance

 - time to respond and load up for a user (ex. withing 2 secs)
 
How to improve:
 - Code level: Ensure java best practices
   - Ensure unnecessary objects are not created
   - Ensure correct data structure/algo is used according to the scenarios
 - Database(datastores):
   - db are tune for the type of queries
   - proper indexes, properly normalized
 - Caching
   - cache all the redundant data for static fields
   - distributed caching is required if you have scaled your application and there are 10 instances
 - Capacity
   - before redundancy see vertical scaling option by increasing CPUs
 - Redundancy
   - Build redundancy (horizaontal scaling), 
 - Modularity:
   - Make sure you app is modular so that it can be scaled

Best practices:
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

## Availability

measure of how often the system is providing the availability

Diff availability needs: 
 - internal application: low
 - available on internet: very high

 - multiple components are deployed and hence no single point of failure
 - reduced bottlenects like single monolith db or application

# Microservices Architectural Patterns

 - Decomposition Patterns
   - Decompose by business capability 
   - Decompose by subdomain
   - Strangler pattern
 - Integration Patterns
   - API Gateway pattern
   - Aggregator pattern
   - Client-Side UI composition pattern
 - Database Patterns
   - Database per service
   - Shared database per Service
   - Command Query Responsibility Saggregation
   - SAGA Pattern
 - Observer Patterns
   - Log Aggregation Pattern
   - Performance Metrics
   - Distributed tracing
   - Health check
 - Cross cutting concerns Patterns
   - External Configuration
   - Service Discovery pattern
   - Circuit breaker pattern
   - Blue green deployment



## References

 - https://martinfowler.com/articles/microservices.html
 - https://martinfowler.com/microservices/
 - https://en.wikipedia.org/wiki/Microservices
 - https://medium.com/hashmapinc/how-i-use-the-twelve-factor-app-methodology-for-building-saas-applications-with-java-scala-4cdb668cc908
 - https://medium.com/microservices-in-practice/microservices-in-practice-7a3e85b6624c
 - https://dzone.com/articles/design-patterns-for-microservices
 - CAP Theorem: https://robertgreiner.com/cap-theorem-revisited/
 - Scale cube: https://microservices.io/articles/scalecube.html
 - Sharding: https://medium.com/@jeeyoungk/how-sharding-works-b4dec46b3f6
 - Best: https://medium.com/@madhukaudantha/microservice-architecture-and-design-patterns-for-microservices-e0e5013fd58a

NFR: https://www.youtube.com/watch?v=R3j0Z1c-0qY&list=PLBBog2r6uMCTB4bYedn-WMW2MoYWk_sgf&index=19
 https://www.springboottutorial.com/availability-non-functional-requirement-in-microservices
 
Best practices: https://github.com/in28minutes/java-best-practices#should-i-be-an-expert-at-all-design-patterns
http://progressivecoder.com/spring-cloud-microservices-a-detailed-guide/
https://www.clariontech.com/blog/5-best-technologies-to-build-microservices-architecture
https://dzone.com/articles/3-popular-frameworks-to-build-microservices?fromrel=true
https://medium.com/microservices-architecture/top-10-microservices-framework-for-2020-eefb5e66d1a2#:~:text=Spring%20Boot%20is%20popular%20Java%20framework%20for%20writing%20Microservices.&text=Spring%20Boot%20allow%20large%20scale,well%20as%20large%20scale%20system.
https://medium.com/hashmapinc/how-i-use-the-twelve-factor-app-methodology-for-building-saas-applications-with-java-scala-4cdb668cc908
https://dzone.com/articles/design-patterns-for-microservices
https://www.edureka.co/blog/microservices-design-patterns#Chained



