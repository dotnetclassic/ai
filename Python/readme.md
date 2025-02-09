# Introduction to Python 🐍

Python is a high-level, interpreted programming language known for its simplicity and readability. It is widely used in web development, data science, automation, AI, and more.

---

## 1. Variables and Data Types
Variables store values in Python. No need to declare types explicitly.

```python
x = 10       # Integer
y = 3.14     # Float
name = "Ali" # String
is_valid = True  # Boolean
```

## 2. Operators
Python supports arithmetic, comparison, logical, bitwise, and assignment operators.

```python
a, b = 5, 2
print(a + b)  # Addition → 7
print(a * b)  # Multiplication → 10
print(a == b) # Comparison → False
print(a > 3 and b < 3) # Logical AND → True
```

## 3. Conditional Statements
Used for decision-making.

```python
age = 18
if age >= 18:
    print("Adult")
elif age > 12:
    print("Teenager")
else:
    print("Child")
```

## 4. Loops
Loops help in iteration.

```python
# For loop
for i in range(5):
    print(i)  # 0 to 4

# While loop
n = 3
while n > 0:
    print(n)
    n -= 1
```


## 5. Functions
Reusable blocks of code.

```python
def greet(name):
    return "Hello, " + name

print(greet("Ali"))  # Output: Hello, Ali
```

## 6. Lists (Arrays)
Ordered, mutable collections.

```python
fruits = ["Apple", "Banana", "Cherry"]
fruits.append("Mango")  # Add item
print(fruits[0])        # Access first item
```

## 7. Tuples
Ordered, immutable collections.

```python
colors = ("Red", "Green", "Blue")
print(colors[1])  # Output: Green
```

## 8. Dictionaries (Key-Value Pairs)
Unordered, mutable collections.


# 🔍 Comparison: List vs. Tuple vs. Dictionary

| Feature       | **List** 📜 | **Tuple** 🎭 | **Dictionary** 📖 |
|--------------|------------|-------------|----------------|
| **Definition** | Ordered, mutable collection | Ordered, immutable collection | Unordered key-value pair collection |
| **Syntax** | `my_list = [1, 2, 3]` | `my_tuple = (1, 2, 3)` | `my_dict = {"name": "Ali", "age": 25}` |
| **Mutability** | ✅ Mutable (can change elements) | ❌ Immutable (cannot change elements) | ✅ Mutable (can change values, but keys must be immutable) |
| **Duplicates** | ✅ Allows duplicates | ✅ Allows duplicates | ❌ No duplicate keys allowed |
| **Indexing** | ✅ Supports indexing and slicing | ✅ Supports indexing and slicing | ✅ Supports key-based access |
| **Performance** | ⏳ Slower than tuples (more memory usage) | ⚡ Faster than lists (less memory usage) | 🚀 Fast for lookups using keys |
| **Use Case** | When you need a dynamic, changeable collection | When you need a fixed, unchangeable collection | When you need a key-value lookup table |
| **Example** | `nums = [1, 2, 3]`<br>`nums.append(4)` → `[1, 2, 3, 4]` | `nums = (1, 2, 3)`<br>`nums[1]` → `2` | `data = {"name": "Ali", "age": 25}`<br>`data["age"]` → `25` |

---

## Example Code:

```python
# List (Mutable)
my_list = [1, 2, 3]
my_list.append(4)  # ✅ Allowed
print(my_list)  # Output: [1, 2, 3, 4]

# Tuple (Immutable)
my_tuple = (1, 2, 3)
# my_tuple[1] = 5  ❌ Not Allowed (Error)
print(my_tuple)  # Output: (1, 2, 3)

# Dictionary (Key-Value Pairs)
my_dict = {"name": "Ali", "age": 25}
my_dict["age"] = 26  # ✅ Allowed (Change value)
print(my_dict)  # Output: {'name': 'Ali', 'age': 26}
```


```python
person = {"name": "Ali", "age": 25}
print(person["name"])  # Output: Ali
```

## 10. Exception Handling
Handles errors gracefully.

```python
try:
    result = 10 / 0
except Exception as e:
    print(f"An error occurred: {e}")  # Output: An error occurred: division by zero
```

## 11. File Handling
Read and write files.

```python
# Write to file
with open("test.txt", "w") as f:
    f.write("Hello, Python!")

# Read from file
with open("test.txt", "r") as f:
    content = f.read()
    print(content)
```

## 12. Classes and Objects (OOP)
Encapsulation of data and methods.

```python
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        return "Hello, " + self.name

p = Person("Ali")
print(p.greet())  # Output: Hello, Ali
```

## 13. Modules and Imports
Reuse code from other files.

```python
import math
print(math.sqrt(16))  # Output: 4.0
```

## 14. Web Scraping (BeautifulSoup)
Extract data from websites.

```python
from bs4 import BeautifulSoup
import requests

url = "https://example.com"
response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")
print(soup.title.text)
```

## 15. NumPy (For Arrays)
Powerful numerical computations.

```python
import numpy as np

arr = np.array([1, 2, 3])
print(arr * 2)  # Output: [2, 4, 6]
```