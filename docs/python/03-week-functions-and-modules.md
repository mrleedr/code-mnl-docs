---
sidebar_position: 3
---

# Functions and Modules

Functions, arguments, scope, lambdas, modules, stdlib

- Defining functions
- Function arguments and return values
- Variable scope
- Lambda functions
- Importing modules
- Standard library modules (e.g., datetime, math, random)

## 1. Defining functions:

- Use the 'def' keyword to define a function
- Functions can have parameters and a return value
  Example:

```python
def greet(name):
    return "Hello, " + name + "!"

message = greet("John")
print(message)  # Output: Hello, John!
```

## 2. Function arguments and return values:

- Positional arguments: matched in order
- Keyword arguments: matched by name
- Default values for arguments
  Example:

```python
def power(base, exponent=2):
    return base ** exponent

result = power(3)  # Uses default exponent value (2)
print(result)  # Output: 9
```

## 3. Variable scope:

- Local variables: defined inside a function and accessible only within that function
- Global variables: defined outside any function and accessible throughout the program
  Example:

```python
x = 10  # Global variable

def display():
    x = 5  # Local variable
    print("Inside function:", x)

display()
print("Outside function:", x)  # Output: Inside function: 5, Outside function: 10
```

##4. Lambda functions:

- Small, anonymous functions defined using the 'lambda' keyword
- Can take any number of arguments but can only have one expression
  Example:

```python
multiply = lambda a, b: a * b
result = multiply(3, 4)
print(result)  # Output: 12
```

## 5. Importing modules:

- Use the 'import' keyword to import a module
- Access functions and variables using the module name and dot notation
  Example:

```python
import math
result = math.sqrt(25)
print(result)  # Output: 5.0
```

## 6. Standard library modules:

- datetime: working with dates and times
- math: mathematical functions
- random: generating random numbers
  Example:

```python
import random
random_number = random.randint(1, 10)
print(random_number)  # Output: a random number between 1 and 10 (inclusive)
```
