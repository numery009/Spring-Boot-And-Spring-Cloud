# Spring-Boot-And-Spring-Cloud

Design microservice with Spring Boot and Spring Cloud----

1) Spring Cloud Config Server and Bus.
2) Load Balancing with Ribbon and Feign.
3) Implementing Naming Server with Eureka.
4) Distibuted Tracing with Zipkin.
5) Fault Tolerance with Hystrix.


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
</table>


Customer Service - Direct Call
http://localhost:8080/api/customer, http://localhost:8081/api/customer
Customer Account Service
http://localhost:8100/api/v1/customer
Customer Account Service – Feign
http://localhost:8100/api/v1/customer-feign
Eureka
http://localhost:8761/
Zuul – Customer Account Service
http://localhost:8765/customer-account-mysql/api/v1/customer-feign
Zuul – Customer Service
http://localhost:8765/customer-service-mysql/api/customer
Zipkin
http://localhost:9411/zipkin/
Spring Cloud Bus Refresh
http://localhost:8080/bus/refresh






# Zipkin Installation
Quick Start Page- 
   https://zipkin.io/pages/quickstart

Downloading Zipkin Jar-
  https://search.maven.org/remote_content?g=io.zipkin.java&a=zipkin-server&v=LATEST&c=exec

Command to run - 
RABBIT_URI=amqp://localhost java -jar zipkin-server-2.5.2-exec.jar

# VM Argument
-Dserver.port=8081





