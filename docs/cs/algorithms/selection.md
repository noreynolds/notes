```java

public class Selection
{
    public static void sort(Comparable[] a)
    {
        int n = a.length;
        for (int i = 0; i < n; i++)
        {
            int min = i;
            for (int j = i+1; j < n; j++)
                if (less(a[j], a[min])) min = j;
            exchange(a, i, min)
        }
    }
}

```
