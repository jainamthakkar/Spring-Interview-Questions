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

### 82. What is the purpose of save () method in CrudRepository?
**Answer:**
An entity can be saved into the database using save () method of CrudRepository. It will persist 
or merge the entity by using JPA Entity Manager. If the primary id is empty, it will call 
entityManager.persist(…) method, else it will merge the existing record by making a call to 
entityManager.merge(…) method.

### 83. Difference between findById() and getOne().
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


### 96. What is the use of @Modifying annotation?
**Answer:**
It indicates that a query method should be considered as a modifying query. It can be implied only on non-select queries (INSERT, UPDATE, DELETE). This annotation can be used only on the query methods which are defined by @Query annotation.

## SpringWeb-MVC

### 97. What is Spring MVC?
**Answer:**
Spring MVC is one of the modules in Spring framework which helps in building web and distributed applications. It supports two design patterns
- MVC Design Pattern
- Front Controller Design Pattern

MVC stands for Model, View and Controller.

The major role is played by DispatcherServlet in Spring MVC which acts as a front controller which receives the incoming request and maps it to the right resource.

The main advantage of Spring MVC is that it helps in the separation of the presentation and business layer.

The components of Spring MVC are:

- Model – A model represents the data which can be an object or a group of objects.

- View – A view represents an UI to display the data. It can be a JSP, or a Thymeleaf page.

- Controller – It acts as an intermediate between model and view components and is responsible to  handle the incoming requests.

- Front Controller – Dispatcher servlet serves the main purpose of redirecting the request to the 
respective controller methods.

### 98. Explain the flow of Spring MVC.
**Answer:**
When a client request comes in, it is intercepted by the Dispatcher Servlet which acts as a Front Controller. The dispatcher servlet is responsible for pre – processing of the request and calls the handler methods to decide which controller should handle the request. It uses BeanNameUrlHandlerMapping and SimpleUrlHandlerMapping to map the request to the corresponding controller method. The controller then processes the request and sends the response 
as ModelAndView back to the DispatcherServlet. Model represents the data to be displayed and view 
represents the component in which data should be rendered on the browser.
Front Controller is also responsible in manipulating the response data(post-processing) before 
sending back to client.

![alt text](images/image-8.png)

### 99. What is Dispatcher Servlet. 
**Answer:**
Dispatcher Servlet acts as a central servlet which handles all the incoming HTTP Requests and 
Responses. Once a client request is sent, it is received by the DispatcherServlet and it forwards the 
request to handler mapper to identify the corresponding controller class to handle the request. The 
controller performs all the business logic and hands over the response back to DispatcherServlet. The 
servlet then prepares the view component by looking for the view resolver in properties file and sends 
the data to be rendered on view page.

### 100. What is the use of @Controller annotation. 
**Answer:**
A class can be represented as a Controller class which is used to handle one or more HTTP requests. It is represented as a controller class using @Controller annotation. It is one of the 
stereotype annotations.
In the example above, whenever a client sends a request with the url as localhost:8090/home, the 
homepage method is invoked and view is returned from the method.


### 101. What is the use of InternalResourceViewResolver?
**Answer:**
InternalResourceViewResolver is the implementation of View Resolver interface which is used 
to resolve logical view names returned by the controller to a physical location where file actually
exists. It is also a subclass of UrlBasedViewResolver which uses “prefix” and “suffix” to convert the 
logical view into physical view.

For example, if a user tries to access /home URL and HomeController returns "home" then 
DispatcherServlet will check with InternalResourceViewResolver and it will use prefix and suffix to find 
the actual physical view.
Iif prefix is "/WEB-INF/views/" and suffix is ".jsp" then "home" will be resolved to "/WEBINF/views/home.jsp" by InternalResourceViewResolver.

### 102. Difference between @RequestParam and @PathVariable.
**Answer:**
@RequestParam is used to access the parameter values which are passed as part of request 
URL.
URL: http://localhost:8090/fee?cname=SBMS&tname=Savitha
In the above example, we can access the parameter values of courseName and trainerName using 
@RequestParam annotation. In case of @RequestParam, if the parameter value is empty , it can take 
default value using attribute defaultValue=XXXXX

![alt text](images/image-9.png)

@PathVariable – It is used to extract data from the request URI. Eg : if the URL is as : 
http://localhost:8090/carPrice/{carName} – the value for the placeholder {carName} can be 
accessed using @PathVariable annotation. In order to access the carName, we need to write code as 
below

### 103. Explain @Service and @Repository annotations.
**Answer:**
A class which is annotated with @Repository annotation is where the data is stored. It is a 
stereotype annotation for the persistence layer.
@Service – It indicates that a java class contains the business logic. It is also a part of @Component 
stereotype annotation.

### 104. What is the purpose of @Model Attribute?
**Answer:**
It is part of Spring MVC module and can be used in two scenarios:
@ModelAttribute at method level: When used at method level, it indicates that a method will return 
one or more model attributes.

![alt text](images/image-10.png)

### 105. Explain @RequestBody annotation.
**Answer:**
This annotation indicates that the method parameter should be bound to the body of the HTTP 
request.

```
@PostMapping("/addUser")
public String addUser(@RequestBody User user){
    System.out.println("user saved");
}
```

