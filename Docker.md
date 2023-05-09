# Docker

## Docker setup
- Go to https://www.docker.com/products/developer-tools
- You have 3 choices now
    - Docker Desktop: This is for building and deploying locally
    - Docker Hub: Cloud-based application registry and development team collaboration services.
        - hub.docker.com -> Signup -> and now you can publish your images here
    - Docker play: In case you want to just learn without installation, follow https://www.docker.com/play-with-docker

## Dockerfile
- **Dockerfile:** default file name that `docker build` command will look for while creating an image.
  - Note that `f` is lower case in `Dockerfile`
- You will write here, how exactly your image will be built
- References: https://docs.docker.com/engine/reference/builder/

### Java project with main class example

```cmd
# pull JDK 8 from DockerHub
FROM openjdk:8

# Copy current code in Docker directory
COPY . /usr/jpop-docker-example 

# Select the working directory
WORKDIR /usr/jpop-docker-example/src

# Compile the main class
RUN javac com/epam/jpop/helloworld/Main.java 

# Execute command
CMD ["java","com.epam.jpop.helloworld.Main"]
```

### Java Spring boot project example

```cmd
# pull JDK 8 from DockerHub
FROM openjdk:8

# Expose Port
EXPOSE 9091

# Select the working directory
WORKDIR /usr/wallet/

# Copy current code in Docker directory
ADD ./target/wallet-0.0.1-SNAPSHOT.jar wallet-0.0.1-SNAPSHOT.jar 

# Execute command
CMD ["java","-jar","wallet-0.0.1-SNAPSHOT.jar"]

```

**Spring boot**  
- If you have set `server.port: 8080`, it means that spring boot application starts the web server that is ready to get accept connections on that port.
- If you want to change that mapping externally without modifying the application.yaml you can do that by passing the additional parameter:
	- `java -jar wallet-0.0.1-SNAPSHOT.jar --server.port=8081`
- This will effectively override the definition in yaml. 
- There are other ways as well (environment variable for example). Spring boot supports many different ways of configurations and there are ways that take precedence over the configuration specified in yaml. Among them SERVER_PORT environment variable is one exmaple.
- Ref: https://docs.spring.io/spring-boot/docs/2.1.9.RELEASE/reference/html/boot-features-external-config.html

**Docker**
- When we run the container with `-p A:B`, This means that it will forward the port A in the host machine to port B inside the container.
- To set/pass environment variable while running docker pass -e switch:
	- `docker run -d -e SERVER_PORT=8081 -p 8081:8081 -it wallet`


## Create Image 
- Command: `docker build -t jpop-docker-example .` (. resembles current directory)  
- Command: `docker build -t jpop-docker-example -f MyDockerfile .` (-f commit in case file name is different from the default name)  

## Publish to Docker Hub
- docker login  
- docker build -t girirajvyas/jpop-docker-example . (repo name has to appended while building, by default latest tag)  
- docker build -t girirajvyas/jpop-docker-example:v1 . (with tag name)  
- docker tag girirajvyas/jpop-docker-example:v1 girirajvyas/jpop-docker-example:v2 (copies image with new tag)  
- docker push girirajvyas/jpop-docker-example  
- docker pull girirajvyas/jpop-docker-example  
- docker image rm girirajvyas/jpop-docker-example (remove image)


## Commands:  
- docker -v  
- docker version  
- docker info  
- docker help  
- docker container ls -all  
- docker ps (Only running containers)  
- docker ps -a (shows even the stopped containers)  

## Ubuntu  
- docker image pull ubuntu  
- docker image ls  
- docker container run ubuntu : To simply run  
- docker container run -it ubuntu: to run and get inside the container  

## Tomcat  
docker run tomcat:9  
docker run -p 9090:8080 tomcat:9 - run tomcat 9 version on 8080 port in container and map that port to 9090 of local machine  

