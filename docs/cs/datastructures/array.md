``` java
public class Stack<Item>
{
    private Node first;  // top of the stack
    private int n;      // number of items in stack
    
    private class Node
    {
        Item item;
        Node next;
    }
    public boolean isEmpty()    { return first == null; }
    public int size()           { return n; }

    public void push(Item item)
    {   // Add item to top of stack
        Node oldFirst = first;
        first = new Node();
        first.item = item;
        first.next = oldFirst;
        n++;
    }

    public Item pop()
    {   // Remove item from top of stack
        Item item = first.item;
        first = first.next;
        n--;
        return item;
    }
}
```
