# Why is String an immutable class?

An example that illustrates the difference between String and StringBuffer:

```java
public class testString
{
    public static void modifyString(String s)
    {
        s = "modified";
    }

    public static void modifyStringBuffer(StringBuffer sb)
    {
        sb.append("modified");
    }

    public static void main(String args[])
    {
        String s = "original";
        modifyString(s);

        StringBuffer sb = new StringBuffer();
        sb.append("StringBuffer sb: ");
        modifyStringBuffer(sb);

        System.out.println("String s: " + s);
        System.out.println(sb.toString());
    }
}
```

**Result**
```
String s: original
StringBuffer sb: modified
```

**Reason**
* String is an immutable class. To be continued