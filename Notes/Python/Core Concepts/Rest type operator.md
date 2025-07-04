
**Python**, which is more commonly referred to as **`*` and `**` unpacking operators**. These are used in different contexts but are conceptually similar to the **rest operator** found in JavaScript.
## 🌟 Python “Rest Operator” Concept (`*args`, `**kwargs`)

In Python, there isn't a dedicated "rest operator" like in JavaScript, but similar functionality is achieved through the `*` and `**` operators.

These are used to **collect or unpack** multiple arguments, items, or variables.

---

## 🔸 `*args` – Collect Positional Arguments

* `*args` collects any **extra positional arguments** into a **tuple**.
* Commonly used when the number of arguments is **not known in advance**.

```python
def add_all(*args):
    return sum(args)

add_all(1, 2, 3)        # 6
add_all(4, 5, 6, 7, 8)  # 30
```

* Internally, `args` is a tuple:

  ```python
  print(args)  # (1, 2, 3)
  ```

---

## 🔹 `**kwargs` – Collect Keyword Arguments

* `**kwargs` collects any **extra named arguments** into a **dictionary**.

```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=30, city="NY")
# name: Alice
# age: 30
# city: NY
```

* Internally, `kwargs` is a dict:

  ```python
  print(kwargs)  # {'name': 'Alice', 'age': 30, 'city': 'NY'}
  ```

---

## 🧰 Use in Function Definitions

### Combining Parameters

You can combine regular, `*args`, and `**kwargs` in the same function:

```python
def example(a, b=2, *args, **kwargs):
    print(a, b)
    print(args)
    print(kwargs)
```

---

## 🔁 Use in Function Calls

### Positional Arguments Unpacking with `*`

```python
def multiply(x, y):
    return x * y

nums = (5, 3)
print(multiply(*nums))  # 15
```

### Keyword Arguments Unpacking with `**`

```python
def greet(name, age):
    print(f"{name} is {age} years old.")

info = {"name": "Alice", "age": 30}
greet(**info)
```

---

## 📋 Extended Iterable Unpacking (Since Python 3.0)

### In Assignments

```python
first, *middle, last = [1, 2, 3, 4, 5]
# first = 1, middle = [2, 3, 4], last = 5
```

### In Loops

```python
pairs = [(1, 2), (3, 4), (5, 6)]
for a, *b in pairs:
    print(a, b)  # 1 [2], 3 [4], ...
```

---

## 💡 Notes & Best Practices

* `*args` must come after normal positional arguments.
* `**kwargs` must come after `*args` if both are used.
* Only one `*args` and one `**kwargs` allowed per function definition.
* Works well for decorators, wrappers, and flexible APIs.

---

## 🧪 Common Use Cases

1. **Flexible Function Definitions**
2. **Argument Forwarding**
3. **Flattening or Merging Lists and Dictionaries**
4. **Custom Decorators**
5. **Data unpacking and manipulation**

---

## Summary Table

| Syntax      | Purpose                                | Type Collected         |
| ----------- | -------------------------------------- | ---------------------- |
| `*args`     | Collect extra positional arguments     | Tuple                  |
| `**kwargs`  | Collect extra keyword arguments        | Dictionary             |
| `*sequence` | Unpack a list or tuple in call/assign  | Elements from iterable |
| `**dict`    | Unpack a dictionary into function args | Keys/values            |
