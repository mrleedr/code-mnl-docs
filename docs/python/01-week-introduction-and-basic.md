---
sidebar_position: 1
---

# Introduction and Basics

Python intro, installation, environment, data types, operators, strings, I/O, control structures, loops

- Introduction to Python
- Installing Python and setting up the development environment
- Python data types and variables
- Basic operators
- String manipulation
- Input and output
- Control structures (if, elif, else)
- loops (for, while)

## 1. Introduction to Python:

Python is a versatile, high-level programming language, widely used for web development, data analysis, artificial intelligence, and more. It is known for its readability and ease of learning.

## 2. Installing Python and setting up the development environment:

- Download and install Python from the official website: [https://www.python.org/downloads/](https://www.python.org/downloads/)
- Install a code editor (IDE) such as Visual Studio Code, PyCharm, or Sublime Text.

## 3. Python data types and variables:

- int (integer): whole numbers, e.g., 5, -3
- float (floating-point): decimal numbers, e.g., 3.14, -2.5
- str (string): text, e.g., "Hello, World!"
- bool (boolean): True or False

Example:

```python
age = 25
height = 1.75
name = "John Doe"
is_student = True
```

## 4. Basic operators:

- Arithmetic operators: +, -, \*, /, //, %, \*\*
- Comparison operators: ==, !=, <, >, <=, >=
- Logical operators: and, or, not
  Example:

```python
a = 10
b = 3
result = a + b
print("Addition:", result)  # Output: 13
```

## 5. String manipulation:

- Concatenation: using the + operator
- Repetition: using the \* operator
- Slicing: using [start:end:step] notation
- String methods: upper(), lower(), strip(), split(), join(), etc.
  Example:

```python
word1 = "Hello"
word2 = "World"
sentence = word1 + " " + word2
print(sentence)  # Output: Hello World
```

## 6. Input and output:

- Use input() to get input from the user
- Use print() to display output
  Example:

```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

## 7. Control structures (if, elif, else):

- if: used to check if a condition is True
- elif: used to check additional conditions if the previous ones are False
- else: used when all conditions are False
  Example:

```python
age = int(input("Enter your age: "))
if age < 18:
    print("You are a minor.")
elif age >= 18 and age <= 64:
    print("You are an adult.")
else:
    print("You are a senior.")
```

## 8. Loops (for, while)

- Iterating through a list using a for loop:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

- Iterating through a dictionary using a for loop:

```python
person = {"name": "John", "age": 30, "city": "New York"}
for key, value in person.items():
    print(key, value)
```

- Using a for loop with the range() function:

```python
for i in range(5):
    print(i)
```

- Using a while loop with a condition:

```python
count = 0
while count < 5:
    print(count)
    count += 1
```
