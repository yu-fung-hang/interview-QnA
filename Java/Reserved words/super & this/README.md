# super & this

## super

### Example:
```java
public class Fruit
{
    String name;

    public Fruit() { }

    public Fruit(String name) {
        this.name = name;
    }

    public void setName() {
        this.name = "fruit";
    }
}

class Apple extends Fruit
{
    public String name;

    public Apple() {
        super();
    }

    public Apple(String name) {
        super("fruit");
        this.name = name;
    }

    public void setName(String name) {
        this.name = name;
        super.setName();
    }

    public void showName() {
        System.out.println("My name: " + this.name);
        System.out.println("My superclass's name: " + super.name);
    }

    public static void main(String[] args) {
        Apple a = new Apple();
        a.setName("apple");
        
//        Apple a = new Apple("apple");
        a.showName();
    }
}
```

### Result:
```
My name: apple
My superclass's name: fruit
```

### Analysis:
We can use `super` in a subclass to:
* call its superclass's methods;
* access its superclass's member variables.

## this
Access current class's member variables.