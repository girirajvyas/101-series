# Maven  
 - Installation  
 - Repositories  
 - Lifecycle  

Why Maven  
Easy Build  
Dependency management  
one liner commands  
 
## Installation    
JAVA_HOME  
M2_HOME (after maven 2) and MAVEN_HOME (before maven 2)  

## Create new project  
- select architecture type of your project, you will have a list of archetype select any 1 from the list:  
   ```mvn archetype: generate```  
- details:  
  groupId: same as package  
  artifactId: unique name of project  
  version: version of project (during dev it is snapshot)     
  package: reverse dns  

## Repositories  
Local  (.M2 folder)
Maven Repository (https://mvnrepository.com/repos)  
Custom configured  (e.g: Nexus, archiva)


## Build Lifecycles
a. verify: verify pom.xml if the Jars are there in repository
b. compile:  
c. test:  
d. package:  
e. verify:  
f. install:   
g. deploy:  

Note: any of the phase called from above list will first execute all the steps specified above it.   
mvn clean install -Dmaven.test.skip=true  

## Dependency Scopes
a. compile
b. provided
c. runtime
d. test
e. system
f. import



## Plugins



References:
https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html