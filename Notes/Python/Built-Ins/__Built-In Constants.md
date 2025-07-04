
##  `True` and `False`

- Boolean values.
- Subclass of `int`: `True == 1`, `False == 0`

```python
is_valid = True
if not False:
    print("This runs!")
````

---

## `None`

* Represents the absence of a value.
* Commonly used to indicate "no result", "not initialized", or a "default placeholder".

```python
result = None

def greet(name=None):
    if name is None:
        name = "Guest"
    print(f"Hello, {name}")
```

---

##  `NotImplemented`

* Used to indicate that an operation is **not implemented** for the given types.
* Usually returned by special method overloads like `__eq__`, `__add__`, etc.

```python
class MyNumber:
    def __eq__(self, other):
        if not isinstance(other, MyNumber):
            return NotImplemented
        return self.value == other.value
```

---

## `Ellipsis` or `...`

* Syntactic placeholder.
* Often used in:

  * Slicing multi-dimensional arrays
  * Stub functions or incomplete code
  * Type hinting in advanced scenarios

```python
a = [ [ [0] * 3 ] * 3 ] * 3
print(a[0][...])  # works in numpy, e.g., arr[..., 0]

def todo():
    ...
```

---

## `__debug__`

* A constant that is `True` if Python was **not started with the `-O` (optimize)** flag.
* Commonly used with `assert` statements and debugging code.

```python
if __debug__:
    print("Debug mode is on")
```

## Summary Table

| Constant           | Description                              |
| ------------------ | ---------------------------------------- |
| `True` / `False`   | Boolean truth values                     |
| `None`             | Represents "no value"                    |
| `NotImplemented`   | Used when an operation isn’t supported   |
| `Ellipsis` (`...`) | Placeholder, often in slicing            |
| `__debug__`        | True unless Python is run with `-O` flag |
