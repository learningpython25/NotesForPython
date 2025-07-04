
*pydocs*: https://docs.python.org/3/reference/lexical_analysis.html#keywords 

|          |            |           |            |          |
| -------- | ---------- | --------- | ---------- | -------- |
| `FALSE`  | `await`    | `else`    | `import`   | `pass`   |
| `None`   | `break`    | `except`  | `in`       | `raise`  |
| `TRUE`   | `class`    | `finally` | `is`       | `return` |
| `and`    | `continue` | `for`     | `lambda`   | `try`    |
| `as`     | `def`      | `from`    | `nonlocal` | `while`  |
| `assert` | `del`      | `global`  | `not`      | `with`   |
| `async`  | `elif`     | `if`      | `or`       | `yield`  |

To get the list programmatically:

```python
import keyword
print(keyword.kwlist)
```

> [!important]
> There are **35** keywords:

## Control Flow Keywords

* `if` – Conditional execution
* `else` – Alternate branch in conditional
* `elif` – Else if; additional condition
* `for` – Loop over an iterable
* `while` – Loop as long as condition is True
* `break` – Exit the nearest loop
* `continue` – Skip rest of loop body and continue
* `pass` – Do nothing (placeholder)

## Function & Class Definition

* `def` – Define a function
* `return` – Return a value from a function
* `lambda` – Anonymous function expression
* `class` – Define a class
* `yield` – Used with generators

## Exception Handling

* `try` – Start a block to catch exceptions
* `except` – Catch an exception
* `finally` – Always execute after try/except
* `raise` – Raise an exception
* `assert` – Debugging check, raises error if False

## Import Management

* `import` – Import a module
* `from` – Import specific items from a module
* `as` – Alias for imports or context

## Variable Scope & Binding

* `global` – Declare a global variable
* `nonlocal` – Use variable from outer non-global scope

## Logical & Comparison Operators

* `and` – Logical AND
* `or` – Logical OR
* `not` – Logical NOT
* `is` – Object identity
* `in` – Membership test

## Special Constants and Modifiers

* `True` – Boolean true value
* `False` – Boolean false value
* `None` – Null/empty value

## Context & Misc

* `with` – Context manager (used with `open`, etc.)
* `del` – Delete a variable, object, or element
* `await` – Wait for an async call (used in `async` code)
* `async` – Define an asynchronous function

