# break & continue

## break

jump out of a loop

### How to jump out of multiple loops

``````java
public class testBreak
{
    public static void main(String[] args)
    {
        block:
        for(int i=0; i<5; i++)
        {
            for(int j=0; j<5; j++)
            {
                if(j >= 4)
                { break block; }

                System.out.println(j);
            }
        }

        System.out.println("Outside of two loops");
    }
}
``````

#### Result
``````
0
1
2
3
Outside of two loops
``````

## continue

break one iteration