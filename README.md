# Microservies-MSA

###  Springboot with Microservies 

#### N-Tier and monolithic applications used to be the de facto standard. In one single binary web artifact, like an EAR or WAR file, there would be a layered architecture with the decomposition of code into more functional components.

* Presentation Layer

* Business Process Layer/Service Layer

* Data Access Layer

#### There are several disadvantages to the n-tier monolithic application architecture:

* Tight coupling of code which makes changes hard.

* A single deployment with multiple layers that causes long testing, building, and deployment cycles.

* A big monolithic application that makes code reuse and sharing of components difficult.

* The Microservices Architecture (MSA) decomposes systems into discrete, individual, standalone components that can communicate amongst themselves, working together or with external systems.


** MSA is a more agile framework that fits well with the cloud-based world and lends itself well to web application development and web service development.**

#### MSA Features:

* MSA is very flexible because it supports any language that can communicate via a RESTful endpoint and leverages REST over HTTP.

* MSA offers agility and systems that are easier to write, test, deploy, and share.

* MSA provides systems that can better scale to load and demand.


* MSA provides systems that are resilient because failures are isolated and don’t cascade through the infrastructure.

#### Eureka:

* Eureka, created by Netflix, is responsible for the registration and discovery microservices. Spring has incorporated Eureka into Spring Cloud, making it even easier to stand up a Eureka server.

* Eureka consists of a server and a client-side component. The server component will be the registry in which all the microservices register their availability. The microservices use the Eureka client to register; once the registration is complete, it notifies the server of its existence.


#### What make a microservice different from a normal RESTful service?

      A microservice must register itself with a discovery service
      
 #### Eureka server to load:
 
#### pom.xml:

* spring cloud starter config
*  spring  cloud netfli eureka server

      <dependency>
          <groupId>javax.xml.bind</groupId>
          <artifactId>jaxb-api</artifactId>
          <version>2.4.0-b180725.0427</version>
      </dependency>
    
#### application.properties:

```
spring.appliation.name=eurela-server
server.port=8761

#dont register itself as client

eureka.client.regiser-with-eureka = false
eureka.client.fetch-registry= false
logging.level.com.netflix.eureka=ON
logging.level.com.netflix.discovery = ON
```


##### Starter:

      @SpringBootApplication
      @EnableEurekaServer

##### login:

      https://localhost:8761

##### Eureka dashboard:

* system status
* current time -> uptime 
* general Info -> total memory, enviroment, cpus
* DS replicas

*** instane currently registered with Eureka

##### Spring Data REST makes it easy to expose microservices. 
##### Spring Data REST builds on top of Spring Data repositories and automatically exports those as REST resources.

#### So how does Spring Data Rest work?

* At application startup, Spring Data Rest finds all of the spring data repositories

* Then, Spring Data Rest creates an endpoint that matches the entity name

* Next, Spring Data Rest appends an S to the entity name in the endpoint

* Lastly, Spring Data Rest exposes CRUD (Create, Read, Update, and Delete) operations as RESTful APIs over HTTP

* There is no need to create a controller or service layer!

<a href="https://github.com/sandysanthosh/Microservies-MSA/blob/master/Items.md">Item Service</a>

<a href="https://github.com/sandysanthosh/Microservies-MSA/blob/master/Eurekaclient.md">Eureka client</a>
 
#### pom.xml:

* spring data

* JPA Item Repository

* Spring DATA REST

* For a @SpringBootApplication to be discovery-aware, all that's needed is the Spring Discovery Client (i.e., spring-cloud-starter-netflix-eureka-client dependency) in the classpath. 
* The next step is to annotate the main Spring application class with the @EnableEurekaClient annotation.
* @EnableEurekaClient is optional if the spring-cloud-starter-netflix-eureka-client dependency is on the classpath.


#### Topics:

```

* Kafka - <a href="https://github.com/sandysanthosh/Apache-Kafka"> Kafka </a>

* Devops - <a href="https://github.com/sandysanthosh/Devops"> [Devops](https://github.com/sandysanthosh/Devops) </a> 

* Gitlab - <a href="https://github.com/sandysanthosh/GitLab"> [Devops](https://github.com/sandysanthosh/GitLab) </a> https://github.com/sandysanthosh/GitLab

* Openshift red- <a href="https://github.com/sandysanthosh/OpenShift"> [Openshift](https://github.com/sandysanthosh/Openshift) </a> 

```

```


Microservices Spring Boot Guide


santhosh kumar
Microservices spring boot checklist 

Here's a checklist for developing microservices using Spring Boot:

Define Service Boundaries: Determine the scope of each service and identify their responsibilities.

Choose an appropriate data storage solution: Decide whether to use a relational database, NoSQL database, or a combination of both.

Implement Service Discovery: Decide on a service discovery mechanism, such as Netflix Eureka or Consul.

Use a Build Tool: Choose a build tool such as Maven or Gradle for building and packaging the application.

Define RESTful APIs: Design and implement RESTful APIs for communication between services.

Use a Configuration Management Tool: Decide on a configuration management tool, such as Spring Cloud Config, to manage configuration properties across all services.

Enable Load Balancing: Implement load balancing, either by using a reverse proxy, such as Nginx, or a service discovery tool.

Add Security: Implement security measures such as authentication, authorization, and encryption to secure communication between services.

Use a Monitoring Tool: Choose a monitoring tool, such as Spring Boot Actuator, to monitor the health and performance of the services.

Implement Resilience: Implement features such as circuit breakers, retries, and timeouts to make services more resilient.

Automate Deployments: Automate the deployment of services using continuous integration and continuous deployment (CI/CD) tools.

Use Logging: Implement logging to monitor and troubleshoot issues in the services.


```




