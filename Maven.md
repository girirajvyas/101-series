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

## text
Your convention seems to be reasonable. If I were searching for your framework in the Maven repo, I would look for awesome-inhouse-framework-x.y.jar in com.mycompany.awesomeinhouseframework group directory. And I would find it there according to your convention.
Two simple rules work for me:
a.reverse-domain-packages for groupId (since such are quite unique) with all the constrains regarding java packages names
b.project name as artifactId (keeping in mind that it should be jar-name friendly)

GROUPID will identify your project uniquely across all projects, so we need to enforce a naming schema. It has to follow the package name rules, what means that has to be at least as a domain name you control, and you can create as many subgroups as you want. Look at More information about package names.
eg. org.apache.maven, org.apache.commons

A good way to determine the granularity of the groupId is to use the project structure. That is, if the current project is a multiple module project, it should append a new identifier to the parent's groupId.
eg. org.apache.maven, org.apache.maven.plugins,  org.apache.maven.reporting

ARTIFACTID is the name of the jar without version. If you created it then you can choose whatever name you want with lowercase letters and no strange symbols. If it's a third party jar you have to take the name of the jar as it's distributed.
eg. maven, commons-math

VERSION if you distribute it then you can choose any typical version with numbers and dots (1.0, 1.1, 1.0.1, ...). Don't use dates as they are usually associated with SNAPSHOT (nightly) builds. If it's a third party artifact, you have to use their version number whatever it is, and as strange as it can look.
eg. 2.0, 2.0.1, 1.3.1

Error:
Could not resolve archetype org.appfuse.archetypes:appfuse-modular-spring:RELEASE from any of the configured repositories.
Could not resolve artifact org.appfuse.archetypes:appfuse-modular-spring:pom:RELEASE
Failed to resolve version for org.appfuse.archetypes:appfuse-modular-spring:pom:RELEASE: Could not find metadata org.appfuse.archetypes:appfuse-modular-spring/maven-metadata.xml in local (C:\Users\giri\.m2\repository)
Failed to resolve version for org.appfuse.archetypes:appfuse-modular-spring:pom:RELEASE: Could not find metadata org.appfuse.archetypes:appfuse-modular-spring/maven-metadata.xml in local (C:\Users\giri\.m2\repository)

5. In the "Remote Archetype Catalog" dialogBox, specify the catalog url and description, by entering "https://oss.sonatype.org/content/repositories/appfuse/archetype-catalog.xml" for the Catalog File, and an appropriate description (e.g Remote catalog of AppFuse archetypes).

# Refernces

 - [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)