### 106. What is the use of Binding Result.
**Answer:**
BindingResult holds the result of the validation and binding and contains errors that have 
occurred. The BindingResult is a spring’s object which must come right after the model object that is 
validated or else Spring will fail to validate the object and throw an exception.

![alt text](images/image-11.png)

### 107. How does Spring MVC support for validation.
**Answer:**
It is used to restrict the user input provided by the user. Spring provides the validation API 
where the BindingResult class is used to capture the errors raised while validating the form.
We need to add spring-boot-starter-validation in pom.xml.

### 108. Explain @GetMapping and @PostMapping. 
**Answer:**
@GetMapping is an alternative for @RequestMapping (method = RequestMethod.GET )
It handles the HTTP Get methods matching with the given URI.

@ PostMapping is an alternative for @RequestMapping (method = RequestMethod.POST)
It handles the HTTP Post methods matching with the given URI.

### 109. How to send the data from Controller to UI.
**Answer:**
In spring mvc, controller is responsible to send the data to UI. We have Model object and 
ModelAndView to send the data from controller to UI.
The data in the model object is represented in key-value format as below.
`model.addAttribute(“key”,”value”);`


### 110. What is the purpose of query parameter?
**Answer:**
QueryParameters are used to send the data from UI to Controller.The query parameters are 
passed in the URL and starts with ?.
Multiple query parameters will be represented with ampersand operator (&).

Query Parameters are appended at the end of the URL and this can be retrieved from the url using 
@RequestParam annotation.

Eg: 

`http://localhost:8090/studentapp?sid=100&sname=Raju`

### 111. Describe the annotations to validate the form data.
**Answer:**
Some annotations to validate the form data.
- @NotNull – It is used to check if the value entered is not null.
- @NotEmpty – It checks whether the annotated element is not null nor empty.
- @Email – It checks whether the given value is a valid email address.
- @Size – It is used to determine that size of the value must be equal to the mentioned size.
- @Null – It checks that the value is null.

### 112. What do you know about Thymeleaf?
**Answer:**
Thymeleaf is used to design the presentation logic. It is a java template engine that helps in 
processing and creating HTML,javascript,etc.

It reads the template file and parses it and produces web content directly on the browser.

It helps in developing dynamic web content.


### 113. Explain the use of @ResponseBody annotation.
**Answer:**
@ResponseBody on a method indicates that the return type should be directly written to the response object.

![alt text](images/image-12.png)

### 114. What is the role of Handler Mapper in Spring MVC.
**Answer:**
Handler mapper is used to map the incoming request to the respective controller method. DispatcherServlet forwards the request received to handler mapper.By default ,It uses BeanNameUrlHandlerMapping and DefaultAnnotationHandlerMapping to map the request to the controller.

### 115. How will you map the incoming request to a Controller method.
**Answer:**
When a client request is received by the dispatcher servlet with the URI , for example as 
http://localhost:8090/home , the central servlet forwards the request to handler mapper which 
checks for the controller method which matches the url pattern, in this case /home and returns the 
name of the controller. The front controller then sends the request to the appropriate Controller which 
processes the business logic and sends back the response to the client.

### 116. How to bind the form data to Model Object in Spring MVC.
**Answer**
In Spring MVC, binding form data to a model object is a straightforward process. It involves using the @ModelAttribute annotation, which tells Spring to populate the model object with the form data. Here's how you can do it step-by-step:

Step-by-Step Guide
1. Create a Model Class: This class will represent the form data.

    ```
    public class User {
        private String firstName;
        private String email;
        private String password;

        // Getters and Setters
    }
    ```

2. Create the Form in JSP: Create a JSP file with a form that will submit data to the Spring controller.
    ```
    <%@ taglib uri="http://www.springframework.org/tags/form" prefix="form" %>
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="ISO-8859-1">
        <title>Ecom Signup</title>
    </head>
    <body>
        <h2>Ecom Signup</h2>

        <form:form action="signup" method="post" modelAttribute="user">
            First Name: <form:input path="firstName" /><br><br>
            Email: <form:input path="email" /><br><br>
            Password: <form:password path="password" /><br><br>
            <input type="submit" value="Signup" />
        </form:form>
    </body>
    </html>
    ```

3. Create the Controller: In the controller, you will handle the form submission and bind the form data to a User object.

    ```
    @Controller
    public class EcomSessionController {
        
        @Autowired
        private EUserDao userDao;

        @GetMapping("/signup")
        public String showSignupForm(Model model) {
            model.addAttribute("user", new User());
            return "EcomSignup";
        }

        @PostMapping("/signup")
        public String processSignup(@ModelAttribute("user") User user) {
            userDao.insertUser(user);
            return "EcomLogin";
        }
    }
    ```

### 117. What is Spring MVC Tag library.
**Answer**
Spring provides a tag library which is used in creating view component. It provides tags to create 
HTML fields, error messages, etc. It is a predefined library which can be used in JSP by using the tag 
as:

`<%@ taglib uri="http://www.springframework.org/tags/form" prefix="form" %>`

After adding the above tag, we can create HTML form input text by using prefix as “form”.

`<td> <form:input path=productId/></td>`


