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
**Answer:**
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

### 19. What is the use of @ResponseBody in Spring Boot?
**Answer:**
The @ResponseBody annotation tells a controller that the object returned is automatically serialized into JSON and passed back into the HttpResponse object. In the developer console of our browser or using a tool like Postman, we can see the following response: {"text":"Thanks For Posting!!!"}

### 20. What is the difference between @RequestBody and @ResponseBody?
**Answer:**
As the name suggest @RequestBody annotation is used to parse the incoming HTTP request while @ResponseBody annotation is used to convert your object into HTTP response in the form client is expecting like JSON, XML, or simply text.

### 21. Explain Spring CLI.
**Answer:**
The Spring Boot CLI is a command line tool that you can use to bootstrap a new project from start.spring.io or encode a password.

Spring Boot CLI(Command Line Interface) is a Spring Boot software to run and test Spring Boot applications from command prompt. When we run Spring Boot applications using CLI, then it internally uses Spring Boot Starter and Spring Boot AutoConfigurate components to resolve all dependencies and execute the application.

### 22. What are embedded containers support by Spring?
**Answer:**
Spring Boot support the main three embedded containers:
1) Tomcat
2) Jetty
3) Undertow.

By default, it uses Tomcat as an embedded container.

### 23. Explain thymeleaf in Spring Boot.
**Answer:**
Thymelaf is a server-side Java template engine for a web application. It helps you to bring elegant natural templates to your web application.

### 24. What is the main difference between JPA and Hibernate?
**Answer:**
JPA is responsible for managing relational databases in Java applications. Hibernate is an ORM tool used for saving the state of the Java object in the database.


### 25. What is a shutdown in the actuator?
**Answer:**
A shutdown is an endpoint that helps application to be shut down properly. This feature is not enabled by default.

However, you can use it by setting command: management.endpoint.shutdown.enabled=true in your application.properties file.

### 26. Is it possible to replace or override the Embedded Tomcat server in Spring Boot?
**Answer:**
Yes, it is possible to replace the Embedded Tomcat with any other servers by using the starter dependencies. For that, you can use `spring-boot-starter-jetty` or as a dependency for according
you to your need.

### 27. Can you disable the default web server in the Spring Boot application?
**Answer:**
The default web server in a Spring Boot application can be disabled by setting the 'spring. main. web-application-type' property to 'none' in the application. properties file.

### 28. How do you Add, Filter to an application? 
**Answer:**
A filter is an object used to intercept the HTTP requests and responses of your application. By using filter, we can perform two operations at two instances − Before sending the request to the controller. Before sending a response to the client.

There are three methods to add filter to Spring
Boot application:
- By implementing Filter interface.
- Using FilterRegistrationBean.
- Using MVC controller.

### 29. What is @PathVariable?
**Answer:**
The @PathVariable annotation is used to extract the value from the URI. It is most suitable for the RESTful web service where the URL contains some value. Spring MVC allows us to use multiple @PathVariable annotations in the same method. A path variable is a critical part of creating rest resources.

### 30. What is Swagger2?
**Answer:**
Swagger is used to describing the structure of APIs. Swagger 2 is an open-source service provided in Spring Boot which makes it easier for the machines to find out the structure of APIs like RESTful Web services.

### 31. What are different environments for enterprise application development?
**Answer:**

- Dev
- QA
- Stage
- Production

### 32. What are the major differences between RequestMapping and GetMapping?
**Answer:**
RequestMapping can be used with GET, POST, PUT, and many other request methods using the method attribute on the annotation. Whereas GetMapping is only an extension of RequestMapping, which helps you to improve clarity on requests.

### 33. What is the use of profiles in Spring Boot?
**Answer:**
Profiles in Spring Boot are a way to define different sets of configurations for your application depending on the environment it is being run in. For example, you might have one set of configurations for your development environment and another set of configurations for your production environment.

