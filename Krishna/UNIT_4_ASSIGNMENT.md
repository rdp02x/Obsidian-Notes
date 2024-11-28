### 1. Define Function. Why Do We Need It?

A function is a block of organized, reusable code that performs a specific task. It helps in dividing a large program into smaller, modular parts, making the code more organized, reusable, and easier to maintain.

Need for functions:
- Code reusability
- Modular design
- Makes code easier to debug and maintain

---

### 2. Difference Between User Defined Function and Built-in Function

| User Defined Function                                    | Built-in Function                                                   |
| -------------------------------------------------------- | ------------------------------------------------------------------- |
| Functions created by the user to perform specific tasks. | Predefined functions provided by Python (e.g., `print()`, `len()`). |
| Need to be explicitly defined before use.                | Directly available without any additional definition.               |

---

### 3. What is Recursion? Explain with Example

Recursion is a process where a function calls itself to solve smaller instances of a problem. It breaks down a complex problem into simpler subproblems.

Example:
```python
def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))
```
In this example, the `factorial` function calls itself until it reaches the base case (`n == 1`).

---

### 4. What are Modules in Python? Write Example of User Defined Module

A module in Python is a file containing Python definitions and statements. A module can define functions, classes, and variables that can be imported into other scripts.

Example of User Defined Module (`mymodule.py`):
```python
def greet(name):
    return f"Hello, {name}!"

import mymodule
print(mymodule.greet("Alice"))
```

---

### 5. List Out Methods of `rand` Module. Explain Any Four with Example

Some methods from the `random` module:
1. `random()` – Returns a random float between 0 and 1.
2. `randint(a, b)` – Returns a random integer between `a` and `b`.
3. `choice(seq)` – Returns a random element from a sequence.
4. `shuffle(seq)` – Shuffles the elements of a sequence in place.

Example:
```python
import random

print(random.random())
print(random.randint(1, 10))
print(random.choice([1, 2, 3, 4, 5]))
my_list = [1, 2, 3, 4]
random.shuffle(my_list)
print(my_list)
```

---

### 6. Explain Any Five Mathematical Functions of `math` Module

1. `sqrt(x)` – Returns the square root of `x`.
2. `pow(x, y)` – Returns `x` raised to the power `y`.
3. `ceil(x)` – Returns the smallest integer greater than or equal to `x`.
4. `floor(x)` – Returns the largest integer less than or equal to `x`.
5. `log(x)` – Returns the natural logarithm of `x`.

Example:
```python
import math

print(math.sqrt(16))
print(math.pow(2, 3))
print(math.ceil(4.3))
print(math.floor(4.7))
print(math.log(10))
```

---

### 7. Explain Main Classes of Date and Time Module with One Example

The `datetime` module in Python provides several classes to manipulate date and time.

- `datetime.date`: Represents the date (year, month, day).
- `datetime.time`: Represents time (hour, minute, second).
- `datetime.datetime`: Combines date and time.
- `datetime.timedelta`: Represents the difference between two dates or times.

Example:
```python
from datetime import datetime

now = datetime.now()
print(now)
```

---

### 8. List Out Types of Plots in Matplotlib. Explain Any One with Example

Types of plots:
1. Line Plot
2. Bar Plot
3. Scatter Plot
4. Histogram
5. Pie Chart

Example – Bar Plot:
```python
import matplotlib.pyplot as plt

x = ['A', 'B', 'C']
y = [5, 10, 15]
plt.bar(x, y)
plt.show()
```

---

### 9. What is a Package? How to Create and Import Package. Explain with Example

A package is a collection of Python modules. It is a directory with an `__init__.py` file that allows the directory to be treated as a package.

Steps to create and import a package:
1. Create a directory for the package.
2. Add an `__init__.py` file (can be empty).
3. Add modules in the package directory.
4. Import the package in other Python scripts.

Example:
```python
def greet():
    return "Hello from module1!"

from mypackage import module1
print(module1.greet())
```

---

### 10. Write Down Steps for PIP Installation

1. Download and install Python from the official website (if not installed).
2. Open the command prompt.
3. Run the following command to install a package using PIP:
   ```
   pip install package_name
   ```
4. To verify installation, use:
   ```
   pip --version
   ```

---

### 11. Write a Program Using Function to Find Maximum from Two Numbers

```python
def find_max(a, b):
    if a > b:
        return a
    else:
        return b

print(find_max(10, 20))
```

---

### 12. Create a User Defined Function Which Prints Square of All Even Numbers Between 1 to 5

```python
def square_even():
    for i in range(1, 6):
        if i % 2 == 0:
            print(f"Square of {i}: {i  2}")

square_even()
```

---

### 13. Create a User Defined Function to Return the Count of Numbers Divisible by 5 in Range 1 to 20

```python
def count_divisible_by_5():
    count = 0
    for i in range(1, 21):
        if i % 5 == 0:
            count += 1
    return count

print(count_divisible_by_5())
```