# myMicroservicesApp
A microservice package that manages a simple application for movie ratings

## The project is based on :

* Java 1.8
* Spring Boot
* Maven

----

In this package there are four microservices containt:

* `discovery-server`	
* `movie-catalog-service`	
* `movie-info-service`	
* `ratings-data-service`

Each directory is a seperate spring-boot application that communicates with the others in order to collect information. Since the main goal of this app is to learn the basic idea of creating microservices applications all the the data that are being exchanged are just hart coded into the classes. 

The main service is the movie-catalog-service which collects movie information from the movie-info-service and the ratings from the rating-data-service.

Discovery-server acts as the connection between the services using Eureka server. So each one microservice registeres at eureka server and then by every request eureka server provides the connection so that `movie-catalog-service`	locates the appropriate microservice.