### 118. Difference between @Controller and @RestController annotations. 
**Answer**
A class which is annotated with @Controller indicates that it is a controller class which is 
responsible to handle the requests and forwards the request to perform business logic. It returns a 
view which is then resolved by ViewResolver after performing business operations. 

@RestController is used in REST Webservices and is combination of @Controller and 
@ResponseBody.It returns the object data directly to HTTP Response as a JSON or XML.

### 119. Explain few tags in Spring MVC tag library.
**Answer**
Few of the spring mvc tags are :
- `<form:form>` - It is used to create a HTML form.
- `<form:input>` - It is used to create input text field.
- `<form:radiobutton>` - It is used to create a radio button.
- `<form:select>` - It is used to create a dropdown list.
- `<form:hidden>` - It is used to create a hidden field.
- `<form:checkbox>` - It is used to create a checkbox.
- `<form:option>` - It is used to create a single Html option inside select tag.


### 120. Explain the use of @ResponseEntity annotation.
**Answer**
@ResponseEntity is used to represent the entire HTTP response such as status code, headers 
and response body.
We can return the entire response from the endpoint. When using @ResponseBody , it returns the 
value into the body of the http response.

```
    @GetMapping("/greet")
    public ResponseEntity<String> greet(@RequestParam(value = "name", defaultValue = "World") String name) {
        String body = "Hello, " + name + "!";
        return new ResponseEntity<>(body, HttpStatus.OK);
    }
```

### 121. How to handle exceptions in Spring MVC.
**Answer:**
In Spring Boot, exceptions can be handled using below two annotations:
- @ExceptionHandler -specific to a controller class
- @ControllerAdvice – common to all controllers.

### 122. Explain @ControllerAdvice in Spring Boot.
**Answer:**
@ControllerAdvice is a specialization of @Component annotation which is used to handle the 
exceptions across the whole application by providing a global code which can be applied to multiple 
controllers.

# Spring Actuator

### 123. What is Spring actuator and its advantages.
**Answer:**
An actuator is mainly used to provide the production ready features of an application. It helps to monitor and manage our application. It provides various features such as healthcheck, auditing, beans loaded into the application,etc.

### 124. How will you enable actuator in spring boot application.
**Answer:**
An actuator can be enabled by adding the starter pom into the pom.xml.

```
    <dependency>
        <groupId> org.springframework.boot</groupId>
        <artifactId> spring-boot-starter-actuator </artifactId>
    </dependency>
```   


### 125. What are the actuator endpoints which are needed to monitor the application.
**Answer:**
Actuators provide below pre-defined endpoints to monitor our application.
- Health
- Info
- Beans
- Mappings
- Configprops
- Httptrace
- Heapdump
- Threaddump
- Shutdown

### 126. How to get the list of beans available in spring application.
**Answer:**
Spring Boot Actuator provides an endpoint url /beans to load all the spring beans of the application.

### 127. What is a shutdown in the actuator?
**Answer:**
A shutdown is an endpoint that helps application to shut down properly. This feature is not 
enabled by default. We can enable it by giving the below command in properties file.

`management.endpoint.shutdown.enabled=true `

# Spring Security

### 128. What is Spring Security?
**Answer:**
Spring security is a powerful access control framework. It aims at providing authentication and authorization to java applications. It enables the developer to impose security restrictions to save from 
common attacks.

### 129. What are the features of Spring Security?
**Answer:**
Spring security provides many features as below:
- Authentication and Authorization.
- Supports Basic and Digest Authentication.
- Supports CSRF Implementation.
- Supports Single Sign-on.

### 130. How to implement JWT?
**Answer:**
JWT stands for Json Web Token which helps in implementing token-based security. Token is 
generated using the secret key. We need to add below dependency in pom.xml.
```
<dependencies>
    <dependency>
        <groupId>io.jsonwebtoken</groupId>
        <artifactId>jjwt</artifactId>
        <version>0.9.1</version>
    </dependency>

    <dependency>
        <groupId>javax.xml.bind</groupId>
        <artifactId>jaxb-api</artifactId>
        <version>2.3.0</version>
    </dependency>
</dependencies>
```

The following diagram depicts the working of JWT.

![alt-text](images/image-13.png)


### 131. What is DelegatingFilterProxy in Spring Security.
**Answer:**
It is a predefined filter class which helps in performing pre-processing of the request.It supports 
for both authentication and authorization. It is a proxy servlet filter which acts as an intermediator 
before redirecting the request to dispatcher servlet.

### 132. What is Spring Security OAuth2.
**Answer:**
OAuth2 is an authorization framework, granting clients access to protected resources via 
authorization server. It allows end user’s account information to be used by third party 
services(eg.facebook) without exposing user’s password.
The oAuth token are random strings generated by the authorization server.

There are 2 types of token.

- Access token – It is sent with each request, usually valid for about an hour only.
- Refresh token – It is used to get a new access token, not sent with each request. It lives longer than 
access token.

### 133. What is the advantage of using JWT Token?
**Answer:**
Advantages of using JWT Token:
- The jwt token has authentication details and expire time information.
- It is one of the approaches to secure the application data because the parties which are 
interacting are digitally signed.
- It is very small token and is better than SAML token.
- It is used at internet scale level, so it is very easy to process on user’s device.

### 134. What is authentication? 
**Answer:**
Authentication is the mechanism to identify whether user can access the application or not.

