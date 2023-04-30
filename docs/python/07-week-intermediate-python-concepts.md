---
sidebar_position: 7
---

# Intermediate Python Concepts

Iterators, generators, decorators, context managers, threading, multiprocessing

- Iterators and generators
- Decorators
- Context managers and the 'with' statement
- Threading and multiprocessing

## 1. Iterators and generators:

- Iterators: objects that implement the iterator protocol (i.e., methods `__iter__()` and `__next__()`)
- Generators: special type of iterator created using a function with the `yield` keyword
  Example (Iterator):

```python
class MyIterator:
    def __init__(self, start, end):
        self.start = start
        self.end = end

    def __iter__(self):
        return self

    def __next__(self):
        if self.start >= self.end:
            raise StopIteration
        self.start += 1
        return self.start - 1

my_iterator = MyIterator(0, 5)
for number in my_iterator:
    print(number)
```

Example (Generator):

```python
def my_generator(start, end):
    while start < end:
        yield start
        start += 1

for number in my_generator(0, 5):
    print(number)
```

## 2. Decorators:

- Functions that modify the behavior of other functions or methods without changing their code
- Can be used to add functionality, logging, or access control to functions or methods
  Example:

```python

def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

## 3. Context managers and the 'with' statement:

- Context managers: objects that define a context for a block of code, usually involving setup and teardown
- The 'with' statement: used to call a context manager, automatically handling setup and teardown
  Example:

```python

class MyContextManager:
    def __enter__(self):
        print("Entering the context")
        return self

    def __exit__(self, exc_type, exc_val, exc_tb):
        print("Exiting the context")

with MyContextManager() as cm:
    print("Inside the context")
```

## 4. Threading and multiprocessing:

- Threading: running multiple threads concurrently, suitable for I/O-bound tasks
- Multiprocessing: running multiple processes concurrently, suitable for CPU-bound tasks
  Example (Threading):

```python
import threading

def print_numbers():
    for i in range(1, 6):
        print(i)

def print_letters():
    for letter in "abcde":
        print(letter)

thread1 = threading.Thread(target=print_numbers)
thread2 = threading.Thread(target=print_letters)

thread1.start()
thread2.start()

thread1.join()
thread2.join()
```

Example (Multiprocessing):

```python
import multiprocessing

def print_numbers():
    for i in range(1, 6):
        print(i)

def print_letters():
    for letter in "abcde":
        print(letter)

process1 = multiprocessing.Process(target=print_numbers)
process2 = multiprocessing.Process(target=print_letters)

process1.start()
process2.start()

process1.join()
process2.join()
```
