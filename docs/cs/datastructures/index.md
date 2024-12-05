## Array
/// define

- **A collection of elements stored at a contiguous memory location.**
- Arrays are of a fixed size. Dynamic arrays (`ArrayList` in Java) create new arrays of an increased length when approaching a pre-determined limit (usually half the size).

///

### Operations

=== "Create"

    ``` java
        int[] arr = new int[5];
        int[] arr = {1,2,3,4,5};
        int[] arr = new int[1];
    ```

=== "Assign"
    ``` java
        arr[0] = 99;
    ```

=== "Access"
    ``` java
        arr[0];
    ```

=== "Modify Element"
    ``` java
        arr[0] = 2;
    ```

=== "Multi-Dimensional Array"
    ``` java
        int[][] arr = new int[5][5];
    ```

## Bag
/// define

- [See Java Implementation](bag.md)

///

### API
``` mermaid
classDiagram
class Bag~Item~{
    +add(Item item): void
    +isEmpty()     : boolean
    +size()        : int
}
```

## Queue
/// define

- **Process by least recently added.**
- FIFO: First In First Out
- [See Java Implementation](queue.md)

///

### API
``` mermaid
classDiagram
class Queue~Item~{
    +enqueue(Item item): void
    +dequeue(): Item
    +isEmpty(): boolean
    +size(): int
}
```

## Stack
/// define

- **Process by most recently added.** 
- LIFO: Last In First Out
- Can be represented in various ways (`Array`/`Linked List`), with `Linked List` being the most common.
- [See Java Implementation](stack.md)

///

### API

``` mermaid
classDiagram
class Stack~Item~{
    +push(Item item): void
    +pop(): Item
    +isEmpty(): boolean
    +size(): int
}
```

## Node
/// define

- **Data structure used to create a `Linked List`.**

///

### API
``` mermaid
classDiagram
class Node{
    +Item item
    +Node next
}
```

## Linked List
/// define

- **A recursive data structure that is either empty (null) or a `node` containing a value and a reference to a linked list.**

///

### Building A Linked List

=== "Create Nodes"
    ``` java
        Node first = new Node();
        Node second = new Node();
        Node last = new Node();
    ```

=== "Initialize Node Values"
    ``` java
        first.item = "to";
        second.item = "be";
        last.item = "or";
    ```

=== "Assign Pointers"
    ``` java
        first.next = second;
        second.next = third;
    ```

### Operations
*Using the 3-node example above*

=== "Insert At The Beginning"
    ``` java
        Node oldFirst = first; 
        first = new Node(); 
        first.item = "not";
        first.next = oldFirst; 
    ```
=== "Remove From The Beginning"
    ``` java
        first = first.next;
    ```
=== "Insert At The End"
    ``` java
        Node oldLast = last;
        last = new Node();
        last.item = "not";
        oldLast.next = last;
    ```
=== "Traverse A Linked List"
    ``` java
        // Please note this only works if the Linked List extends the Iterable interface.
        for (Node x = first; x != null; x = x.next) {
           //process 
        }
    ```

