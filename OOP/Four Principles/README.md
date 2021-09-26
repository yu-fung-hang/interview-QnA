# Four Principles

Four principles in Object-Oriented Programming are **Encapsulation**, **Abstraction**, **Inheritance** and **Polymorphism**.

## Encapsulation

Protect classes / methods / variables from unwanted access.

## Inheritance

The procedure in which one class inherits the attributes and methods of another class:

1. Superclass defines the common attributes and methods which could be inherited by its subclasses;

2. A subclass could override its superclass's methods and add its own attributes and methods.

## Abstraction

The difference between inheritance and abstraction is that an abstract class could not be instantiated. Its subclasses should implement all abstract methods of this class, unless they are also abstract classes. An abstract method could not have a body.

## Polymorphism

A single action could be performed in different ways in different contexts.

**Forms**:

1. **override** and **overload**:
    1. **override**: a subclass could override a superclass's method based on its own requirement. 
    2. **overload**: a class contains multiple methods with the same name, but their parameters are different (number, type & sequence).
    
2. **interface**: an interface could be implemented by many classes by their own way.

3. **abstract class** and **abstract method**: see [Abstraction](#Abstraction) above.
