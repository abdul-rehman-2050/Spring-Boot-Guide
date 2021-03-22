# Spring-Boot-Guide
Spring Boot guide and resources for Starter

# Create Project from Curl Command Line

```
$ sudo apt-get install unzip
$ mkdir blog && cd blog
$ curl https://start.spring.io/starter.zip -d language=kotlin -d dependencies=web,mustache,jpa,h2,devtools -d packageName=com.example.blog -d name=Blog -o blog.zip -d type=gradle-project

$ gralew bootRun --args='--server.port=8888'

$./mvnw spring-boot:run -Pprod

```


# Basic Dependency 
 List of Dependency I have to add for this tutorial.
 ```
“web”, “mysql”, “jpa”, “security”, “Actuator” , “DevTool” and “Lombok” as Dependency.
Web --> Starter for building web application, including RESTful, Spring MVC. And Tomcat as the default embedded container.
mysql --> JDBC Type driver for MySQL
jpa --> Starter for using Spring Data JPA with Hibernate
security --> Starter for using Spring Security
Actuator --> Starter for using Spring Boot's Actuator which provides production ready features to help you monitor and manage your application
DevTool --> additional set of tools that can make the application development experience a little more pleasant
Lombok --> Lombok is used to reduce boilerplate code for model/data objects, e.g., it can generate getters and setters for those object automatically by using Lombok annotations. The easiest way is to use the @Data annotation.
```


# Demo Class for Hello World!

```java
package com.demo;

import org.springframework.boot.*;
import org.springframework.boot.autoconfigure.*;
import org.springframework.stereotype.*;
import org.springframework.web.bind.annotation.*;

@RestController
@EnableAutoConfiguration
public class DemoApplication {

    @RequestMapping("/")
    String home() {
        return "Hello World!";
    }

    public static void main(String[] args) throws Exception {
        SpringApplication.run(DemoApplication.class, args);
    }

}


```
