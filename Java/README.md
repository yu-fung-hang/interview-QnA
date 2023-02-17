# Java Q&A

## Q1: Why is Java platform-independent?

Java compiler transforms source code into bytecode. This bytecode could run in any operating system, and the JVM in each operating system could transform the bytecode into its own machine code which could be executed by the machine.

![](images/platform-independent.png)

image reference: https://www.upgrad.com/blog/why-is-java-platform-independent-language/ 

## Q2: Differences between C++ and Java

1. The C++ compiler compiles and converts the source code into machine code. That's why C++ is faster than Java but not platform-independent ([*reference*](https://www.geeksforgeeks.org/similarities-and-difference-between-java-and-c/));

2. Java is completely object-oriented, while C++ is both object-oriented and procedural. We could define a variable or a method outside of a class in C++, while Java doesn't support this;

3. There is no pointer in Java;

4. Java doesn't support multiple inheritance, but allows a class to implement multiple interfaces;

5. Java provides garbage collection which frees developers from managing memory.

## Q3: Shallow copy vs Deep copy

A new object B is created, and the field values of A are copied over to B.

**shallow copy**: If the field value is a reference to an object (e.g., a memory address), it copies the reference, hence referring to the same object as A does. And if the field value is a primitive type, it copies the value of the primitive type.

**deep copy**: create a new instance for any referenced objects.

## Q4: Abstract class vs Interface

**Similarity**: could not be instantiated

**Differences**:

1. An interface only contains abstract methods, while an abstract class could contain non-abstract methods;

2. A class could implement multiple interfaces, while it could inherit from only one abstract class.

## Q5: JVM vs JRE vs JDK

**JVM**: Java Virtual Machine, responsible for transforming bytecode into machine code.

**JRE**: Java Runtime Environment, a package of everything necessary to run a compiled Java program which includes JVM. It cannot be used to create new programs.

**JDK**: Java Development Kit, the full-featured SDK for Java. It has everything the JRE has, but also the compiler and other tools. It is capable of creating and compiling programs.

Reference: https://stackoverflow.com/questions/1906445/what-is-the-difference-between-jdk-and-jre

## Q6: ArrayList vs Vector

**ArrayList** is not synchronized, while **Vector** is.

## Q7: equals() vs ==

**==** checks whether both objects point to the same memory location while **equals()** compares the values of the two objects.

## Q8: HashMap vs HashTable

|                                               HashMap                                               |                                HashTable                                 |
|:---------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| **NOT synchronized**. It cannot be shared between many threads without proper synchronization code. | **Synchronized**. It is thread-safe and can be shared with many threads. |
|                          one null key and multiple null values are allowed                          |                     no null key or value are allowed                     |
