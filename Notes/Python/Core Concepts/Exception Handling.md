

Exception handling in Python is a mechanism that allows you to **gracefully respond to runtime errors** or unexpected conditions.

---

## What is an Exception?

An **exception** is an error that occurs during program execution, disrupting the normal flow.
Examples: division by zero, accessing an undefined variable, file not found, etc.

---

## Basic Structure

```python
try:
    # Code that might raise an exception
except SomeException:
    # Code to handle that exception
```

---

## Example

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

---

## `try`...`except`...`else`...`finally`

```python
try:
    # Code that might raise an exception
except SomeException:
    # Handles the exception
else:
    # Executes if no exceptions were raised
finally:
    # Executes no matter what (cleanup code)
```

### Use Case:

```python
try:
    f = open("file.txt")
except FileNotFoundError:
    print("File not found")
else:
    print(f.read())
    f.close()
finally:
    print("Execution complete")
```

---

## Catching Multiple Exceptions

```python
try:
    risky_function()
except (TypeError, ValueError) as e:
    print("Caught a type or value error:", e)
```

---

## Catch All Exceptions (Not Recommended for General Use)

```python
try:
    do_something()
except Exception as e:
    print("Error:", e)
```

> ⚠️ Use with caution. It hides bugs if overused.

---

## Raising Exceptions

You can **manually raise exceptions**:

```python
raise ValueError("Invalid input")
```

---

##  Creating Custom Exceptions

```python
class MyCustomError(Exception):
    pass

raise MyCustomError("Something went wrong!")
```

---

## 📘 Built-in Exceptions

| Exception           | Trigger Condition                      |
| ------------------- | -------------------------------------- |
| `ZeroDivisionError` | Division by zero                       |
| `TypeError`         | Wrong data type                        |
| `ValueError`        | Correct type but invalid value         |
| `KeyError`          | Dict key not found                     |
| `IndexError`        | List index out of range                |
| `FileNotFoundError` | Missing file                           |
| `ImportError`       | Failed to import a module              |
| `AttributeError`    | Object does not have a named attribute |

[ Full list](https://docs.python.org/3/library/exceptions.html)

---

## Best Practices

* Catch specific exceptions rather than using `except:`
* Always clean up (close files, DBs) in `finally`
* Use logging (not just print) to report exceptions
* Raise meaningful exceptions in functions/APIs

---

## Debug Tip

Use `traceback` module to get full stack trace:

```python
import traceback

try:
    1 / 0
except:
    traceback.print_exc()
```