### 34. What is LiveReload in Spring Boot?
**Answer:**
LiveReload is a spring-boot-devtools module that includes LiveReload server to trigger a browser refresh when a resource is changed. LiveReload server extensions are available freeware for Firefox, Chrome, and Safari.

### 35. What do you mean by hot-swapping in Spring Boot?
**Answer:**
It is a way to reload the changes without restarting Tomcat, or Jetty server. Eclipse and Many other IDEs support bytecode hot swapping. If you make any changes that don’t affect the method signature, it should reload without side effect.

### 36. What is the difference between build path and classpath?
**Answer:**
Build path is used by the compiler to resolve dependencies and build a project. Classpath is used during runtime when running a project in order to find necessary dependencies. Build path is configured on the Java Build Path property page of a project.

The classpath also contains additional libraries (JARs), which also can have a static folder, which would then be included for serving static resources.

### 37. What is the meaning of Aspect-Oriented Programming (AOP)? 
**Answer:**
Aspect-oriented programming (AOP) is an approach to programming that allows global properties of a program to determine how it is compiled into an executable program. AOP can be used with object-oriented programming ( OOP ). An aspect is a subprogram that is associated with a specific property of a program.

In computing, aspect-oriented programming (AOP) is a programming paradigm that aims to increase modularity by allowing the separation of cross-cutting concerns.

### 38. How to enable logging in Spring Boot?
**Answer:**
In application.properties add this property.
`debug=true`

### 39. Explain Docker in Spring Boot.
**Answer:**
Docker is a platform that combines your application, its dependencies, and even an OS into an image that can run on any platform.

### 40. Define ELK stack.
**Answer:**
The ELK Stack is made of three open-source products: 
- Elasticsearch: It is a NoSQL database which is based on the open-source search engine
called Lucene.
- Logstash: It is a data processing pipeline tool which accepts inputs from sources, performs
different transformations, and exports the data to targets.
- Kibana: Kibana helps users to visualize data with graphs and chart in Elasticsearch.

### 41.  How to handle exception in Spring Boot.
**Answer:**
Spring Boot provides a very useful way to handle exceptions using @ControllerAdvice annotation.

The @ExceptionHandler annotation is used to handle specific exceptions. The annotated method is invoked when the specified exceptions are thrown from a @Controller. We can define these methods either in a @Controller class or in @ControllerAdvice class.

### 42. Explain caching.
**Answer:**
Caching is a memory are that temporary stores frequently accessed data that is otherwise expensive to get or compute. Normally it's used to store session id, password, user interactions etc.

### 43. Define apache freemarker.
**Answer:**
FreeMarker is a Java based template engine from the Apache Software Foundation. Like other template engines, FreeMarker is designed to support HTML web pages in applications following the MVC pattern.

### 44. What is mean by spring batch?
**Answer:**
Spring Batch is the de facto standard for batch processing on the JVM. Its implementation of common batch patterns, such as chunk-based processing and partitioning, lets you create high-performing, scalable batch applications that are resilient enough for your most mission-critical processes.

### 45. Explain Apache Kafka.
**Answer:**
Apache Kafka is an open-source messaging platform. LinkedIn develops it. Apache Kafka enables the user to build distributed applications and handle real-time data feeds. Kafka is suitable for both offline and online messaging.

### 46. Explain CORS in Spring Boot?
**Answer:**
In Spring boot we have cors which stands for Cross-Origin Resource Sharing, it basically means that the host which is representing the UI, and the host which serves the data both are different. Means both are running on a different host, in such type of cases we may encounter this problem which running the application.

CORS is a W3C specification and mechanism that you can use to request restricted resources from a domain outside the current domain. In other words, CORS is a technique for consuming an API served from an origin different than yours.

### 47. Explain different types of dependency injection.
**Answer:**
- Setter injection: When dependencies are provided through a public property of the dependent class. 
- Constructor injection: When dependencies are provided through the constructor of the dependent class.
- Interface injection: When dependencies are provided directly in a method of the dependent class, as an argument.

