# Tuple
A tuple is a collection data type used to store multiple values in a single variable.  
Tuples are written inside parentheses ( ) and the values are separated by commas.  

The main feature of a tuple is that it is immutable, which means its values cannot be changed after creation.

### Example of a Tuple
    numbers = (10, 20, 30, 40)
    print(numbers)
### Output
    (10, 20, 30, 40)

--------------------------------------------------------------------------------------------------------------------------------------------

## Accessing Tuple Elements
Tuple elements are accessed using index numbers starting from 0.

### Example:
    numbers = (10, 20, 30, 40)
    print(numbers[1])
#### Output
    20

--------------------------------------------------------------------------------------------------------------------------------------------

## Tuple with Different Data Types
    data = (10, "Kimi", 3.5, True)
    print(data)
### Output
    (10, 'Kimi', 3.5, True)

--------------------------------------------------------------------------------------------------------------------------------------------

## Tuple Methods
Tuples have very few methods because they cannot be modified.

Method	|Description	|Example
--------|-------------|-----------
count()	|Counts how many times a value appears	|t.count(10)
index()	|Returns the index of a value	|t.index(30)

### Example Program
    t = (10, 20, 30, 10)
    
    print(t.count(10))
    print(t.index(30))
#### Output
    2
    2
### Explanation:
- count() shows how many times 10 appears
- index() shows the position of 30
