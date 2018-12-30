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
         Zuul – Customer Account Service
      </td>      
      <td>
         http://localhost:8765/customer-account-mysql/api/v1/customer-feign
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





