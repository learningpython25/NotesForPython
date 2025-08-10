
* **Mutable**: Objects that can be changed **after** creation.
* **Immutable**: Objects that **cannot** be changed after creation; operations create new objects instead.

---

## Immutable Types

* `int`, `float`, `bool`
* `str`
* `tuple`
* `frozenset`
* `bytes`

```python
x = "hello"
x = x.upper()
# x is now "HELLO", original "hello" is discarded and a new string object is created
```

---

## Mutable Types

* `list`
* `dict`
* `set`
* `bytearray`
* `custom classes` (usually, unless designed otherwise)

```python
lst = [1, 2, 3]
lst.append(4)
# lst is modified in place to [1, 2, 3, 4]
```

---

## Reassignment vs Mutation

### Immutable Example

```python
a = 10
b = a
a = 20
# b remains 10; reassignment makes 'a' point to a new object
```

### Mutable Example

```python
a = [1, 2, 3]
b = a
a.append(4)
# b is also [1, 2, 3, 4]; 'a' and 'b' point to the same object
```

---

## Mutating vs Rebinding

* **Mutating** modifies the object *in-place*.
* **Rebinding** makes a variable point to a new object.

```python
# Mutating
my_list = [1, 2]
my_list.append(3)  # modifies original list

# Rebinding
my_list = [4, 5]   # now points to a new list, original is discarded
```

---

## Behavior in Functions

### Immutable Types in Functions

```python
def modify(x):
    x = x + 1

a = 5
modify(a)
print(a)  # 5 — original not modified
```

* `x` is rebound to a new int inside the function; original `a` remains unchanged.

### Mutable Types in Functions

```python
def modify(lst):
    lst.append(4)

a = [1, 2, 3]
modify(a)
print(a)  # [1, 2, 3, 4] — original list is changed
```

* Function modifies the object itself (no rebinding), so the change reflects outside.

---

## Common Mistakes

* Default arguments in functions:

```python
def add(item, lst=[]):
    lst.append(item)
    return lst

add(1)  # [1]
add(2)  # [1, 2] ← unexpected behavior
```

🧠 **Why?** Because default arguments are evaluated once at function definition time. Use this instead:

```python
def add(item, lst=None):
    if lst is None:
        lst = []
    lst.append(item)
    return lst
```


## Summary 

| Type    | Mutable? | Can be changed without reassignment? |
| ------- | -------- | ------------------------------------ |
| `int`   | No       | ❌                                    |
| `str`   | No       | ❌                                    |
| `tuple` | No       | ❌                                    |
| `list`  | Yes      | ✅ (e.g., append, extend)             |
| `dict`  | Yes      | ✅ (e.g., assign new key)             |
| `set`   | Yes      | ✅ (e.g., add, remove)                |
