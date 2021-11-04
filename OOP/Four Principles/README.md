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

**static polymorphism**:

1. Method Overloading: several methods with the same name can be defined in the same class, however, their parameters should be different(number, sequence & type);
2. Operator Overloading;
3. Generics: one or more types are not specified by name but by abstract symbols that can represent any type.

**dynamic polymorphism**:

Overriding: the implementation in the subclass overrides that in the superclass by providing a method that has same name, same parameters, and same return type as the method in the superclass.