### 135. What is authorization?
**Answer:**
Authorization is the process to know what the user can access inside the application and what it 
cannot i.e which functionality it can access and which it cannot.

### 136. What is filter Chain Proxy?
**Answer:**
The filter Chain Proxy contains multiple security filter chains and a task is delegated to the filter 
chain based on the URI mapping. It is not executed directly but started by DelegatingFilterProxy.

### 137. What is security context in Spring Security.
**Answer:**
It is used to store the details of the current authenticated user, which is known as principle. So if we want to get the current username, we need to get the SecurityContext.

### 138. Difference between hasAuthority and hasRole?
**Answer:**
hasRole – defines the role of the user.It does not use the ROLE_prefix but it will automatically 
added by spring security as hasRole(ADMIN);

has Authority – defines the rights of the user. It uses ROLE prefix while using has Authority method as 
has Authority (ROLE_ADMIN)


### 139. How to enable spring boot security in spring boot project?
**Answer:**
If Spring boot Security dependency is added on class path, it automatically adds basic 
authentication to all endpoints. The Endpoint “/” and “/home” does not require any authentication. All 
other Endpoints require authentication.
The following dependency needs to be added.
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

### 140. What is Basic Authentication?
**Answer:**
In Basic Authentication, we send username and password as part of the request to allow user to 
access the resource. The user credentials are sent as authorization request headers. This approach 
is used to authenticate the client requests.


### 141. What is Digest Authentication?
**Answer:**
Digest Authentication is more preferable when compared to basic authentication as the 
credentials are in encrypted format by applying hash function to username,password,etc. It does not 
send the actual password to the server. Spring security provides digest authentication filter to 
authenticate the user using digest authentication header.

### 142. How to get current logged in user in spring security.
**Answer:**
We can get the current logged in user by using the following code snippet.

`User user = (User)SecurityContextHolder.getContext().getAuthentication().getPrincipal();`

`String name = user.getUsername();`


### 143. What is SSL and its use?
**Answer:**
SSL stands for secure socket layer which is an encryption- based internet security protocol.

It is mainly used to secure client information (such as credit card number /password/ssn) to a web 
server.

SSL provides a secure channel between two machines or devices running over the internet. A 
common example is when SSL is used to secure communication between a web browser and a web 
server. This changes the address of the website from HTTP to HTTPS, basically 'S' stands for 'Secure'.


### 144. What is salting?
**Answer:**
Salting is used to generate random bytes that is hashed along with the password. Using salt , we 
can add extra string to password , so that hackers finds difficult to break the password. The salt is 
stored as it is, and need not be protected.

### 145. What is hashing in spring security.
**Answer:**
Hashing is an approach where a string is converted into encoded format using hashing 
algorithm. The hashing algorithm takes input as password and returns hashed string as output. This 
hashed data is stored in the database instead of plain text which is easily vulnerable to hacker 
attacks.

### 146. How to secure passwords in a web application?
**Answer:**
Generally, passwords should not be stored as plain text into the storage as it can easily be 
accessed by the hackers.

We need to use encryption techniques before storing the password.

We need to use hashing and salting techniques to prevent from security breaches.

### 147. What is AuthenticationManager in spring security?
**Answer:**
Authentication manager is the interface that provides the authentication mechanism for any 
object. The most common implementation of it is the AuthenticationProvider.

If the principal of the input is valid , and authenticated , it returns an authentication instance if 
successful.

It checks whether the username and password is authenticated to access a specific resource.

### 148. What are the various ways to implement security in spring boot project?
**Answer:**
There are 3 ways to implement security.

- In Memory Credential – In this mechanism, we configure the user credentials in the application itself,
and use it when there is a request to validate the user.

- Using JDBC Credentials – Here, the user credentials are stored into the database and when the 
client request comes, it is validated against it.

- Using UserDetailsService – It is an interface provided by Spring framework. After entering the 
username in the form and clicking on Login button invokes a call to this service. It locates the user 
based on the username provided. It contains a method loadUserByUsername(String username) which 
returns UserDetails object.

### 149. What are the essential components of Spring Boot? 
**Answer:**
Some of the components of Spring Boot are:
- Spring Boot Starter
- Spring Boot autoconfiguration
- Spring Boot Actuator
- Spring Boot CLI

### 150. How can you set active profile in Spring Boot?
**Answer:**
We can set the active profile by using configuration properties as:

`spring.profiles.active=production`

### 151. What is YAML?
**Answer:**
YAML is mainly used for configuration purpose. It is similar to properties file and provides more 
readability.


### 152. Use of @Profile annotation.
**Answer:**
The @Profile annotation indicates that a component is eligible for registration when the specified 
profile is active. The default profile is called default, all the beans that do not have a profile set belong 
to this profile.

### 154. How to get current profile in Spring Boot.
**Answer:** 
`String[] activeProfiles = environment. getActiveProfiles()`

