# Conditional Statment
A conditional statement in Python is used to make decisions in a program based on a condition.  
It checks whether a condition is true or false and executes code accordingly.

---------------------------------------------------------------------------------------------------------------------------------------------------

## Types of Conditional Statements in Python
### 1. if Statement
Executes code only if the condition is true.

#### Syntax
    if condition:
        statement
        
#### Example
    age = 18
    
    if age >= 18:
        print("You can vote")
##### Output:
    You can vote

### 2. if-else Statement
Executes one block if the condition is true, otherwise another block.

#### Syntax
    if condition:
        statement1
    else:
        statement2

#### Example
    age = 16
    
    if age >= 18:
        print("You can vote")
    else:
        print("You cannot vote")
##### Output:
    You cannot vote

### 3. if-elif-else Statement
Used when multiple conditions are checked.

#### Syntax
    if condition1:
        statement1
    elif condition2:
        statement2
    else:
        statement3

#### Example
    marks = 75
    
    if marks >= 90:
        print("Grade A")
    elif marks >= 60:
        print("Grade B")
    else:
        print("Grade C")
##### Output:
    Grade B
