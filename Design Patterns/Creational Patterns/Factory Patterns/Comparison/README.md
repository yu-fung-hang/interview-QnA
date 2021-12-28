# Comparison of three Factory Patterns

## Similarity

A class delegates object creation to a factory object instead of creating objects directly.

## Characteristic

**Simple Factory**: a factory class is responsible for all object creation.

**Factory Method**: define an interface for creating an object, but let subclasses decide which class to instantiate. The Factory method lets a class defer instantiation it uses to subclasses.

**Abstract Factory**: define an interface for creating a number of objects, and its implementation would create those objects in its own way.

## Open¨Cclosed Principle

**Simple Factory**: unable to add new products.

**Factory Method**: able to add new products by adding new factories.

**Abstract Factory**: able to add new derived products by adding a factory, however, it is unable to add a completely new product.