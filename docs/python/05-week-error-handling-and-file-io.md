---
sidebar_position: 5
---

# Error Handling and File I/O

Exceptions, try-except, file I/O, CSV, JSON

- Exceptions and exception handling
- The try-except-else-finally block
- Creating, reading, and writing files
- Working with CSV and JSON files

## 1. Exceptions and exception handling:

- Exceptions: events that occur when an error is encountered during program execution
- Handling exceptions using try-except blocks to prevent program termination
  Example:

```python

try:
    num = int(input("Enter a number: "))
except ValueError:
    print("Invalid input. Please enter a number.")
```

## 2. The try-except-else-finally block:

- try: code that may raise an exception
- except: code that handles the exception
- else: code that runs if no exception is raised
- finally: code that always runs, regardless of whether an exception was raised or not
  Example:

```python
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("Invalid input. Please enter a number.")
else:
    print("You entered:", num)
finally:
    print("Program completed.")
```

## 3. Creating, reading, and writing files:

- Use the 'open()' function to open a file with specified mode (e.g., 'r', 'w', 'a')
- Use the 'read()', 'write()', 'readline()', and 'readlines()' methods to read and write data
- Close the file using the 'close()' method
  Example:

```python
file = open("example.txt", "w")
file.write("Hello, World!")
file.close()
```

## 4. Working with CSV and JSON files:

- Use the 'csv' module to read and write CSV files
- Use the 'json' module to read and write JSON files
  Example (CSV):

```python

import csv

with open("example.csv", "w", newline="") as csvfile:
    writer = csv.writer(csvfile)
    writer.writerow(["Name", "Age", "City"])
    writer.writerow(["John", 25, "New York"])
    writer.writerow(["Jane", 28, "Los Angeles"])
```

Example (JSON):

```python
import json

data = {
    "name": "John",
    "age": 25,
    "city": "New York"
}

with open("example.json", "w") as jsonfile:
    json.dump(data, jsonfile)
```