### 48. What are the advantages of micro service?
**Answer:**
Following are the major advantages of micro service:
- It makes development fast and easy.
- Compatible with all container.
- Reduce production time.
- It's a lightweight model that supports a major business application.

### 49. What is the default package in Spring Boot?
**Answer:**
A class without any package declaration is considered as a default package.

### 50. Explain the difference between an embedded container and a WAR.
**Answer:**
The main difference between these two is:

Embedded containers help you to run Spring Boot application as a JAR from the command prompt without setting up any web server, while to run a WAR you need first to set up Tomcat.

### 51. Explain Spring MVC.
**Answer:**
A Spring MVC is a Java framework which is used to build web applications. It follows the Model-View-Controller design pattern. It implements all the basic features of a core spring framework like Inversion of Control, Dependency Injection.

### 52. What do you mean by aspect in spring?
**Answer:**
Aspects enable the modularization of concerns (such as transaction management) that cut across multiple types and objects. (Such concerns are often termed "crosscutting" concerns in AOP literature.) One of the key components of Spring is the AOP framework. It can done using @Aspect annotation.

### 53. What is join point in Spring Boot?
**Answer:**
It is a program execution point like the handling of an exception or the execution of a method. I  AOP, a join point is referred to as a method execution.


### 54. How can you set active profile in Spring Boot?
**Answer:**
In Spring Boot, you can set the active profile using the spring.profiles.active property. Here are a couple of ways to do it:

1) Application Properties File:

- Add the following line to activate the dev profile (replace dev with the desired profile):
`spring.profiles.active=dev`

- Spring Boot will load the corresponding application-dev.properties file.

2) Programmatic Configuration:
- In a web application, implement the WebApplicationInitializer interface.

### 55.  Is excluding package without using the basePackages filter is possible? How?
**Answer:**
Annotate classes you want to exclude with a custom annotation (e.g., @ExcludedFromITests).
In your main application class, use @ComponentScan with an excludeFilters attribute.
Java

```
@SpringBootApplication
@ComponentScan(basePackages = "com.example", excludeFilters = {
    @ComponentScan.Filter(type = FilterType.ANNOTATION, classes = ExcludedFromITests.class)
})
```

### 56. Explain steps to deploy an application on virtual machine.
**Answer:**
Below are the steps to deploy application on virtual machine.
- Install Java.
- Install the Application Server.
- Deploy the application war file.

### 57. List out some of the Spring Boot Starters.
**Answer:**
Different Spring Boot Starters are as follows:
- Security
- Parent
- web
- Thymeleaf
- Freemarker

#

### 58. What is Spring Boot?
**Answer:**
Spring Boot is used to create stand-alone, production ready Spring based applications that can just run.

Spring boot internally uses Spring framework which helps in making the application development easy and faster. It is built on top of Spring framework.

It helps in developing the microservice based application.

### 59. Advantages of Spring Boot?
**Answer:**
The main advantages of Spring Boot are:

- Auto Configuration – It helps in automatically configuring the application based on the dependencies added in the classpath. When using spring, to configure a datasource , a lot of configuration is need to configure entity manager ,transaction manager,etc. But Spring boot reduces to minimal configuration and uses the existing configuration.

- Starter POMS – It consists of multiple starter POMS which are mainly used to reduce maven configuration. It helps in maintaining the POM more easily as number of dependencies are reduced.

- Actuators – This helps in providing the production ready features of the application such as health check, metrics, classes loaded by the application,etc.

- Rapid Application Development – Spring Boot provides the infrastructure support which is required for our application and hence the application can be developed in the quickest manner. 

- Embedded Servers – It comes with embedded servers such as Tomcat, Jetty etc without the need to set up an external server.

- Embedded Database Integration – It also supports integration with the embedded database such as H2 database.

### 60. What is the internal working of @SpringBootApplication annotation?
**Answer:**
: It is a combination of three annotations `@ComponentScan`, `@EnableAutoConfiguration` and `@Configuration`.

