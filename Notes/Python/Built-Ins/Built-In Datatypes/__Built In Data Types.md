
| Category           | Type(s)                            |
| ------------------ | ---------------------------------- |
| Text Sequence Type | `str`                              |
| Numeric            | `int`, `float`, `complex`          |
| Sequence           | `list`, `tuple`, `range`           |
| Mapping            | `dict`                             |
| Set                | `set`, `frozenset`                 |
| Boolean            | `bool`                             |
| Binary             | `bytes`, `bytearray`, `memoryview` |
| None               | `NoneType`                         |


### 1. Text Type

* **`str`** → A string of characters.

```python
name = "John"
```

### 2. Numeric Types

* **`int`** → Integer numbers (e.g., 5, -3)
* **`float`** → Floating point numbers (e.g., 3.14)
* **`complex`** → Complex numbers (e.g., 2 + 3j)

```python
a = 10         # int
b = 3.14       # float
c = 2 + 5j     # complex
```

### 🧮 3. Sequence Types

* **`list`** → Ordered, mutable, allows duplicates.
* **`tuple`** → Ordered, immutable, allows duplicates.
* **`range`** → Sequence of numbers, commonly used in loops.

```python
fruits = ["apple", "banana"]     # list
point = (1, 2)                   # tuple
numbers = range(5)              # 0 to 4
```

### 4. Mapping Type

* **`dict`** → Key-value pairs, unordered (as of Python 3.7, insertion ordered).

```python
person = {"name": "Alice", "age": 30}
```

### 🎯 5. Set Types

* **`set`** → Unordered, no duplicates, mutable.
* **`frozenset`** → Like set, but immutable.

```python
unique_items = {1, 2, 3}
frozen = frozenset([1, 2, 3])
```

### 6. Boolean Type

* **`bool`** → True or False (used for logic)

```python
is_valid = True
```

### 7. Binary Types

* **`bytes`** → Immutable sequence of bytes.
* **`bytearray`** → Mutable sequence of bytes.
* **`memoryview`** → View over binary data without copying.

```python
b = bytes([65, 66, 67])
ba = bytearray([65, 66, 67])
mv = memoryview(b)
```

### 8. None Type

* **`NoneType`** → Represents absence of a value.

```python
result = None
```
