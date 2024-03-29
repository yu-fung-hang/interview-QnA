# Access Modifiers

In this blog, I am going to compare the differences in four Java access modifiers (**public**, **protected**, **no access modifier**, and **private**).

## Q1: Where can they be used?

|    |class|method|variable|interface|
|:---|:---:|:---:|:---:|:---:|
|public|✔|✔|✔|✔|
|protected|❌|✔|✔|❌|
|no access modifier|✔|✔|✔|✔|
|private|❌|✔|✔|❌|

> **Attention**: Inner class is not considered here.

## Q2: Where can they be accessed?

|    |current class|current package|its subclass in a different package|a different package|
|:---|:---:|:---:|:---:|:---:|
|public|✔|✔|✔|✔|
|protected|✔|✔|✔ (inheritance) / ❌ (package)|❌|
|no access modifier|✔|✔|❌|❌|
|private|✔|❌|❌|❌|

### Conclusion
1. **public** class / method / variable / interface can be accessed in any case.
2. **private** method / variable could only be accessed within the same class.
3. **no access modifier** class / method / variable / interface could only be accessed within the same package.
4. **protected** method / variable:
    1. can be accessed within the same package;
    2. can only be accessed through **inheritance** when the two classes are not in the same package.


## Q3: An example of accessing superclass's protected methods and variables from an outside package

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

ClassB.java:
```java
package package2;

import package1.ClassA;

public class ClassB extends ClassA
{
    public void showName() {
        System.out.println("My superclass's name: " + super.name);
    }

    public static void main(String[] args) {
        ClassB classB = new ClassB();
        classB.sayHi();
        classB.showName();

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
My superclass's name: ClassA
```

> ClassB could not pass compilation when we remove all protected statements in ClassA, which indicates the difference between protected and no access modifier.

## Q4: Inheritance rules (override superclass's method)

* If a method is set to be **public** in the superclass, its subclass should also set it to be **public**;
* If a method is set to be **protected** in the superclass, its subclass should set it to be either **public** or **protected**;
* If a method is not assigned any access modifier in the superclass, its subclass should set it to be **public** / **protected** / **no access modifier**;
* If a method is set to be **private** in the superclass, this method could not be inherited by its subclasses.