- `@Configuration`: It is a class level annotation which indicates that a class can be used by the Spring IOC container as a source of bean definition. The method annotated with @Bean annotation will 
return an object that will be registered as a Spring Bean in IOC.

- `@ComponentScan`: It is used to scan the packages and all of its sub-packages which registers the classes as spring bean in the IOC container.

- `@EnableAutoConfiguration`: This annotation tells how Spring should configure based on the jars in the classpath. For eg , if H2 database jars are added in classpath , it will create datasource 
connection with H2 database.


### 61. What is Spring Initializer.
**Answer:**
Spring initializer is a web - based tool which is used to create a project structure for spring based applications. It does not generate any source code but helps in creating a project structure by providing maven or gradle build tool for building the application.

### 62. What is the default port number of tomcat in Spring Boot? Is it possible to change the port number?
**Answer:**
The default port number of tomcat is 8080, yet it is possible to override it using the property server.port = port_number in application.properties or application.yml.

### 63. What are the spring boot starters?
**Answer:**
Spring Boot provides multiple starter projects which are needed to develop different types of web application. For e.g., if we add spring-boot-starter-web as a dependency in pom.xml, we can develop mvc applications. All the dependency jars will be added to the classpath which are required for the application development using MVC.

Some of the starter POMS are:
- Spring-boot-starter – It helps in developing stand-alone applications.
- Spring-boot-starter-web - It helps in designing web based and distributed applications.
- Spring-boot-starter-data-jpa – used in designing the persistence layer.

It reduces the code for maven configuration.

### 64. Explain the need of dev-tools dependency.
**Answer:**
The main aim of adding dev-tools dependency is to improve the development time. When this dependency is included in the project, it automatically restarts the server when there are any modifications made to the source code which helps in reducing the effort of a developer to manually build and restart the server. 

### 65.  Difference between Spring and Spring Boot.
**Answer:**
- Spring – It is an open-source J2EE framework which helps in developing web based and 
enterprise applications easily. Its main feature is dependency injection by which we can achieve 
loosely coupling while developing the application. In order to develop a web application, developer 
needs to write a lot of code for configuring the dispatcher servlet in web.xml, configuring the 
database,etc. This can be avoided while using Spring Boot.It does not support embedded servers and 
embedded database integration.

- Spring Boot – Spring Boot is built on top of Spring framework which provides flexibility to design 
applications in a rapid and easier approach. It provides auto configuration feature through which it 
reduces the developer’s effort to write large xml configuration. It provides support for embedded 
server without the need to install it explicitly.

### 66. How to create a spring boot project using Spring Initializer?
**Answer:**
Spring initializer is a web-based tool developed by Pivotal. With the use of it, we can easily create the project structure needed to develop Spring based application.
- Go to the official Spring Initialize website: https://start.spring.io
- Select the project details such as language, spring boot version, build tool which is needed for 
application development as:
- Language: Java
- Java Version: 1.8 
- Spring Boot: 2.1.4
- Add the required dependencies and click on Generate project. It shall the download the project in your system.
- Import the zip file into the eclipse.

### 67. What is a Spring Bean?
**Answer:**
A java class which is managed by the IOC container is called as Spring Bean.The life cycle of the spring bean are taken care by the IOC container.
A spring bean can be represented by using the below annotations.
- @Component
- @Service
- @Repository
- @Configuration
- @Bean
- @Controller
- @RestController

### 68. What is the use of @Configuration annotation?
**Answer:**
A class which is used to provide few configurations such as Swagger configuration, Kafka configuration,etc can be represented using @Configuration annotation. This class contains Bean 
methods to customize the object creation and returns the object which can be represented as a Spring Bean by the IOC container.


### 69. What is Auto-wiring?
**Answer:**
Autowiring is the process of injecting one class object into another class. It cannot be implied on primitive types and String type.

Autowiring can be done in 3 ways:
- Constructor Injection
- Setter Injection
- Field Injection (@Autowired)