## Install MySQL  
docker pull mysql  
docker run -p 3306:3306 --name mysqldb -e MYSQL_ROOT_PASSWORD=root -e MSQL_DATABASE=users -d mysql:latest  
docker logs mysqldb (name that you used above)  
docker logs mysqldb -f (continous logs)  

## Create Network  
docker network create --driver bridge micro-service-network  
--network micro-service-network (pass this parameter while starting containers to be on the same network)  
  
docker run -p 3306:3306 --name mysqldb -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=users -d mysql:latest --network micro-service-network

## Must if you are new to docker
Docker Desktop is a native application that delivers all of the Docker tools to your Mac or Windows Computer.  

- Open Docker Desktop. (Download here if you don't have it).  
- Type the following command in your terminal: `docker run -dp 80:80 docker/getting-started`
- Open your browser
- you can do this without downloading docker as well, follow https://www.docker.com/101-tutorial

## Spring boot app on Docker

### Create Dockerfile
- To create a Docker image, we fist need to build our project as the built jar will be deployed as an image on dockerhub
- Please refer the DockerFile below:
```
FROM  - Must be the first non-comment instruction in the Dockerfile. This command creates a layer from the Docker image. In our case, we have used  java:8 which means this application will run on Java 8.
EXPOSE - Exposing the port for the endpoint. In this example, we have configured 8080.
ADD - This command helps to take a source and destination. Normally, the source is your local copy. The COPY command also does same thing, but there is a small difference between the COPY and ADD  commands.
ENTRYPOINT - It's similar to CMD, where our command/jar file will be executed.
```

### Genrate image from the Dockerfile
```unix
PS D:\Sources\Jpop\jpop-service-registry> docker build -t jpop-service-registry-0.0.1 .
Sending build context to Docker daemon  44.05MB
Step 1/4 : FROM openjdk:8
 ---> 5684f3366a1f
Step 2/4 : EXPOSE 8761:8761
 ---> Running in 0b40e6b9a628
Removing intermediate container 0b40e6b9a628
 ---> 257ed26121a4
Step 3/4 : ADD /target/jpop-service-registry-0.0.1-SNAPSHOT.jar jpop-service-registry-0.0.1-SNAPSHOT.jar
 ---> 9d1fa2d44ada
Step 4/4 : ENTRYPOINT ["java", "-jar", "jpop-service-registry-0.0.1-SNAPSHOT.jar" ]
 ---> Running in 8fda8f55d5df
Removing intermediate container 8fda8f55d5df
 ---> 999c15ad835e
Successfully built 999c15ad835e
Successfully tagged jpop-service-registry-0.0.1:latest
SECURITY WARNING: You are building a Docker image from Windows against a non-Windows Docker host. All files and directories added to build context will have '-rwxr-xr-x' permissions. It is recommended to double check and reset permissions for sensitive files and directories.
PS D:\Sources\Jpop\jpop-service-registry>
```

### Run created image
docker run -p 8761:8761 -t jpop-service-registry-0.0.1

### Publish to Docker Hub
- docker tag jpop-service-registry-0.0.1:latest girirajvyas/jpop-service-registry-0.0.1:latest (copies image with new tag)  

## Check logs
 - docker logs --follow <Container ID> (continously tail logs)
 - docker logs --tail 100 <Container ID> (last 100 lines)
 - For other: https://docs.docker.com/engine/reference/commandline/logs/
 


# References
- https://stackoverflow.com/questions/18093928/what-does-could-not-find-or-load-main-class-mean
- https://medium.com/@hudsonmendes/docker-spring-boot-choosing-the-base-image-for-java-8-9-microservices-on-linux-and-windows-c459ec0c238
- https://stackoverflow.com/questions/54954187/docker-images-types-slim-vs-slim-stretch-vs-stretch-vs-alpine
- [docker in 1 hour](https://www.youtube.com/watch?v=pTFZFxd4hOI)



https://docs.docker.com/engine/reference/builder/#parser-directives
https://hub.docker.com/repositories/giririajvyas