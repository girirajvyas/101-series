## Micro-services
   "Micro-services are:  
      - Variant of SOA (Service Oriented Architecture)  
      - Structures application as a collection of loosely coupled services  
      - Services are fine-grained and protocols are lightweight  
      - Single DB per Micro-services (Recommended)  
      - Easy to develop, deploy, test and enables continous delivery  
      - It is divided on the basis of domains (Account, Cart..)
	  									                      
## Principles of Micro-services (https://12factor.net/)

## Why

## How
Micro-services can be written in below three frameworks:  
 **A. Spring boot  
 B. Play-Framework(written in scala)  
 C. Grails**  
 
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
   

Architecture can be designed in below way
1. msparentpom
   Common dependencies across all micro-services created **on the same platform**
   update dependencies at one place and it will be available everywhere   
   
2. CCCLib

3. MSLib

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
