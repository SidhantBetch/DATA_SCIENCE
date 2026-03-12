# Slicing
Slicing in Python is used to extract a part of a string, list, or sequence.  
It allows you to get a specific range of elements.

### Syntax
    sequence[start : end]
- start → starting index
- end → ending index (not included)

--------------------------------------------------------------------------------------------------------------------------------------------

### Example 1: String Slicing
    text = "Python"
    print(text[0:3])
#### Output:
    Pyt
#### Explanation:
Index 0 to 2 is selected (3 is not included).

### Example 2
    text = "Python"
    print(text[2:5])
#### Output:
    tho

### Example 3: From Beginning
    text = "Python"
    print(text[:4])
#### Output:
    Pyth

### Example 4: To the End
    text = "Python"
    print(text[2:])
#### Output:
    thon

--------------------------------------------------------------------------------------------------------------------------------------------------------------

## Negative Index Slicing
Python also supports negative indexing.

### Example:
    P  y  t  h  o  n
    0  1  2  3  4  5
    -6 -5 -4 -3 -2 -1

### Example code:
    text = "Python"
    print(text[-3:])
#### Output:
    hon
