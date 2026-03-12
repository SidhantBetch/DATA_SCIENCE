# List
A list in Python is a data type used to store multiple values in a single variable.  
Lists are written using square brackets [ ] and values are separated by commas.

### Example of a List
    numbers = [10, 20, 30, 40]
    print(numbers)
#### Output:
    [10, 20, 30, 40]

----------------------------------------------------------------------------------------------------------------------------------------
    
## List Slicing in Python
List slicing is used to extract a part of a list.

### Syntax
    list[start : end]
- start → starting index
- end → ending index (not included)

### Example
    numbers = [10, 20, 30, 40, 50]
    print(numbers[1:4])
#### Output
    [20, 30, 40]

----------------------------------------------------------------------------------------------------------------------------------------

## Common List Methods
List methods are built-in functions used to perform operations on lists.

Method	|Description	|Example
--------|---------------|--------------
append()	|Add element at end	|list.append(10)
insert()	|Insert element at position	|list.insert(1, 50)
remove()	|Remove element	|list.remove(20)
pop()	|Remove last element	|list.pop()
sort()	|Sort list	|list.sort()
reverse()	|Reverse list	|list.reverse()
count()	|Count element	|list.count(10)
index()	|Find index of element	|list.index(30)

----------------------------------------------------------------------------------------------------------------------------------------

## List with Different Data Types
A list can store different types of data.

### Example:
    data = [10, "Kimi", 3.5, True]
    print(data)
#### Output:
    [10, 'Kimi', 3.5, True]

----------------------------------------------------------------------------------------------------------------------------------------

## Accessing List Elements
Each element has an index starting from 0.

### Example:
    numbers = [10, 20, 30, 40]
    print(numbers[1])
#### Output:
    20

----------------------------------------------------------------------------------------------------------------------------------------

## Changing List Elements
Lists are mutable, meaning their values can be changed.

### Example:
    numbers = [10, 20, 30]
    numbers[1] = 50
    print(numbers)
#### Output:
    [10, 50, 30]

----------------------------------------------------------------------------------------------------------------------------------------

## Common List Operations
### 1. Add element
    numbers.append(60)

### 2. Remove element
    numbers.remove(20)

### 3. Length of list
    print(len(numbers))
