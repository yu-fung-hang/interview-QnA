# Spring

## Inversion of Control (IoC)

**a programming principle**: objects do not create other objects on which they rely to do their work. Instead, they get the objects they need from an outside source

**advantage**: by removing a client's knowledge of how its dependencies are implemented, programs become more reusable, testable and maintainable

## Dependency Injection

a technique in which an object receives other objects that it depends on (**dependencies**)

**client**: the object that receives dependencies

**service**: the injected object

**injector**: the code that passes the service to the client

### Types

There are three types of Dependency Injection, which are **constructor injection**, **field injection**, and **setter injection**.

### Why constructor injection is advocated

1. Implement application components as immutable objects;
2. Ensure that required dependencies are not null;
3. Constructor-injected components are always returned to client (calling) code in a fully initialized state.

## Aspect of Programming

There are two modes which are **proxy** and **aspectj**.

**proxy mode**:
1. The @Transactional annotation should only be applied to methods with public visibility;
2. A method within the target object calls some other method of the target object, won't lead to an actual transaction at runtime even if the invoked method is marked with @Transactional;
3. @Transactional does not work for static methods since proxies could not be created.

Reference: https://docs.spring.io/spring-framework/docs/3.0.0.M3/reference/html/ch11s05.html

## Spring Web MVC

**DispatcherServlet**: the front controller of the framework which is responsible for delegating control to various interfaces during the execution of an HTTP request

**HandlerMapping**: select handlers that handle incoming requests

**HandlerAdapter**: execute handler execution chain

**HandlerExecutionChain**: consist of handler object and any handler interceptors

**ViewResolver**: selecting a View based on a logical name (not strictly required)

**View**: responsible for returning a response to the client

### Flow

![](images/mvc.png)

Reference: https://www.upgrad.com/blog/wp-content/uploads/2020/08/RequestLifecycle.png



## Spring Boot

1. Make it easy to create stand-alone, production-grade Spring based Applications that you can "just run";
2. Embed Tomcat & Jetty directly so there is no need to deploy WAR files;
3. No requirement for XML configuration.
