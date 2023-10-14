# Comparison of three Factory Patterns

## Similarity

A class delegates object creation to a factory object instead of creating objects directly.

## Characteristic

**Simple Factory**: a factory class is responsible for all object creation.

**Factory Method**: define an interface for creating an object, but let subclasses decide which class to instantiate. The Factory method lets a class defer instantiation it uses to subclasses.

**Abstract Factory**: the client software creates a concrete implementation of the abstract factory and then uses the generic interface of the factory to create the concrete objects that are part of the theme.

## Open-closed Principle

**Simple Factory**: unable to add new products.

**Factory Method**: able to add new products by adding new factories.

**Abstract Factory**: able to add new derived products by adding a factory, however, it is unable to add a completely new product.