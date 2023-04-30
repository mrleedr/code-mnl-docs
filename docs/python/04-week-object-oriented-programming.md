---
sidebar_position: 4
---

# Object-Oriented Programming

Classes, objects, inheritance, encapsulation, polymorphism, built-ins

- Classes and objects
- Inheritance
- Encapsulation
- Polymorphism
- Python's built-in classes and methods

## 1. Classes and objects:

- Classes: a blueprint for creating objects
- Objects: instances of a class with their own properties and methods
  Example:

```python

class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print("Woof!")

my_dog = Dog("Buddy", "Golden Retriever")
my_dog.bark()  # Output: Woof!
```

## 2. Inheritance:

- Allows a class to inherit properties and methods from a parent class
- Use the 'super()' function to call the parent class's method
  Example:

```python

class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("Some generic animal sound")

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)
        self.breed = breed

    def speak(self):
        print("Woof!")

my_dog = Dog("Buddy", "Golden Retriever")
my_dog.speak()  # Output: Woof!
```

## 3. Encapsulation:

- Bundling of data (attributes) and methods within a class
- Using private attributes (by convention, prefix with an underscore) and providing getter and setter methods
  Example:

```python

class Person:
    def __init__(self, name, age):
        self._name = name
        self._age = age

    def get_name(self):
        return self._name

    def set_name(self, name):
        self._name = name

person = Person("John", 30)
person.set_name("Jane")
print(person.get_name())  # Output: Jane
```

## 4. Polymorphism:

- The ability of different classes to share the same method name and functionality
  Example:

```python

class Bird:
    def fly(self):
        print("I can fly!")

class Airplane:
    def fly(self):
        print("I can fly too!")

def start_flying(obj):
    obj.fly()

bird = Bird()
airplane = Airplane()

start_flying(bird)      # Output: I can fly!
start_flying(airplane)  # Output: I can fly too!
```

## 5. Python's built-in classes and methods:

- Examples: str, list, dict, tuple, set
- Using built-in methods like len(), max(), min(), etc.
  Example:

```python
my_list = [1, 2, 3, 4, 5]
list_length = len(my_list)
print(list_length)  # Output: 5
```
