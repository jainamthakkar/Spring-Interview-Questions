# Spring-Interview-Questions

### 1. Explain the term ‘Spring Boot’
**Answer**:
Spring Boot is a Spring module that offers Rapid Application Development (RAD) for the Spring framework. It simplifies the process of creating a Spring-based application by reducing the need to configure multiple Spring files. Spring Boot provides the following features to streamline application development:

- **Auto-Configuration**: Automatically configures your Spring application based on the dependencies you include, minimizing the need for manual configuration.
- **Starter POMs**: Pre-configured Maven or Gradle dependencies that bring in the necessary libraries for your project, such as `spring-boot-starter-web` for web applications.
- **Embedded Servers**: Includes embedded servers like Tomcat, Jetty, or Undertow, allowing you to run your application without needing an external server.
- **Production-Ready Features**: Built-in features like health checks, metrics, and externalized configuration to help get your application production-ready quickly.
- **Command Line Interface (CLI)**: A CLI tool for quickly prototyping and running Spring applications using Groovy scripts.

### 2. Spring boot is used to develop stand alone application. what does it means?
**Answer**:
A stand-alone application is a software program that works on its own, without requiring an internet connection or any server access. It is not bundled with other independent software features, and it installs directly on the user's system.

### 3.  What is RAD model?
**Answer**:
RAD or Rapid Application Development process is an adoption of the waterfall model; it targets
developing software in a short period. RAD follow the iterative
SDLC(Software development life cycle) RAD model has the following phases:
- Business Modeling
- Data Modeling
- Process Modeling
- Application Generation
- Testing and Turnover

(or we can remember CPMCD { Communication, Planning, Modeling, Construction, Deployment })

### 4. What are the commands to run and stop Spring Boot executable jar file?
**Answer:**
You need to open cmd or shell window command and use

`java -jar`

Example:

`$ java -jar myproject-0.0.1-SNAPSHOT.jar`

To stop use `ctrl+C`

### 5. How can you change JDK version in Spring Boot?
**Answer:**
`<properties>
    <java.version>17</java.version>
</properties>`

### 6. What is the process that you need to follow to run Spring Boot application on the custom port?
**Answer:**
In order to run a Spring Boot application, you require to put server.port properties in application.properties. For example, `server.port=8050`

### 7. What is Spring Boot starter? How is it useful?
**Answer:**
Spring Boot has many starters. They are a set of convenient dependency descriptors. Starter allows you to include these descriptors in your pom.xml.

For example, If you want to work with Spring MVC, you can include `spring–boot–starter–web` as a dependency in pom.xml.

Also we have `spring–boot–starter–security`.

### 8. Can you use Spring Boot with applications which are not using Spring?
**Answer:**
No, it is not possible as Spring Boot is limited to Spring application only.

### 9. What is the name of the configuration file which you can use in Spring Boot?
**Answer:**
The configuration file used in Spring Boot projects is called application.properties. It is an important file which allows you to override your default configurations.

### 10. What is DevTools in Spring Boot?
**Answer:**
Spring Boot DevTools helps you to increase the productivity of the developer. So, you don't require to redeploy your application every time you make the changes. It allows the developer to
reload changes without the need of restarting of the server.

### 11. What are the essential components of Spring Boot?
**Answer:**
The important components of Spring Boot are:
- Spring Boot Starter
- Spring Boot auto-configuration
- Spring Boot Actuator
- Spring Boot CLI

### 12. How to enable HTTP/2 supports in Spring Boot?
**Answer:**
User can enable HTTP/2 support by using
server.http2.enabled configuration property.

### 13. What is a Spring Boot Actuator?
**Answer:**
Spring Boot Actuator is a module that provides production-ready features to monitor and manage your Spring Boot application. It offers various endpoints and metrics that can be used for monitoring, health checks, auditing, and managing your application.

### 14. How can you access a value defined in the application? What is properties file in Spring Boot?
**Answer:**
Use the @Value annotation to access the properties which is defined in the application - properties file.

```
@Value("${custom.value}")
private String customVal;
```
### 15. What is the primary difference between Spring and Spring Boot?
Spring is a web application development framework based on Java. On the other hand Spring Boot is an extension of the spring framework which eliminated the boilerplate configuration
required for setup a Spring application.

### 16.  Explain Spring Boot Admin.
**Answer:**
Spring Boot Admin is a web application, used for managing and monitoring Spring Boot applications. Each application is considered as a client and registers to the admin server. Behind the scenes, the magic is given by the Spring Boot Actuator endpoints.

### 17.  How can you connect Spring Boot to the database using JPA?
**Answer:**
To connect Spring Boot to the database using JPA, follow these steps:

1. Define the database connection properties in the application.properties file.
2. Create JPA entity classes annotated with @Entity.
3. Use Spring Data JPA repositories or @Repository interfaces to perform database operations.

### 18. Explain @RestController annotation in Spring Boot?
**Answer:**
Spring 4.0 introduced the @RestController annotation in order to simplify the creation of RESTful web services. It's a convenient annotation that combines @Controller and @ResponseBody, which eliminates the need to annotate every request handling method of the controller class with the @ResponseBody annotation.

### 19. What is the use of response body in Spring Boot?
**Answer:**
The @ResponseBody annotation tells a controller that the object returned is automatically serialized into JSON and passed back into the HttpResponse object. In the developer console of our browser or using a tool like Postman, we can see the following response: {"text":"Thanks For Posting!!!"}

### 20. What is the difference between @RequestBody and @ResponseBody?
**Answer:**
As the name suggest @RequestBody annotation is used to parse the incoming HTTP request while @ResponseBody annotation is used to convert your object into HTTP response in the form client is expecting like JSON, XML, or simply text.