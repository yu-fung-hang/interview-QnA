# Other Modifiers

## static

**static variable** or **class variable**:
* belongs to its class and it is initialized only once at the start of the execution
* cannot be declared inside a method

**static method**: 
* belongs to its class rather than an instance of its class
* could be called without creating an instance
* cannot call a non-static method inside a static method
* cannot access member variables inside a static method

## final

**final variable**: this variable cannot be assigned a new value again (cannot point to another reference, but modifying the current reference is allowed).

**final method**: this method cannot be overridden by its subclasses.

**final class**: this class cannot be inherited.

## abstract

**abstract class**:
* cannot be instantiated;
* could consist of both abstract and non-abstract methods;
* must become abstract when there are abstract methods inside;
* could contain no abstract method.

**abstract method**:
* a subclass must implement all abstract methods of its superclass unless it is also an abstract class;
* example: abstract void methodName();

## synchronized

to be continued

## transient

to be continued

## volatile

to be continued