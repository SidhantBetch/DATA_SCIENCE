# Type Conversion
Type Conversion in Python means changing one data type into another data type.  
For example, converting a string to an integer or an integer to a float.

## Types of Type Conversion in Python
### 1. Implicit Type Conversion
This conversion is done automatically by Python.

#### Example
    a = 5      # integer
    b = 2.5    # float
    c = a + b
    print(c)

#### Output:
    7.5
Here Python automatically converts the integer (5) into float (5.0).

### 2. Explicit Type Conversion
This conversion is done manually by the programmer using functions.

#### Common Functions
Function	|Use
----------|------------
int()	|Convert to integer
float()	|Convert to float
str()	|Convert to string
bool()	|Convert to boolean

#### Examples
Convert string to integer

        x = "10"
        y = int(x)
        print(y)


Convert integer to float
  
  a = 5
  b = float(a)
  print(b)


Convert number to string

    num = 20
    text = str(num)
    print(text)
