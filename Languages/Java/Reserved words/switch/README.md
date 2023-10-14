# switch

For switch (expr), expr could only be one of the following:
* char / Character
* byte / Byte
* short / Short
* int / Integer
* String
* an enum

These primitive types are not allowed as expr:
* long
* float
* double

## Remember to put break in each case

**Example**:
``````java
public class testSwitch
{
    public static void main(String args[])
    {
        int x = 4;

        switch (x) {
            case 1: System.out.println(x);
            case 2: System.out.println(x);
            case 3: System.out.println(x);
            case 4: System.out.println(x);
            case 5: System.out.println(x);
            default: System.out.println(x);
        }
    }
}
``````

**Result**:
``````
4
4
4
``````

**Reason**: Once a case is matched, and the program has not met a break, it will keep executing the following code, regardless whether the case matches or not util a break shows up.