### 70. What is a Runner and its use?
**Answer:**
Runner classes are used to execute the piece of code as soon as the application starts. The code inside the runner classes will execute once on bootstrap of the application. There are mainly used to setup a data source, load the data into cache, etc. These runners will be called from SpringApplication.run() method.

There are two types of Runner Interfaces.
- ApplicationRunner
- CommandLineRunner

### 71. What is ApplicationRunner in SpringBoot?
**Answer:**
Application Runner is a functional interface which contains only one abstract method run().

When there is a need to execute some piece of code during the bootstrap of the spring boot application, then we need to write a Runner class to override the run method and provide the 
implementation.

![alt text](images/image-0.png)

### 72. What is CommandLineRunner in SpringBoot?
**Answer:**
CommandLineRunner is similar to the ApplicationRunner interface which is also used to execute the logic only once during application startup. The only difference between CommandLineRunner and ApplicationRunner is that ApplicationRunner accepts the arguments in the form of ApplicationArguments where as CommandLineRunner accepts in String[] array.
![alt text](images/image-1.png)

### 73. Explain Constructor Injection.
**Answer:**
Constructor Injection is the process of injecting the dependent bean object into the target bean 
using the target class construction. 
E.g. : If a class Car is dependent on the Engine object which is needed for Car to run, in this case 
Engine object will be created first and dependency will be injected into Car class. If the dependency is 
achieved using the target class constructor, it is referred to as Constructor injection.
![alt text](images/image-2.png)

It is not mandatory to give @Autowired annotation if there is only one constructor.

### 74. Explain Setter Injection. 
**Answer:**
Setter injection is another mechanism to perform dependency injection. In this approach, the 
dependent object is injected into target class using target class setter methods. Setter injection can 
override the constructor injection.
@Autowired annotation is used on the setter methods.
![alt text](images/image-3.png)

In setter injection, target class object should be created first followed by dependent object.

### 75. Explain Field Injection.
**Answer:**
Field injection is a mechanism where the dependent object is injected into the target object using target class variable directly with the use of @Autowired annotation. It internally uses Reflection API to perform field injection.
![alt text](images/image-4.png)

### 76. Can you override the default web server in Spring Boot.
**Answer:**
By default, Spring Boot provides Tomcat as the embedded server. This can be changed, as we can configure Jetty, Netty as embedded servers in Spring boot. This can be done in a convenient way by adding the starter dependencies in the maven pom.xml.
Example: Adding Jetty as dependency to pom.xml
```
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-jetty</artifactId>
</dependency>
```

## Spring-JPA

### 77. What is Spring Data JPA
**Answer:**
- Spring data JPA is used for designing the persistence layer of the web application. 
- It is used for managing the relational data in a java application. It acts as an intermediate between the java object and relational database.
- Spring data JPA is mainly built on top of JDBC API and it helps in reducing the boilerplate code.
- Spring boot provides a starter-POM `spring-boot-starter-data-jpa` which is used to design the DAO layer. All the required jars are added to the classpath after adding the starter pom in dependency management configuration file.
- It provides predefined interfaces which has methods to perform CRUD operations

### 78. Explain features of Spring Data JPA?
**Answer:**
The main advantages of using Spring Data are:

- No-code repositories: Spring data provides predefined repository interfaces which should be extended to create a repository for the entity class. It has the built-in methods to perform the CRUD 
operation.
- Reduces Boilerplate code: It reduces a lot of boiler plate such as creating a connection object, creating a statement and executing the query,closing the resources,etc.Spring data provides predefined methods which are already implemented in the Repository interfaces,
and by just calling those methods, we can perform CRUD operations.

- Generation of the queries: Another feature is queries are automatically generated based on the method names.
Eg: If there is a method in EmployeeRepository as:

`public List<Employee> findByName(String empName);`

Spring data jpa will create a query as below :

`select e.empid,e.empname,e.esalary from employee e where e.name = ? ;`
- Pagination and Sorting support: It supports pagination and sorting using predefined interface PagingAndSortingRepository.

