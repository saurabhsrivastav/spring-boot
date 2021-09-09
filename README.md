# Spring Boot

## Interview Questions

No | Description
:-- | :-- |
1. [What is Spring Boot? Why did you use Spring boot in Project ? Why Not Spring ?](#Q1)
2. [What is RAD](#Q2-What-is-RAD?)
3. [Test](#test)


## Q1 What is Spring Boot? Why did you use Spring boot in Project ? Why NOT Spring ?

Answer:
* Spring boot is open-source and it's spring module which gives us production ready app feature  
* It's used for **RAD** (Rapid Application development) build using spring framework with extra support of auto-configuration and embadded application server (tomcat, jetty)  
* It helps us to create efficient fast stand-alone application which you can just run basicaly removes lots of configurations and dependency    
* We have to concentrate only on business logic, forget about configuration


## Q2 What is RAD?
Answer: Spring boot modified waterfal model to RAD which focus on developing software in a short span of time.

**Phase of RAD**
* Step 1: Business Modeling
* Step 2: Data Modeling
* Step 3: Rrocess Modeling
* Step 4: Application Generation
* Step 5: Testing and Turnover

## Q3 Is it possible to change the **port** of embedded tomcat server in spring boot?
Answer: **YES**, default tomcat server port is 8080,
in **application.properties** - server.port = 8091

## Q4 Can we override or replace the embedded **tomcat server** in spring boot?
Answer: **YES**,
in pom.xml exclude the dependency ~spring-boot-starter-tomcat~
```java
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
</dependency>
<exclusion>
	<groupId>org.springframework.boot</groupId>
	<artifactId><spring-boot-starter-tomcat></artifactId>
</exclusion>
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-jetty</artifactId>
</dependency>
```

## Q5 Can we disable the default **web server** in spring boot?
Answer: **YES**, 
📌 in ***application.properties*** [spring.main.web.application.type = none]

## Q6 How to disable auto-configuration in spring boot?
Answer: 
**@EnableAutoConfiguration(exclude={DataSourceAutoConfiguration.class})**  
OR  
in **application.properties** 
- spring.autoconfigure.exclude = \org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration

## Q7 How to use a property defined in application.properties file into your .java class or in controller?
Answer: 
**@Value("${custom.value}")**  
private String customval;

## Q8 Explain @RestController annotation?
Answer: 
- @RestController used to create Restful Controller 
- It adds @Controller + @Responsebody or can save combination of these two annotation
- It Convert response o JSON/XML

## Q9 Difference between @RestController and @Controller
Answer:  

@Controller | @RestController
:-- | :-- |
@controller map of the model object to view or template and makes it human readable | @RestController returns the object and object data is directly written into HTTP response as JSON/XML  

## Q10 Difference between @GetMapping and @RequestMapping
Answer:  

@GetMapping | @RequestMapping
:-- | :-- |
can be use if knows the request is get only, it help to improve clarity of request | can be used with GET/POST/PUT/DELETE  

## Q11 How to profile your application?
Answer:  
in **application.properties** 
_abc_ 
<mark> spring.profile.active = dev/test/prod  </mark>
OR  
If there are three .properties file for each environment then there should be three .properties file    
DEV -- properties-dev.properties  
TEST -- properties-test.properties  
PROD-- properties-prod.properties  

## Test 

**[⬆ Back to Top](#Spring-Boot)**
