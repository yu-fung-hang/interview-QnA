# Java Access Modifiers

In this blog, I am going to compare the difference in four Java access modifiers (`public`, `protected`, no modifier, and `private`).

## Q1: Where can they be used?

|    |class|method|variable|interface|
|:---|:---:|:---:|:---:|:---:|
|public|?|?|?|?|
|protected|?|?|?|?|
|no modifier|?|?|?|?|
|private|?|?|?|?|

> **Attention**: Inner class is not considered here.

## Q2: Where can they be accessed?

|    |current class|current package|its subclass in a different package|a different package|
|:---|:---:|:---:|:---:|:---:|
|public|?|?|?|?|
|protected|?|?|? (inheritance) / ? (package)|?|
|no modifier|?|?|?|?|
|private|?|?|?|?|

### Conclusion
1. `public` class / method / variable / interface can be accessed in any case.
2. `private` method / variable could only be accessed within the same class.
3. `no modifier` class / method / variable / interface could only be accessed within the same package.
4. `protected` method / variable:
    1. can be accessed within the same package;
    2. can only be accessed through **inheritance** when two classes are not in the same package.


## Q3: An example of accessing superclass's protected method and variable from an outside package

ClassA.java:

```java
package package1;

public class ClassA
{
    protected String name = "ClassA";

    protected void sayHi() { 
        System.out.println("Hi, I am ClassA!"); 
    }
}
```

ClassC.java:
```java
package package2;

import package1.ClassA;

public class ClassC extends ClassA
{
    public void showName() {
        System.out.println("My father's name: " + super.name);
    }

    public static void main(String[] args) {
        ClassC classC = new ClassC();
        classC.sayHi();
        classC.showName();

//        will show an error here, which means we could not access them directly from an outside package
//        ClassA classA = new ClassA();
//        classA.sayHi();
//        System.out.println(classA.name);
    }
}
```

Result:
```
Hi, I am ClassA!
My father's name: ClassA
```

> ClassC could not pass compilation when we remove all protected statements in ClassA, which indicates the difference between protected and no modifier. 