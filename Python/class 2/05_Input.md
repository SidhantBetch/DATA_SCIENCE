# Input
In Python, input is used to take data from the user during program execution.  
Python uses the input() function to get input from the keyboard.

-----------------------------------------------------------------------------------------------------------------------------------------------

### Syntax
    input("message")

### Example 1: Simple Input
    name = input("Enter your name: ")
    print(name)

#### Example Output
    Enter your name: Kimi
    Kimi

### Example 2: Input with Numbers
By default, input() takes data as string, so we use type casting.
    
    age = int(input("Enter your age: "))
    print(age)

#### Example Output
    Enter your age: 21
    21

### Example 3: Adding Two Numbers
    a = int(input("Enter first number: "))
    b = int(input("Enter second number: "))
    print(a + b)

#### Output Example
    Enter first number: 5
    Enter second number: 3
    8

-----------------------------------------------------------------------------------------------------------------------------------------------

## Important Point
input() always returns string data, so sometimes we convert it using:
- int()
- float()
