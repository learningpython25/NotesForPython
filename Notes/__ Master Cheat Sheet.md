### 1. Basics
**Comments**
```python
# - single Line comments
# This is a single-line comment

'''
This is a multi-line comment
You can also use triple double quotes like this:
"""
Multi-line docstring or comment
"""
'''
```

**Variables and Data Types**
```python
x = 10         # Integer
name = "Alice" # String
pi = 3.14      # Float
is_ready = True # Boolean
```

**Input/Output**
```python
name = input("Enter your name: ")
print("Hello", name)

```

### 2. Data Types

**Numbers**
```python
a = 5           # int
b = 3.14        # float
c = 2 + 3j      # complex
```

**Boolean**
```python
is_active = True
is_closed = False

print(type(is_active))  # <class 'bool'>
```

**String**
```python
greeting = "Hello"
multiline = '''This is
a multi-line string'''

# String methods
print(greeting.upper())       # "HELLO"
print(greeting.lower())       # "hello"
print(greeting.startswith("H"))  # True
print(len(greeting))          # 5
```

**Type Conversion**
```python
x = int("123")     # 123
y = str(123)       # "123"
z = float("3.14")  # 3.14
```

**Type Checking**
```python
type(x)             # <class 'int'>
isinstance(x, int)  # True
```

### 3. Functions

**Basic Function**
```python
def greet():
    print("Hello!")
```

**Function with Parameters**
```python
def greet(name):
    print(f"Hello, {name}!")
```

**Return Values**
```python
def add(a, b):
    return a + b

result = add(3, 4)
print(result)  # 7
```

**Default Arguments**
```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()          # Hello, Guest
greet("Alice")   # Hello, Alice
```

**Keyword Arguments**
```python
def order(item, quantity):
    print(f"{quantity}x {item}")

order(quantity=2, item="Apple")
```

**Variable-length Arguments**
```python
def print_args(*args):
    for arg in args:
        print(arg)

def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

**Type Hints (Python 3.5+)**
```python
def add(a: int, b: int) -> int:
    return a + b

def greet(name: str) -> None:
    print(f"Hello, {name}")
```

**Lambda Functions (Anonymous Functions)**
```python
square = lambda x: x**2
print(square(5))  # 25
```

### 2. Operators
- Arithmetic Operators
- Comparison Operators
- Logical Operators
- Bitwise Operators
- Assignment Operators
- Membership and Identity Operators

### 3. Control Flow
- `if`, `elif`, `else`
- Loops: `for`, `while`
- Loop Control: `break`, `continue`, `pass`

### 4. Functions
- Defining Functions
- Arguments and Return Values
- Lambda Functions
- `*args` and `**kwargs`

### 5. Data Structures
- Lists
- Tuples
- Sets
- Dictionaries
- Comprehensions

### 6. Strings
- String Literals
- Common String Methods
- f-Strings and Formatting

### 7. Modules and Imports
- Import Syntax
- Standard Library Examples
- Aliasing and `from ... import`

### 8. Exception Handling
- `try`, `except`, `else`, `finally`
- Common Exceptions

### 9. Classes and OOP
- Defining Classes
- `__init__` and `self`
- Inheritance
- Class vs. Instance Variables

### 10. File I/O
- Reading and Writing Files
- Context Managers (`with` statement)

### 11. Common Built-in Functions
- `len()`, `range()`, `enumerate()`, `zip()`
- `map()`, `filter()`, `sorted()`, etc.

### 12. Miscellaneous
- List Slicing
- `*` and `**` Unpacking
- Decorators (Brief Overview)
- Type Hints