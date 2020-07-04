
#### Eureka Module:

   The case study is an online ordering service. There are multiple services that work together to create the system.

            Item Service
            Order Service
            Shipping Service

   Eureka Registry accessible via http://localhost:8761

#### Items Microservices Module

```
  CRUD Repository - ItemRepository.java
  Domain Entity/Model -Item.java
  H2 Database accessible via http://localhost:8080/h2/
  Tomcat Server accessible via http://localhost:8080
  Items Microservice accessible via http://localhost:8080/items
  ```
  
 
  #### You may need this additional dependency in your POM file for the Eureka server to load:
  
  #### pom.xml:
  
     <dependency>
       <groupId>javax.xml.bind</groupId>
       <artifactId>jaxb-api</artifactId>
       <version>2.4.0-b180725.0427</version>
   </dependency>
   