### 153. Difference between Spring and Spring boot?
**Answer:** 
| Feature/Aspect          | Spring                                      | Spring Boot                                        |
|-------------------------|---------------------------------------------|----------------------------------------------------|
| Purpose                 | Comprehensive framework for Java applications | Simplifies Spring application development           |
| Configuration           | Manual configuration (XML, Java-based)       | Auto-configuration                                  |
| Startup                 | Requires setup of external server            | Embedded servers (Tomcat, Jetty, Undertow)          |
| Dependency Management   | Requires explicit dependency management      | Starter dependencies for common setups              |
| Project Initialization  | Manual setup                                 | Spring Initializr for quick project setup           |
| Deployment              | Deployed to external servers                 | Standalone deployment with embedded servers         |
| Use Case                | Suitable for complex, customized applications | Ideal for rapid development, microservices, and smaller projects |
| Application Context     | Manually created and managed                 | Automatically created and managed                   |
| Production Readiness    | Additional configuration needed              | Built-in production-ready features (e.g., metrics, health checks) |


### 155. Difference between @controller and @Restcontroller.
**Answer:** 
- The @Controller annotation is used to define a web controller in Spring MVC. It is typically used in combination with @RequestMapping annotations to handle web requests and return a view (e.g., HTML, JSP) for the client.
    ```
    @Controller
    public class MyController {
        @RequestMapping("/hello")
        public String hello(Model model) {
            model.addAttribute("message", "Hello, World!");
            return "hello"; // returns the view name "hello"
        }
    }
    ```
- The @RestController annotation is a specialized version of @Controller that is used 
to create RESTful web services. It combines @Controller and @ResponseBody, 
meaning that the methods in the controller return data directly in the body of the response, rather than a view.
    ```
    @RestController
    public class MyRestController {
        @RequestMapping("/hello")
        public String hello() {
            return "Hello, World!"; // returns "Hello, World!" as the response body
        }
    }
    ```


### 156. Difference between @Enableautoconfiguration and @SpringBootApplication.
**Answer:**
| Feature/Aspect                 | @EnableAutoConfiguration                                      | @SpringBootApplication                                      |
|--------------------------------|--------------------------------------------------------------|-------------------------------------------------------------|
| Purpose                        | Enables Spring Boot’s auto-configuration mechanism            | Convenience annotation that combines multiple annotations   |
| Annotations Combined           | Only @EnableAutoConfiguration                                 | @EnableAutoConfiguration, @ComponentScan, @Configuration    |
| Component Scanning             | Does not include component scanning                           | Includes component scanning                                 |
| Configuration Source           | Can be used independently                                     | Typically used as the main application class annotation     |
| Default Package Scanning       | No default package scanning                                   | Scans the package of the annotated class and its sub-packages |


### 157. How does Server configuration is done?
**Answer:**
There are various ways to configure a server in spring boot:
1. Configuration Properties in applicaion.properties file 
    ```
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.url=jdbc:mysql://localhost:3306/inventory_service
    spring.datasource.username=root
    spring.datasource.password=.
    ```
2. Using application.properties and Environment Variables

    `$ java -jar myapp.jar --server.port=8081 --server.servlet.context-path=/myapp`

3. Embedded Server Customization - Spring Boot applications typically use embedded 
servers such as Tomcat, Jetty, or Undertow. These can be further customized if 
needed.

### 158. What is the use of the new keyword in Java and Spring Boot?
**Answer:**
In Java, new is used to instantiate objects by invoking their constructors. In Spring 
Boot, it's also used for object instantiation, but Spring Boot emphasizes 
dependency injection, making direct use of new less common.

### 159. What are @Component and @ComponentScan used for?
**Answer:**
- @Component is used to denote a class as a Spring-managed component, while 
- @ComponentScan enables Spring to automatically discover and register 
components within specified packages.

### 160. What is @Configuration?
**Answer:**
@Configuration indicates that a class contains Spring bean definitions and is 
processed by the Spring container to generate bean definitions and manage those beans at runtime.

```
    @Configuration
    public class AppConfig {
        @Bean
        public MyService myService() {
            return new MyService();
        }
    }
```

### 161. What is @Component, when it is used?
**Answer:**
- The @Component annotation is one of the stereotype annotations provided by 
Spring Framework. It is used to indicate that a class is a Spring-managed 
component. Components are essentially Spring beans that are automatically 
detected and registered during the component scanning process.

- When you annotate a class with @Component, Spring will automatically create an 
instance of that class and register it as a bean in the application context. These 
beans can then be injected into other Spring-managed components using 
dependency injection.

- @Component is a generic stereotype annotation and serves as the base for more 
specific annotations like @Service, @Repository, and @Controller, each indicating 
a specific type of Spring-managed component with a distinct purpose.

### 162. Stereotype Annotations. 
**Answer:**
Spring Framework provides us with some special annotations. These annotations are used to create Spring beans automatically in the application context. @Component annotation is the main Stereotype Annotation. There are some Stereotype meta-annotations which is derived from @Component those are: (so we have total four stereotypes annotations.)

- @Service: We specify a class with @Service to indicate that they’re holding the business logic. Besides being used in the service layer, there isn’t any other special use for this annotation. The utility classes can be marked as Service classes.

- @Repository: We specify a class with @Repository to indicate that they’re dealing with CRUD operations, usually, it’s used with DAO (Data Access Object) or Repository implementations that deal with database tables.

- @Controller: We specify a class with @Controller to and responsible to indicate that a class serves as a controller, handle user requests and return the appropriate response. It is mostly used with REST Web Services.

