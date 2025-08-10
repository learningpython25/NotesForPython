
* `bool` is a built-in data type in Python used to represent **truth values**.
* There are only two Boolean values:

  ```python
  True  # represents truth
  False # represents falsehood
  ```
* Internally, `bool` is a subclass of `int`:

  ```python
  isinstance(True, int)  # True
  int(True)  # 1
  int(False) # 0
  ```

### Truthy vs Falsy

* **Falsy values** in Python:

  * `None`
  * `False`
  * `0` (of any numeric type)
  * `''` (empty string)
  * `[]` (empty list)
  * `{}` (empty dict)
  * `set()`, `tuple()`, `range(0)`
* All other values are considered **truthy**.

### Example:

```python
if []:
    print("Truthy")
else:
    print("Falsy")  # Will run
```

### Using `bool()` constructor:

```python
bool(0)        # False
bool(1)        # True
bool("")       # False
bool("Hello")  # True
```


## Boolean Operators

### 1. `and`

* Returns the **first falsy** value or the **last** if all are truthy.

```python
True and False  # False
1 and 0         # 0
"Hi" and 123    # 123
```

### 2. `or`

* Returns the **first truthy** value or the **last** if all are falsy.

```python
True or False   # True
"" or "Hi"      # "Hi"
0 or [] or {}   # {}
```

### 3. `not`

* Negates the truth value.

```python
not True   # False
not 0      # True
not "Hi"   # False
```


## Comparison with Other Types

| Expression      | Result  | Explanation                |
| --------------- | ------- | -------------------------- |
| `bool(10)`      | `True`  | Non-zero number is truthy  |
| `bool('')`      | `False` | Empty string is falsy      |
| `bool([])`      | `False` | Empty list is falsy        |
| `bool(None)`    | `False` | `None` is falsy            |
| `bool('False')` | `True`  | Non-empty string is truthy |

## Immutable Nature

* `bool` values are **immutable**.
* There are only **two singleton instances**: `True` and `False`.


