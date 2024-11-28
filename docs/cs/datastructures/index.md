## Array

A collection of elements stored at a contiguous memory location.

Fixed size

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
Process by least recently added.

FIFO: First In First Out

### Operations
- Queue (Insert)
- Enqueue (Remove)
- Iterate
- isEmpty

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
Process by most recently added.

LIFO: Last In First Out

Can be represented in various ways (`Array`/`Linked List`), with `Linked List` being the most common.

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
Data structure used to create a `linked list`.

``` mermaid
classDiagram
class Node{
    +Item item
    +Node next
}
```

## Linked List
A recursive data structure that is either empty (null) or a "node" containing a value and a reference to a linked list.

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