### 163. What is Dependency injection and @Autowired?
**Answer:**
- Dependency injection (DI) is a design pattern used in software development to 
achieve loose coupling between components and facilitate modular, maintainable 
code. In the context of Spring Boot, dependency injection is a core feature that 
allows you to inject dependencies (i.e., objects) into other objects, rather than 
creating them manually or tightly coupling them within the class.

- @Autowired is the most commonly used annotation for dependency injection in 
Spring Boot. It tells the Spring container to automatically wire up dependencies for 
a particular bean. When Spring encounters a bean with an @Autowired annotation, 
it searches for a compatible bean in its application context and injects it into the 
dependent object.
Here's a simplified example to illustrate how @Autowired works in Spring Boot:
    ```
    @Service
    public class MyService {
        private final MyRepository repository;
        @Autowired
        public MyService(MyRepository repository) {
            this.repository = repository;
        }
    }
    ```
### 164. Difference between @requestparam and @pathvariable?
**Answer:**
@RequestParam and @PathVariable are both annotations used in Spring MVC for 
handling incoming HTTP requests, but they serve different purposes and are used in different scenarios.

- RequestParam
 ```   
    @GetMapping("/foos")
    @ResponseBody
    public String getFooByIdUsingQueryParam(@RequestParam String id) {
        return "ID: " + id;
    }
```   
- PathVariable
```
    @GetMapping("/foos/{id}")
    @ResponseBody
    public String getFooById(@PathVariable String id) {
        return "ID: " + id;
    }
```

### 165. Define ORM (Object-Relational Mapping) and discuss commonly used ORM frameworks in Spring Boot, such as Hibernate.
**Answer:**
Object-Relational Mapping (ORM) is a programming technique used to map objects 
from an object-oriented domain model to a relational database model and vice 
versa. It simplifies the interaction between object-oriented programming languages 
and relational databases by abstracting away the need to write complex SQL 
queries manually. ORM frameworks handle the mapping of objects to database 
tables, relationships between objects, and the translation of object-oriented 
operations into corresponding database operations.

Hibernate:

Description: Hibernate is one of the most popular ORM frameworks in the Java 
ecosystem. It provides a powerful and flexible way to map Java objects to database 
tables and vice versa.

Features:
- Object-oriented querying with HQL (Hibernate Query Language) or Criteria 
API.
- Support for various database vendors and dialects.
- Automatic schema generation and management.
- Support for caching mechanisms to improve performance.
- Lazy loading and eager loading strategies for associations.
- Integration with Spring Boot: Spring Boot provides seamless integration with 
Hibernate through starter dependencies, auto-configuration, and Spring 
Data JPA repositories.

Spring Data JPA:

Description: Spring Data JPA is a part of the broader Spring Data project, which aims 
to simplify database access in Spring applications. It builds on top of JPA (Java 
Persistence API) and provides additional features and abstractions to reduce 
boilerplate code.

Features:

- Repository abstraction for CRUD operations, reducing the need to write 
custom DAO (Data Access Object) implementations.
- Query methods derived from method names, reducing the need to write 
JPQL (Java Persistence Query Language) queries manually.
- Support for pagination, sorting, and dynamic query generation.
- Integration with Spring Boot: Spring Boot provides auto-configuration for 
Spring Data JPA repositories, making it easy to set up and use in Spring Boot 
applications.

### 166.  How do you handle database exceptions in Spring Boot? Talk about exception handling strategies and the use of @ControllerAdvice and @ExceptionHandler.
**Answer:**
- In Spring Boot, handling database exceptions effectively is crucial for building 
robust and reliable applications. There are several approaches and best practices 
for handling database exceptions, including the use of @ControllerAdvice and 
@ExceptionHandler.

- Catch and Handle Specific Exceptions:
Identify specific database-related exceptions that may occur, such as 
DataAccessException, SQLException, or framework-specific exceptions like 
Hibernate's HibernateException.

- Use Spring's DataAccessException Hierarchy:
Spring provides a hierarchy of exception classes under 
org.springframework.dao.DataAccessException. You can handle exceptions at 
different levels of abstraction, such as DuplicateKeyException, 
DataIntegrityViolationException, etc.

- Graceful Error Messages:
Provide meaningful error messages to users or clients when database operations 
fail. This helps in debugging and troubleshooting issues more efficiently.

- Logging:
Log exceptions and relevant details (e.g., error message, stack trace) using logging 
frameworks like Logback or Log4j. This information is valuable for diagnosing issues 
in production environments.

Use of @ControllerAdvice and @ExceptionHandler:

- @ControllerAdvice:
    
    - @ControllerAdvice is an annotation used to define global exception handling 
    for Spring MVC controllers. It allows you to centralize exception handling 
    logic in one place.
    - You can define methods annotated with @ExceptionHandler within a 
@ControllerAdvice class to handle specific types of exceptions across 
multiple controllers.

- @ExceptionHandler:
    - @ExceptionHandler is an annotation used to handle exceptions at the 
controller level. You can annotate methods within your controller classes 
with @ExceptionHandler to handle specific exceptions thrown by methods in 
that controller.
    - Spring Boot automatically detects and invokes @ExceptionHandler methods when 
the corresponding exception occurs during the execution of a controller method.

