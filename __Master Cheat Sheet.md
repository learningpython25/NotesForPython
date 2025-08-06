##### 1. Comments

```python
# Single-line comment

"""
Multi-line comments or docstrings
Good for documentation
"""
```

---

##### 2. Variables

```python
x = 10              # Integer
name = "Alice"      # String
pi = 3.1415         # Float
is_valid = True     # Boolean
nothing = None      # Null value

# Multiple assignment
a, b = 1, 2
a = b = 0           # Both a and b become 0

# Swapping
a, b = b, a
```

---

##### 3. Data Types

#### Numbers

```python
int_val = 5
float_val = 5.0
result = 2 + 3 * 4    # Follows PEMDAS
```

#### Strings

```python
s = "hello"
s[0]                 # 'h'
s[-1]                # 'o'
len(s)               # 5
s.upper()            # 'HELLO'
s.replace("e", "a")  # 'hallo'
"e" in s             # True
```

#### Booleans

```python
True, False
not True             # False
True and False       # False
True or False        # True
```

#### None

```python
x = None
if x is None:
    print("No value")
```

---

##### 4. Collections

#### List

```python
nums = [1, 2, 3]
nums.append(4)
nums[0] = 10
nums.pop()          # removes last element
nums[1:3]           # slicing

# Loop with index
for i, val in enumerate(nums):
    print(i, val)
```

#### Tuple

```python
coords = (10, 20)
x, y = coords       # unpacking
```

#### Set

```python
colors = {"red", "green", "blue"}
colors.add("yellow")
"red" in colors     # True
colors.remove("blue")
```

#### Dictionary

```python
person = {"name": "Alice", "age": 30}
person["name"]      # 'Alice'
person.get("email", "N/A")  # Safe access
for key, value in person.items():
    print(key, value)
```

---

##### 5. Conditional Statements

```python
x = 10

if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")

# Ternary operator
status = "OK" if x > 0 else "Fail"
```

---

##### 6. Loops

#### For loop

```python
for i in range(5):      # 0 to 4
    print(i)

for char in "abc":
    print(char)

for item in [1, 2, 3]:
    print(item)
```

#### While loop

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

#### Loop `else`

```python
# Runs else only if loop is not broken
for i in range(5):
    if i == 6:
        break
else:
    print("Completed without break")

# same for while
```

#### break / continue

```python
for i in range(5):
    if i == 2:
        continue
    if i == 4:
        break
    print(i)
```

---

##### 7. Operators

#### Arithmetic

```python
+  -  *  /   # float division
// % **      # floor division, modulo, power
```

#### Comparison

```python
== != > < >= <=
```

#### Logical

```python
and or not
```

#### Membership

```python
"a" in "cat"           # True
2 not in [1, 3, 5]     # True
```

#### Identity

```python
a = [1]
b = [1]
a == b     # True (values equal)
a is b     # False (different objects)
```

---

##### 8. Functions

```python
def greet(name):
    return f"Hello, {name}"

def add(a, b=0):   # Default argument
    return a + b

def print_all(*args):     # Variable arguments
    for arg in args:
        print(arg)

def show_info(**kwargs):  # Keyword arguments
    print(kwargs["name"])

# Lambda (anonymous function)
square = lambda x: x ** 2
```

---

##### 9. Importing Modules

```python
import math
math.sqrt(16)

from random import randint, choice
randint(1, 10)
```

Other useful ones:

```python
import datetime
import os
import sys
```

---

##### 10. Input & Output

```python
name = input("Enter name: ")
print("Hello", name)

# f-strings (formatted output)
age = 25
print(f"{name} is {age} years old")
```

---

##### 11. Error Handling

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Can't divide by zero")
except Exception as e:
    print("Other error:", e)
else:
    print("No errors!")
finally:
    print("Always runs")
```

---

##### 12. Useful Built-ins

```python
len([1, 2, 3])         # Length
type("abc")           # <class 'str'>
sorted([3,1,2])        # [1, 2, 3]
sum([1, 2, 3])         # 6
max([5, 8, 2])         # 8
min([5, 8, 2])         # 2
range(5)               # [0,1,2,3,4]
list("abc")            # ['a','b','c']
str(100)               # '100'
int("5")               # 5
```
