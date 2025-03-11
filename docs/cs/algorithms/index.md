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

### Templates
The following code blocks are used in the sorting algorithm examples below.

#### Less
```java
private static boolean less(Comparable v, Comparable w)
{ return v.compareTo(w) < 0; }
```

#### Exchange
```java
private static boolean exchange(Comparable[] a, int i, int j)
{ Comparable t = a[i]; a[i] = a[j]; a[j] = t; }
```


### Insertion Sort
/// define

- [Java Implementation](insertion.md)

///

#### Strategy
1. Start a loop from `1` to `n`;
2. Compare the current item (`j`) with the previous item (`j-1`). 
    2. If `j` is smaller, exchange items and repeat the process. 

Items to the left of the current index are sorted, but not in their final position. Items may shift if a smaller item is found later. Sorting is finished when the final item is reached. 

!!! note "Good To Know"
    
    Very efficient for partially sorted arrays.

    For an array of length `n`:
    
    | Algorithm Analysis | Comparisons      | Exchanges        |
    |--------------------|:----------------:|:----------------:|
    | Average Case       | ~$\frac{n^2}{4}$ | ~$\frac{n^2}{4}$ |
    | Best Case          |        n-1       |         0        |
    | Worst Case         | ~$\frac{n^2}{2}$ | ~$\frac{n^2}{2}$ |

    Insertion sort can be improved by shortening the inner loop to move the larger entries to the right one position instead of doing exchanges. This would cut array accesses in half.

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

### Shellsort
/// define

- [Java Implementation](shell.md)

///

#### Strategy

An extension of insertion sort. 

Create an _h_-sorted array. An _h_-sorted array is _h_ independent sorted subsequences. If _h_ is 5, this means there are 5 subsequences within the array that are each sorted. When _h_ equals 1, the sorting operation is complete. 

The implementation uses the sequence of decreasing values $\frac{1}{2}(3^k-1)$, starting at the smallest increment greater than or equal to $\lfloor$_n_/3$\rfloor$ and decreasing to 1.

## Mergesort

> The algorithms discussed in this section are based on _merging_. the combination of 2 ordered arrays into one larger ordered array. 

An array is sorted by:

1. Dividing into two halves
1. Sorting the two halves (recursively)
1. Merging results

### Abstract In-Place Merge
/// define

- [Java Implementation](mergesort_in_place.md)

///

#### Strategy
The straightforward approach. Merge two disjoint ordered orders into a third array.

1. Create an output array
1. Choose the smallest remaining item form the two input arrays
1. Add the chosen item to the output array.

#### Faults
When size increases, creating an ouput array for every merge becomes expensive.


### Top-Down Mergesort
/// define

- [Java Implementation](top_down_mergesort.md)

////