### 167. What is pagination in Spring Boot?
**Answer:**
- Spring Data JPA’s pagination feature provides an efficient way to handle large data 
sets by dividing them into manageable chunks, or pages, and retrieving them one at 
a time. This is particularly useful in applications where you need to display a subset 
of records from a large database table, such as in a web application with a 
paginated list of results.

Key Concepts:

- Pageable Interface - The Pageable interface provides pagination information such 
as the page number, page size, and sorting order.
Page Interface:The Page interface represents a single page of data and provides 
methods to access the content of the page and pagination details like total pages, 
total elements, current page, etc.

- Sorting - Sorting can be applied along with pagination by using the 
PageRequest.of(int page, int size, Sort sort) method, where Sort specifies the 
sorting criteria.

### 168. What are the best standards that are used in building RESTAPI?
**Answer:**
 Stateless/ Versioning /Documented / Use HTTP Methods and Status Code / 
Pagination, Filtering, and Sorting / Error Handling and Responses/Monitoring and 
Analytics.

### 169. Discuss strategies for managing and processing large datasets efficiently.
**Answer:**
- Managing and processing large datasets efficiently requires a combination of 
strategies to optimize performance, ensure scalability, and maintain system 
stability. Here are several strategies that can help you achieve these goals:
1. Database Optimization:
- Indexing: Create appropriate indexes on database tables to speed up query 
execution. Avoid over-indexing as it can slow down write operations.
- Query Optimization: Write efficient SQL queries. Use tools like EXPLAIN to 
analyze and optimize query execution plans.
- Partitioning: Split large tables into smaller, more manageable pieces using 
horizontal partitioning (sharding) or vertical partitioning.
- Connection Pooling: Use connection pools to manage database connections 
efficiently and reduce overhead.

2. Efficient Data Retrieval:
Pagination: Retrieve data in chunks using pagination to avoid loading large datasets 
into memory all at once.

3. In-Memory Data Processing:
- Batch Processing: Process data in batches to reduce memory usage and 
improve performance
- Caching: Use in-memory caches (e.g., Redis, Ehcache) to store frequently 
accessed data and reduce database load.

4. Data Warehousing and ETL:
- ETL (Extract, Transform, Load): Use ETL processes to transform and load 
large datasets into a data warehouse for efficient querying and analysis.
- Tools like Apache NiFi, Talend, and AWS Glue can help automate ETL 
processes.
- Data Warehousing: Use data warehousing solutions like Amazon Redshift, 
Google BigQuery, or Snowflake for scalable data storage and querying.
5. Cloud Services:
- Scalable Storage: Use cloud storage solutions like Amazon S3, Google Cloud 
Storage, or Azure Blob Storage to handle large datasets.
- Managed Services: Utilize cloud-based managed services for databases 
(e.g., Amazon RDS, Azure SQL Database) to handle scaling, backups, and 
maintenance.

6. Performance Monitoring and Tuning:
- Monitoring Tools: Use monitoring tools like New Relic, Datadog, or 
Prometheus to keep track of system performance and identify bottlenecks.
- Profiling: Profile your application to identify slow operations and optimize 
them.

### 170. Discuss the use of Spring Batch or other techniques for batch processing.
**Answer:**
Batch processing involves executing a series of jobs, typically large volumes of 
data, that are divided into manageable chunks. Spring Batch is a framework 
designed for batch processing and offers a robust, flexible, and high-performance 
solution for executing large-scale batch jobs.

Key Concepts in Spring Batch
- Job: Represents the batch process. It consists of multiple steps.
- Step: A single phase of the job, including reading, processing, and writing.
- ItemReader: Interface for reading data from a source.
- ItemProcessor: Interface for processing data.
- ItemWriter: Interface for writing data to a destination.

Other Batch Processing Techniques

1. Apache Kafka:
Apache Kafka is a distributed streaming platform often used for real-time data 
pipelines.

    Kafka Streams: A library for building applications and microservices that process 
data stored in Kafka.

    Consumer Groups: Use Kafka consumer groups to read and process messages 
from topics.

2. Hadoop MapReduce:
A programming model for processing large datasets with a distributed algorithm.

    Mapper: Processes input data and generates intermediate key-value pairs.

    Reducer: Aggregates intermediate data to produce final output.

Key Techniques for Batch Processing

1. Chunking:
Divide data into chunks and process each chunk independently to manage memory 
usage.

2. Parallel Processing:
Use multithreading or parallel execution frameworks to process data concurrently.

3. Asynchronous Processing:
Handle long-running tasks asynchronously to improve application responsiveness.

4. Data Partitioning:
Partition data across multiple nodes to distribute the load and improve processing 
speed.

How to use spring batch:
1. Add Dependencies
2. Batch Configuration
3. Implement Reader, Processor, and Writer

### 171. How Client-Side load balancing is different from server-side load balancing in spring boot.
**Answer:**
- Server-side load balancing is managed by a load balancer (a dedicated server or 
appliance) that sits between the clients and the backend servers. It receives client 
requests and distributes them across a pool of backend servers based on 
predefined algorithms.

- Client-side load balancing is managed by the client itself. The client maintains a list 
of server instances and uses an algorithm to select one of these instances for each 
request.


### 172. How to handle failure in microservices environment.
**Answer:**
- Circuit Breaker Pattern
Prevents cascading failures by stopping requests to failing services.
Example: Spring Cloud Circuit Breaker.

