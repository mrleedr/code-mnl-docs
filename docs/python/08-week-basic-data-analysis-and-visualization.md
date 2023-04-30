---
sidebar_position: 8
---

# Basic Data Analysis and Visualization

Data analysis intro, NumPy, Pandas, Matplotlib

- Introduction to data analysis with Python
- NumPy basics
- Pandas basics
- Data visualization with Matplotlib

## 1. Introduction to data analysis with Python:

- Python libraries for data analysis: NumPy, pandas, Matplotlib
- NumPy: a library for working with arrays and performing mathematical operations
- Pandas: a library for data manipulation and analysis
- Matplotlib: a library for data visualization

## 2. NumPy basics:

- Creating NumPy arrays
- Array attributes and methods (shape, size, dtype, etc.)
- Basic array operations (addition, subtraction, multiplication, etc.)
- Indexing, slicing, and iterating through arrays
  Example:

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = a + b
print(c)  # Output: [5 7 9]
```

## 3. Pandas basics:

- Creating and manipulating data using pandas DataFrame and Series objects
- Loading and saving data with pandas
- Data exploration and manipulation with pandas (sorting, filtering, selecting data, handling missing values, grouping, and aggregation)
  Example:

```python
import pandas as pd

data = {"Name": ["John", "Jane", "Alex"], "Age": [25, 28, 30]}
df = pd.DataFrame(data)
print(df)
```

## 4. Data visualization with Matplotlib:

- Creating different types of plots (line plots, scatter plots, bar plots, etc.)
- Customizing plots (labels, titles, colors, markers, etc.)
- Saving plots to files
  Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y, marker='o', linestyle='--', color='r', label='Line')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot Example')
plt.legend()
plt.savefig('line_plot.png')
plt.show()
```
