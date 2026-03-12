# List
A list in Python is a data type used to store multiple values in a single variable.  
Lists are written using square brackets [ ] and values are separated by commas.

### Example of a List
    numbers = [10, 20, 30, 40]
    print(numbers)
#### Output:
    [10, 20, 30, 40]

## List with Different Data Types
A list can store different types of data.

### Example:
    data = [10, "Kimi", 3.5, True]
    print(data)
#### Output:
    [10, 'Kimi', 3.5, True]

## Accessing List Elements
Each element has an index starting from 0.

### Example:
    numbers = [10, 20, 30, 40]
    print(numbers[1])
#### Output:
    20

## Changing List Elements
Lists are mutable, meaning their values can be changed.

### Example:
    numbers = [10, 20, 30]
    numbers[1] = 50
    print(numbers)
#### Output:
    [10, 50, 30]

## Common List Operations
### 1. Add element
numbers.append(60)

### 2. Remove element
numbers.remove(20)

3. Length of list
print(len(numbers))