- Retry Pattern
Attempts to re-invoke a failed operation.
Example: Spring Retry.

- Bulkhead Pattern
Isolates failures to prevent them from affecting other parts of the system.
Example: Resilience4j Bulkhead.

- Timeouts
Sets limits on the time to wait for a service response.
Example: Configuring timeouts in RestTemplate.

- Service Discovery and Load Balancing
Dynamically discovers services and distributes load evenly.
Example: Eureka, Spring Cloud LoadBalancer.

- Centralized Logging and Monitoring
Aggregates logs and monitors across services for diagnostics.
Example: ELK Stack (Elasticsearch, Logstash, Kibana).

- Health Checks
Regularly checks service status to ensure functionality.
Example: Spring Boot Actuator.

- Fallback Mechanisms
Provides alternative responses when a service fails.
Example: Hystrix (or alternatives like Resilience4j).

Tools and Frameworks:
- Spring Cloud Circuit Breaker
- Spring Retry
- Resilience4j
- RestTemplate
- Eureka
- Spring Cloud LoadBalancer
- ELK Stack
- Spring Boot Actuator
- Hystrix (legacy, replaced by Resilience4j)


### 173. How a block thread causes issues in microservices environment. 
**Answer:**

Resource Contention
- Thread Pool Exhaustion: Limited threads can lead to exhaustion, making the service unresponsive.
- Increased Latency: Blocked threads cause longer response times.
Reduced Throughput
- Slower Processing: Fewer threads handle requests, reducing throughput.
- Backpressure: Upstream services get overwhelmed due to slow downstream 
services.

Cascading Failures
- Service Degradation: Slowdowns propagate across dependent services.
- Service Unavailability: Can lead to timeouts and failures in multiple services.

Resource Utilization
- High Memory Usage: Idle blocked threads consume memory inefficiently.
- Increased Load: More infrastructure resources are required to maintain 
performance.

Error Propagation
- Timeouts and Retries: Cause additional load and potential feedback loops.
- Frequent Failovers: Increased triggers of failover mechanisms like circuit 
breakers.

Debugging Complexity
- Difficult Diagnosis: Hard to pinpoint blocking issues in distributed systems.
- Monitoring Overhead: Requires sophisticated tools for identification and 
monitoring.
Best Practices to Avoid Blocking Issues:
- Asynchronous Processing: Use asynchronous models (e.g., 
CompletableFuture) to handle operations without blocking.
- Reactive Programming: Implement reactive paradigms (e.g., Spring WebFlux) 
for non-blocking request handling.
- Bulkheads and Isolation: Isolate critical components to prevent widespread 
impact.
- Timeouts and Circuit Breakers: Proactively manage and handle blocking 
issues.

### 174. How does a spring application get started?
**Answer:**
Spring application gets started by calling the main() method with 
@SpringBootApplication annotation in the SpringApplication class. This method 
takes a SpringApplicationBuilder object as a parameter, which is used to configure 
the application.
- Once the SpringApplication object is created, the run() method is called.
- Once the application context is initialized, the run() method starts the application’s 
embedded web server.

Code -
```
import org.springframework.boot.SpringApplication; 
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class MyApplication 
{ 
 public static void main(String[] args) {
 SpringApplication.run(MyApplication.class, args);
 }
}
```

### 175. What is an IOC container?
**Answer:**
An IoC (Inversion of Control) Container in Spring Boot is essentially a central 
manager for the application objects that controls the creation, configuration, and 
management of dependency injection of objects (often referred to as beans), also 
referred to as a DI (Dependency Injection) container.

### 176. What is Spring Bean?
**Answer:** 
An object that is managed by the Spring IoC container is referred to as a spring bean. A Spring bean can be any Java object.

### 177. What Do you understand about Spring Data Rest?
**Answer:**
Spring Data REST is a framework that exposes Spring Data repositories as RESTful 
web services. It allows us to expose repositories as REST endpoints with minimal 
configuration by following Spring Data REST Technologies like Spring Data and 
Spring MVC.


### 178. Why is Spring Data REST not recommended in real-world applications?
**Answer:**
Here are the reasons why not to choose Spring Data REST:
- Performance – Performance may not be optimal for very large-scale 
applications.
- Versioning – It can be difficult to version the REST APIs exposed by Spring 
Data REST.
- Relationships – Handling relationships between entities can be tricky with 
Spring Data REST.
- Filtering – There are limited options for filtering the results returned by the 
endpoints.


### 179. How is Hibernate chosen as the default implementation for JPA without any configuration?
**Answer:**
Spring Boot automatically configures Hibernate as the default JPA implementation 
when we add the spring-boot-starter-data-jpa dependency to our project. This 
dependency includes the Hibernate JAR file as well as the Spring Boot auto-configuration for JPA

### 180. What is the difference between Bean Factory and ApplicationContext?
**Answer:**
Application contexts provide a means for resolving text messages, a generic way to load file resources (such as images), they can
publish events to beans that are registered as listeners. In addition, operations on the container or beans in the container, which
have to be handled in a programmatic fashion with a bean factory, can be handled declaratively in an application context. The application context implements MessageSource, an interface used to obtain localized messages, with the actual implementation
being pluggable.