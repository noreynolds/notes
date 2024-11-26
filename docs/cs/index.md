# Computer Science

## Basics

### Bits

| Size             | Description               |
| :--------------: | :-----------------------: |
| `Bit`            | 0 or 1                    |
| `Byte`           | 8 bits                    |
| `Megabyte(MB)`   | 1 million or 2^20^ bytes. |
| `Gigabyte(GB)`   | 1 billion or 2^30^ bytes. |


### Java Memory Usage

| Size             | Description               |
| :--------------: | :-----------------------: |
| `int`            | 4 bytes                   |
| `double`         | 8 bytes                   |
| Object reference | 8 bytes                   |
| `Array`          | 24 bytes + memory for each array entry |
| `Object`         | 16 bytes + memory for each instance variable + 8 if inner class (pointer) |


If array entry or instance variable is a reference, add memory (recursively) for referenced object.


## Recursion

- Base Case: A conditional statement as the first statement that has a return.
- Recursive calls must address sub-problems. Meaning they must be smaller problems that converge to the base case.
- Recursive calls __should not overlap__.

### Examples
- Binary Search
- Tree traversal
