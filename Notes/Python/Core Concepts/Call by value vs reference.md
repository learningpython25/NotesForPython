
Python uses **"call by object reference"** (also called **call by assignment**). This behavior is often misunderstood as either *call by value* or *call by reference*, but it's actually a blend.

## What happens during a function call?

* When you pass an object to a function, **the reference (or address)** to the object is passed **by value**.
* This means:

  * Inside the function, the parameter refers to the **same object**.
  * But **reassigning** the parameter to something else will not affect the original object.

## Immutable vs Mutable Behavior

### Immutable Types (`int`, `float`, `str`, `tuple`, etc.)

```python
def modify(x):
    x = x + 1

a = 10
modify(a)
print(a)  # ➜ 10
```

* `x = x + 1` creates a **new object**.
* Original `a` is unchanged.

---

### Mutable Types (`list`, `dict`, `set`, etc.)

```python
def modify(lst):
    lst.append(4)

a = [1, 2, 3]
modify(a)
print(a)  # ➜ [1, 2, 3, 4]
```

* `lst.append(4)` modifies the original object.
* Function and caller both see the change.

---

## Key Points

| Concept                     | Description                                         |
| --------------------------- | --------------------------------------------------- |
| Function arguments          | Passed by *object reference*                        |
| Immutable objects           | Cannot be changed; reassigning creates a new object |
| Mutable objects             | Can be modified in-place                            |
| Rebinding inside a function | Does **not** affect original object                 |


## Rebinding

```python
def modify(lst):
    lst = [4]  # Rebinding to a new object

a = [1, 2, 3]
modify(a)
print(a)  # ➜ [1, 2, 3]
```

* `lst = [4]` creates a new list; does **not** affect `a`.
