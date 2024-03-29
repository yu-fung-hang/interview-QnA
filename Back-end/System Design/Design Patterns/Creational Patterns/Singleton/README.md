# Singleton (object scope)

* Ensure that a class only has one instance;
* The singleton class creates an instance itself, and disallows other classes to create its instance by providing a private constructor;
* The singleton class provides a public method for other classes to get its instance.

## Class Diagram

![](images/singleton.png)

Reference: https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Singleton_UML_class_diagram.svg/330px-Singleton_UML_class_diagram.svg.png

## Eager Instantiation (❌ lazy loading)

```java
class MySingleton
{
    private static MySingleton instance = new MySingleton();

    private MySingleton(){}

    public static MySingleton getInstance()
    { return instance; }
}
```

## Static Inner Class (✔ lazy loading)

``````java
class MySingleton
{
    private static class SingletonHolder
    { private static MySingleton instance = new MySingleton(); }

    private MySingleton() {}

    public static MySingleton getInstance()
    { return SingletonHolder.instance; }
}
``````