### 79. How to create a custom Repository class in Spring JPA?
**Answer:**
We can create custom repository by extending one of the interfaces as below:
- CrudRepository
- JpaRepository
- PagingAndSortingRepository

E.g.:-

`public interface EmployeeRepo extends JpaRepository<Employee, Integer>{}`


### 80. Difference between CRUDRepository and JPARepository.
**Answer:**
CrudRepository interface provides method to perform only crud operations. 

It allows to create , read, update and delete records without creating own methods.

JPARepository extends PagingAndSortingRepository which provides methods to retrieve records using pagination and also to sort the records.

PagingAndSortingRepository extends CrudRepository which allows to do CRUD operations.

### 81. Write a custom query in Spring JPA?
**Answer:**
A custom query can be written using @Query annotation in the Repository interface. Using this annotation, we can write HQL queries and native SQL queries.

HQL queries can be written as below to fetch Emp Salary based on name.

E.g:-
```
@Query("Select * from employees")
public List<Employee> getAllEmployees();
```

### 82. What is the purpose of save () method in CrudRepository
**Answer:**
An entity can be saved into the database using save () method of CrudRepository. It will persist 
or merge the entity by using JPA Entity Manager. If the primary id is empty, it will call 
entityManager.persist(…) method, else it will merge the existing record by making a call to 
entityManager.merge(…) method.

### 83. Difference between findById() and getOne()
**Answer:**
The findById() method is available in CrudRepository while getOne() is available in JpaRepository.
 
The findById() returns null if record does not exist while the getOne() will throw an exception called EntityNotFoundException.

getOne() is a lazy operation where it will return a proxy without even hitting the database.

findById() – will retrieve the row record by directly hitting the database.

### 84. Use of @Temporal annotation.
**Answer:**
Prior to Java 8, @Temporal annotation is mainly used to convert the date and time values of an object to the compatible database type.

Generally, when we declare a Date field in the class and try to store it.It will store as TIMESTAMP in the database.

Eg:

```
@Temporal
private Date DOJ;
```

Above code will store value looks like 08-07-17 04:33:35.52000000 PM.

We can use TemporalType to DATE if the requirement is to store only date.

```
@Temporal (TemporalType.DATE)
private Date DOJ;
```

But after Java 8, there is no need to use @Temporal due to the introduction of LocalDate and LocalTime Api.


### 85. Write a query method for sorting in spring data jpa.
**Answer:**
Spring data JPA provides two ways to sort the records in ascending and descending manner.
- Approach 1: Using OrderBy method

    `List<Employees> findAllByOrderByEmpNameAsc()`

- Approach 2: Using Sort.by method 
To sort the same above requirement, we can write the method as below

    `List<Employee> employees = empRepo.findAll(Sort.by(Sort.Direction.ASC, "empName"));`

### 86. Explain @Transactional annotation in Spring.
**Answer:**
A database transaction is a sequence of statements/actions which are treated as a single unit of 
work. These operations should execute completely without any exception or should show no changes 
at all. The method on which the @Transactional annotation is declared, should execute the 
statements sequentially and if any error occurs, the transaction should be rolled back to its previous 
state. If there is no error, all the operations need to be committed to the database. By using 
@Transactional, we can comply with ACID principles.

E.g.: If in a transaction, we are saving entity1, entity2 and entity3 and if any exception occurs while 
saving entity3, then as enitiy1 and entity2 comes in same transaction so entity1 and entity2 should be 
rolledback with entity3.

A transaction is mainly implied on non-select operations (INSERT/UPDATE/DELETE).


### 87. What is the difference between FetchType.Eager and FetchType.Lazy?
**Answer:**
If there exists a relationship between two entity classes, in this case for eg: Company Entity and an Employee entity as shown in the diagram.

When you are trying to load the company details, it will load the id, name columns, etc. But it will not 
load the employee details. Employee details can be loaded in two ways.

FetchType.LAZY – It will not load the Employee details while firing the query to get Company Data.
This is called as lazy loading where in the employee details will be loaded on demand.

