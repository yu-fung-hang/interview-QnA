# super

### Example:
```java
public class Fruit
{
    String name;

    public void setName() {
        this.name = "fruit";
    }
}

class Apple extends Fruit
{
    String name;

    public void setName(String name) {
        this.name = name;
        super.setName();
    }

    public void showName() {
        System.out.println("My name: " + this.name);
        System.out.println("My father's name: " + super.name);
    }

    public static void main(String[] args) {
        Apple a = new Apple();
        a.setName("apple");
        a.showName();
    }
}
```

### Result:
```
My name: apple
My father's name: fruit
```

### Analysis:
We can use `super` in a child class to:
* call its parent class's methods;
* access its parent class's member variables.