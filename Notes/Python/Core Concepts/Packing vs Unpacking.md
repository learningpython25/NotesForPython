
In Python, *packing* and *unpacking* are powerful features used to handle variable-length data in assignments, functions, and more.

### Packing

**Packing** is the process of placing multiple values into a single iterable (usually a tuple, but can also be a list or dictionary).

#### Tuple Packing

When you assign multiple values to a single variable without brackets, Python automatically packs them into a tuple.

```python
data = 1, 2, 3
print(data)         # (1, 2, 3)
print(type(data))   # <class 'tuple'>
```

####  List Packing (explicit)

You can pack into a list using brackets:

```python
data = [1, 2, 3]
```

####  Dictionary Packing

Using `**` in function parameters:

```python
def func(**kwargs):
    print(kwargs)

func(a=1, b=2)  # {'a': 1, 'b': 2}
```

### Unpacking

**Unpacking** is extracting values from a sequence (or iterable) into individual variables.

####  Basic Unpacking

```python
x, y = (10, 20)       # tuple unpacking
a, b = [1, 2]         # list unpacking
c, d = 'hi'           # string unpacking
```

❗ The number of variables must match the number of items.

####  Extended Unpacking (Python 3.0+)

You can use the `*` operator to unpack a part of a sequence into a list:

```python
first, *middle, last = [1, 2, 3, 4, 5]
# first = 1, middle = [2, 3, 4], last = 5
```

This works with:

* Lists
* Tuples
* Strings
* Ranges

Only one `*` can be used in an unpacking assignment.

---

### Swapping with Unpacking

Python allows elegant swapping without a temp variable:

```python
a, b = 1, 2
a, b = b, a  # Swaps values
```

---

### Function Arguments

####  Unpacking in Function Calls

```python
def add(a, b, c):
    return a + b + c

args = (1, 2, 3)
print(add(*args))  # 6

kwargs = {'a': 1, 'b': 2, 'c': 3}
print(add(**kwargs))  # 6
```

####  Packing Parameters in Function Definition

```python
def example(*args, **kwargs):
    print(args)
    print(kwargs)

example(1, 2, three=3, four=4)
# args = (1, 2)
# kwargs = {'three': 3, 'four': 4}
```

---

### Examples

```python
# Unpacking a list in a for loop
my_list = [("Alice", 25), ("Bob", 30)]
for name, age in my_list:
    print(f"{name} is {age} years old.")

# Extended unpacking in a loop
for first, *rest in [(1, 2, 3), (4, 5, 6)]:
    print(first, rest)  # 1 [2, 3] then 4 [5, 6]
```
