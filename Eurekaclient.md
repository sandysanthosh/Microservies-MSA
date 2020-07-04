### POM.xml:

```   <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-config</artifactId>
        </dependency>
        
        <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.springframework.cloud</groupId>
                <artifactId>spring-cloud-starter-parent</artifactId>
                <version>Greenwich.RELEASE</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>
 ```
  
  ### Enable @EnableEurekaClient:

    ```
        @SpringBootApplication
        @EnableEurekaClient
         public class DogMicroserviceApplication {
               public static void main(String[] args) {
              SpringApplication.run(DogMicroserviceApplication.class, args);
              }
            }
     ``` 
 
 ### Application.properties:

```
  spring.application.name=dog-service
  server.port=8762
  eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka/
  eureka.client.service-url.default-zone=http://localhost:8761/eureka/
  eureka.instance.prefer-ip-address=true
```
        
