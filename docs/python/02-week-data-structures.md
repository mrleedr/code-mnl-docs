---
sidebar_position: 2
---

# Data Structures

Lists, tuples, sets, dictionaries, comprehensions

- Lists
- Tuples
- Sets
- Dictionaries
- List comprehensions

## 1. Lists:

- Ordered, mutable collection of items
- Items can be of different data types
- Created using square brackets [ ]
  Example:

```python

fruits = ["apple", "banana", "orange"]
fruits.append("grape")
print(fruits)  # Output: ['apple', 'banana', 'orange', 'grape']
```

## 2. Tuples:

- Ordered, immutable collection of items
- Items can be of different data types
- Created using parentheses ( )
  Example:

```python

colors = ("red", "green", "blue")
print(colors[1])  # Output: green
```

## 3. Sets:

- Unordered, unique collection of items
- Items can be of different data types
- Created using curly braces { }
  Example:

```python

numbers = {1, 2, 2, 3, 4, 4, 5}
print(numbers)  # Output: {1, 2, 3, 4, 5}
```

## 4. Dictionaries:

- Unordered collection of key-value pairs
- Keys must be unique and of immutable data types
- Created using curly braces { } with key-value pairs
  Example:

```python
student = {"name": "John", "age": 22, "course": "Computer Science"}
student["grade"] = "A"
print(student)  # Output: {'name': 'John', 'age': 22, 'course': 'Computer Science', 'grade': 'A'}
```

## 5. List comprehensions:

- Concise way to create a list using a single line of code
  Example:

```python
numbers = [1, 2, 3, 4, 5]
squares = [x * x for x in numbers]
print(squares)  # Output: [1, 4, 9, 16, 25]
```
