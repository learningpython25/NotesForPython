

### 1. Basics
**Comments**
```python
# single line comment
"""multi line comment
"""
''' multi line single quote comment
'''

def add(x, y):
	""" docstring - function, class, module
	""" first line
```

**Variables and Data Types**
```python
x = 10
name = "user"
pi = 3.14
is_ready = True / False
```

**Input**
```python
name = input("Enter your name; ")
print(int(name))
```

### 2. Data Types

**Numbers**
```python
a = 5
b = 3.14
c = 2 + 3j
```

**Boolean**
```python
is_active = True
is_ready = False
#truthy, falsy
0 -> False
None Zero -> True

"" -> False, everything else True
None -> False
```

**String**
```python
greeting = "Hello"
multline = '''
this is multi line
'''

str.upper()
str.lower()
str.strip() # remove leading and trailing spaces " a " >> "a"
str.capitalize() #"the" > "The"
len(str)
str.startswith("h")
str[::]
```

**Type Conversion**
```python
x = int("123")
x = int("str") # ValueError
y = str(123)
```

**Type Checking**
```python
type(x) # <class 'int'>
isinstance(x, int)
```

### 3. Functions

**Basic Function**
```python
def greet():
	print("Hello")
```

**Function with Parameters**
```python
def greet(name):
	print("name is", name)
```

**Return Values**
```python
def add(a, b);
	return a + b
sum = add(11,2)
print(sum)
```

**Default Arguments**
```python
def greet(name="Guest"):
	print("name is", name)
greet()
greet("user")
```

**Keyword Arguments**
```python
def country(name, size):
	print(name, int(size))
country(size=123, name="abc")
country(name="def", size=456)
```

**Variable-length Arguments**
```python
# *args
def print_args(a, b, *args, **kwargs):
	for arg in args:
		print(arg)
print_args(1,3,'ab',[1,2], (1,2), a = 19, b=10)
# **kwargs alwasy at the ends
# *args -> alway at end, except **kwards
```

**Type Hints (Python 3.5+)**
```python
def add(a: int, b: int) -> int:
	return a+b
# giving hint to the user about the type
```

**Lambda Functions (Anonymous Functions)**
```python
square = lambda x: x**2

# single line
# single input
# single output

def sqr(x):
    return x**2
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