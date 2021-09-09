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

## Q4 Can we disable the default **web server** in spring boot?
Answer: **YES**,
in **application.properties** - #####spring.main.web.application.type = none


test

## Test 

Testing 2, **Block quotes** _block quotes_

<mark> Highlight </mark>

* Test 1
* Test 1
* Test 1
* Test 1
* Test 1
* Test 1
* Test 1

1. OBJECT 1

**[⬆ Back to Top](#Spring-Boot)**


