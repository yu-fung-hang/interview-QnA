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

