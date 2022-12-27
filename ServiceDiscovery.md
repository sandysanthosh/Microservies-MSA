

##### Services in Monolithic:

client 1 -> Load Balancer -> Service 1

client 2 -> Load Balancer -> Service 2

##### Service Discovery:
```
HOST 
PORT
URI
```

##### services in Microservices:

##### Load Balancer/Cache

##### Service Discovery App:

Client1 -  Service Discovery app - App1


Home Microservice- port: 8081
Product Microservice- port: 8082

```
@RestController 
public class productController{
@GetMapping("/products")
public String products(){
return "Products";
}
}
```

##### HomeConfig Class:

##### Rest Template:

```
@Configuration
public class HomeConfig{

@Autowired
private RestTemplate resttemplate;

@GetMapping("/home")
public String home()
{
String products = restTemplate.getForObject("http://localhost:8082/products", String.class);
return products;
}
}
```
##### Eureka Service Starter:

##### Dependency:
```
Eureka Server
Spring Web
```
##### Main class:
```
@EnableEurekaServer
public static void main()
{
SpringApplication.run(SpringbootserviceDiscovery.class,args);
}
}
```
##### app.properties:
```
server.port = 8761
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
```

##### spring cloud starter netflix eureka client:


##### add in pom.xml
	```
spring.application.name=HOME-microservices

spring.application.name=PRODUCTS-microservices
```

localhost:8761:
```
##### instance currently registered

String products = restTemplate.getForObject("http://PRODUCTS-microservices/products", String.class);
return products;
```

##### SPRING CLOUD:

```
@Bean
@LoadBalanced
```