FetchType.EAGER – This will load all the employee details while loading the Company data.

### 88. Use of @Id annotation.
**Answer:**
@Id annotation is used on a field of an Entity class to mark the property/column as a primary 
key in the database. It is used along with @GeneratedValue which is used to generate the unique 
primary keys.

### 89. How will you create a composite primary key in Spring JPA.
**Answer:**
A composite primary is a combination of two or more primary keys in a database table.We can 
create composite primary keys in 2 ways in spring data jpa.
1. Using @IdClass annotation – Suppose there is a CustomerAccount class which has two 
primary keys(account Id, account type)
Then we need to create an AccountPK class which must be public and should implements the 
serializable interface.

```
@Data
public class AccountPK implements Serializable{
    private Integer accId;
    private String accType;
}
```
Associate this class with the CustomerAccount Entity. In order to do that, we need to annotate 
the entity with the @IdClass annotation. Also the declare the primary key columns in entity 
with @Id annotation.

![alt text](images/image-5.png)

2. Using @EmbeddedId annotation –
Create a class which implements Serializable interface which contains all primary keys in it. 
Annotate the class with @Embeddable annotation.

![alt text](images/image-6.png)

### 90. What is the use of @EnableJpaRepositories method? 
**Answer:**
If the repositories classes belong to the sub package of the Spring Boot Main class, then 
@SpringBootApplication is enough as it scans the package using @EnableAutoConfiguration.
If the repository classes are not part of the sub package of the Main class, in that case, it will not scan 
the repository classes, we need to use @EnableJpaRepositories. This needs to be provided in 
Configuration class or SpringBootApplication class.

### 91. What are the rules to follow to declare custom methods in Repository.
**Answer:**
We need to follow certain rules to declare custom methods to retrieve the data as below.

The fetch methods should start with findByXXXXX followed by property name.

If you want to retrieve list of employees based on name, then write the custom method in Repository as:

`public List<Employee> findByEmpName(String name);`

Here the property name in entity class is empName which should be in camel case while appending 
to the findBy method.

### 92. Explain QueryByExample in spring data jpa.
**Answer:**
It is another way to pass the search criteria in the where clause where the requirement is to 
retrieve the data based on multiple conditions.
It allows us to generate the queries based on Example instance.
Example instance is created as 
`Example<Employee> empExample = Example.of(emp);`
Where emp obj holds the search criteria.

Eg: Search for an employee whose empId is 102, name is Swathi and salary is 14000.

![alt text](images/image-7.png)

### 93. What is pagination and how to implement pagination in spring data?
**Answer:**
It is the process of displaying the records in small chunks into multiple pages. 

Eg: in an ecommerce application, there are several products available, but all of them will not be loaded on first 
page, if the client clicks on second page, few of them will be loaded and so on. This is mainly to avoid 
the overload on the application.

Pagination contains two fields – pageSize and pageNumber.

It can be implemented using PagingAndSortingRepository which provides methods to retrieve data 
using pagination.

Page findAll(Pageable pageable) – it returns the n records based on the pageSize to be 
displayed on each page.

To apply pagination on the records fetched from database, we need to create Pageable object as :

`PageRequest pageReq = PageRequest.of(pgNo,pageSize);`
And then pass to the find method as:

`Page<Employee> pageData = repository.findAll(pageReq);`

### 94. Explain few CrudRepository methods.
**Answer:**
Some of the methods to perform DML operations are :

- findById – to retrieve record based on the primary key.

- findAll – to retrieve all records from the database.

- existsById – to check if the record exists by passing primary key

- count – to check the total number of records.
- Save – to insert a record into the database
- deleteById – to delete a record using primaryKey
- deleteAll – to delete all records from the table

### 95. Difference between delete () and deleteInBatch() methods.
**Answer:**
delete() – It is used to delete a single record at a time. It internally uses remove method of 
entitymanager.

deleteInBatch() – it can delete multiple records at a time, it internally calls executeUpdate() method.It 
is much faster than delete method.

