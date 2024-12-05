# Sorting
/// define 

- The process of rearranging a sequence of objects to put them in some logical order.

///

## Considerations

### Certification

Does the sorting implementation put the array in order, no matter what the initial order is?

The example has a `isSorted(a)` method. It is good practice to include it in every sorting implementation.

### Running Time
    
Consider the basic operations (compares, exchanges, read/write operations on the array).

Develop a hypothesis about the comparative performance and use tools to validate performance.

### Extra Memory
    
Extra memory used is just as important as running time.

Sorting algorithms fall into 2 categories:

1. Sort in place. Use constant or logarithmic extra memory. (Loop index variables or recursive calls)
2. Linear extra memory. (Hold a copy of an array to sort)

### Types of Data

Items must be of the same data type to compare.

By implementing the `Comparable` interface, you can implement `compareTo()`. It must implement a total order as such:

1. _Antisymmetric_: if `v<=w` and `w<=v` then `v=w`
1. _Transitive_: if `v<=w` and `w<=x` then `v<=x`
1. _Total_: either `v<=w` or `w<=v` or both

## Elementary Sorts

### Selection Sort
/// define

- [Java Implementation](selection.md)

///

#### Strategy

1. Find the smallest item in the array and exchange it with the first entry (Itself if the first entry is already the smallest).
2. Find the next (second) smallest item and exchange with the second entry.
3. Continue until complete.

!!! note "Good To Know"
    
    For an array of length n:

    - ~$\frac{n}{2}$ compares
    - `n` exchanges
    
    Running time is insensitive to input. It can take a sorted array as long as an unsorted array because no information is carried to the next operation.
    
    Data movement is minimal. Entries are only moved once (if needed). Worst case `n` exchanges.

### Insertion Sort
/// define

- [Java Implementation](insertion.md)

///

#### Strategy

Items to the left of the current index are sorted, but not in their final position. Items may shift if a smaller item is found later. Sorting is finished when the final item is reached. 

!!! note "Good To Know"
    
    For an array of length `n`:
    
    | Algorithm Analysis | Comparisons      | Exchanges        |
    |--------------------|:----------------:|:----------------:|
    | Average Case       | ~$\frac{n^2}{4}$ | ~$\frac{n^2}{4}$ |
    | Best Case          |        n-1       |         0        |
    | Worst Case         | ~$\frac{n^2}{2}$ | ~$\frac{n^2}{2}$ |

### Shellsort

