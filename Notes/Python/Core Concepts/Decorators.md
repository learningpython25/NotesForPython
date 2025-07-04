A **decorator** is a function that **modifies the behavior** of another function without changing its source code. Decorators are often used in logging, timing, access control, caching, etc.

---

## 🧠 Key Concept

> A decorator is a function that takes another function as input and returns a new function.

---

## 🧰 Basic Syntax

```python
def decorator(func):
    def wrapper():
        # Do something before
        func()
        # Do something after
    return wrapper

@decorator
def say_hello():
    print("Hello!")

say_hello()
```

This is **equivalent to**:

```python
say_hello = decorator(say_hello)
```

---

## 🔧 Decorator with Arguments

```python
def decorator(func):
    def wrapper(*args, **kwargs):
        print("Before")
        result = func(*args, **kwargs)
        print("After")
        return result
    return wrapper

@decorator
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
```

---

## 🪄 Built-in Decorators

### ✅ `@staticmethod`

```python
class MyClass:
    @staticmethod
    def greet():
        print("Hello")
```

### ✅ `@classmethod`

```python
class MyClass:
    count = 0
    
    @classmethod
    def get_count(cls):
        return cls.count
```

### ✅ `@property`

```python
class Circle:
    def __init__(self, radius):
        self._radius = radius

    @property
    def area(self):
        return 3.14 * self._radius ** 2
```

---

## 🧠 Decorator with Parameters (Decorator Factory)

```python
def repeat(n):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(n):
                func(*args, **kwargs)
        return wrapper
    return decorator

@repeat(3)
def greet():
    print("Hi!")
```

---

## 🧪 Example: Timing Decorator

```python
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"⏱️ Took {end - start:.4f}s")
        return result
    return wrapper

@timer
def slow_function():
    time.sleep(1)
    print("Done")

slow_function()
```

---

## 🧼 Preserving Metadata: `functools.wraps`

```python
from functools import wraps

def decorator(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs)
    return wrapper
```

Without `@wraps`, the wrapped function loses its name and docstring.

---

## 📌 Use Cases

* Logging
* Timing
* Caching (`@lru_cache`)
* Authorization
* Retry mechanisms

---

## ✅ Summary

* Decorators wrap functions to add or modify behavior
* Use `*args` and `**kwargs` for flexible wrappers
* Use `@wraps` to preserve metadata
* Decorators can be stacked or parameterized

