# Spring-Boot-And-Spring-Cloud

Design microservice with Spring Boot and Spring Cloud----

1) Spring Cloud Config Server and Bus.
2) Load Balancing with Ribbon and Feign.
3) Implementing Naming Server with Eureka.
4) Distibuted Tracing with Zipkin.
5) Fault Tolerance with Hystrix.


a) Spring Cloud Config Server: Centralized external configuration management backed by a git repository. The configuration resources map directly to Spring Environment but could be used by non-Spring applications if desired.

b) Spring Cloud Bus: An event bus for linking services and service instances together with distributed messaging. Useful for propagating state changes across a cluster (e.g. config change events).

c) Spring Cloud OpenFeign: Spring Cloud OpenFeign provides integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment and other Spring programming model idioms.

d )Spring Cloud Netflix: Integration with various Netflix OSS components (Eureka, Hystrix, Zuul, Archaius, etc.)
         i) Eureka: This is a Naming Server. All microservices will be registered on Eureka server.
        ii) Zuul : This is an API Gateway. It uses for Security, Rate Limits, Fault Tolerance, Service Aggregation.

e) Spring Cloud Sleuth: Distributed tracing for Spring Cloud applications, compatible with Zipkin, HTrace and log-based (e.g. ELK) tracing.

f) Spring Cloud Security: Provides support for load-balanced OAuth2 rest client and authentication header relays in a Zuul proxy.




# Ports

<table>
   <tr>
      <td>
         Application
      </td>      
      <td>
         Ports
      </td>
   </tr>    
   <tr>
      <td>
         Spring Cloud Config Server
      </td>      
      <td>
         8888
      </td>
   </tr> 

   <tr>
      <td>
         Customer Service
      </td>      
      <td>
         8080, 8081, ..
      </td>
   </tr> 
   <tr>
      <td>
         Customer Account Service
      </td>      
      <td>
         8100, ...
      </td>
   </tr> 
   <tr>
      <td>
         Netflix Eureka Naming Server
      </td>      
      <td>
         8761
      </td>
   </tr> 
   <tr>
      <td>
         Netflix Zuul API Gateway Server
      </td>      
      <td>
         8765
      </td>
   </tr> 
   <tr>
      <td>
         Zipkin Distributed Tracing Server
      </td>      
      <td>
         9411
      </td>
   </tr>    
<table>


# URLs

<table>
   <tr>
      <td>
         Application
      </td>      
      <td>
         URL
      </td>
   </tr>   
   <tr>
      <td>
         Spring Cloud Config Server
      </td>      
      <td>         
http://localhost:8888/customer-service-mysql/dev,
http://localhost:8888/customer-service-mysql/test,
http://localhost:8888/customer-service-mysql/stage,
http://localhost:8888/customer-service-mysql/prod
      </td>
   </tr>   
   <tr>
      <td>
         Customer Service - Direct Call
      </td>      
      <td>
         http://localhost:8080/api/customer, http://localhost:8081/api/customer
      </td>
   </tr>
    <tr>
      <td>
         Customer Account Service
      </td>      
      <td>
         http://localhost:8100/api/v1/customer
      </td>
   </tr>   
    <tr>
      <td>
         Customer Account Service – Feign
      </td>      
      <td>
         http://localhost:8100/api/v1/customer-feign
      </td>
   </tr>   
    <tr>
      <td>
         Eureka
      </td>      
      <td>
         http://localhost:8761/
      </td>
   </tr>   
   <tr>
      <td>
         Zuul – Customer Account Service Feign
      </td>      
      <td>
         http://localhost:8765/customer-account-mysql/api/v1/customer-feign
      </td>
   </tr>  
   
   <tr>
      <td>
         Zuul – Customer Account Service 
      </td>      
      <td>
         http://localhost:8765/customer-account-mysql/api/v1/customer
      </td>
   </tr>  
   <tr>
      <td>
         Zuul – Customer Service
      </td>      
      <td>
         http://localhost:8765/customer-service-mysql/api/customer
      </td>
   </tr>   
   <tr>
      <td>
         Zipkin
      </td>      
      <td>
         http://localhost:9411/zipkin/
      </td>
   </tr>   
   <tr>
      <td>
         Spring Cloud Bus Refresh
      </td>      
      <td>
         http://localhost:8080/bus/refresh
      </td>
   </tr>   
</table>




# Zipkin Installation
Quick Start Page- 
   https://zipkin.io/pages/quickstart

Downloading Zipkin Jar-
  https://search.maven.org/remote_content?g=io.zipkin.java&a=zipkin-server&v=LATEST&c=exec

Command to run - 
RABBIT_URI=amqp://localhost java -jar zipkin-server-2.5.2-exec.jar

# VM Argument
-Dserver.port=8081





