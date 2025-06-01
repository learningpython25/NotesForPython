

A **range** represents an **immutable sequence of numbers**, commonly used in loops.


```python
range(stop)
range(start, stop)
range(start, stop, step)
```

### Examples:

```python
list(range(5))           # [0, 1, 2, 3, 4]
list(range(2, 6))        # [2, 3, 4, 5]
list(range(2, 10, 2))    # [2, 4, 6, 8]
list(range(10, 2, -2))   # [10, 8, 6, 4]
```

### Characteristics:

| Property             | Description                                 |
| -------------------- | ------------------------------------------- |
| **Immutable**        | ✅ Cannot change a range after creation      |
| **Ordered**          | ✅ Maintains order                           |
| **Indexable**        | ✅ Supports indexing and slicing             |
| **Memory Efficient** | ✅ Stores only start, stop, step (lazy eval) |
| **Iterable**         | ✅ Can use in loops and comprehensions       |
| **Hashable**         | ✅ Yes                                       |

* Looping a fixed number of times:

```python
for i in range(5):
    print(i)
```

### Advanced: `range` object methods

```python
r = range(10)
r.start   # 0
r.stop    # 10
r.step    # 1
```

---

### Converting to list:

* `range` is **not a list**.
* Use `list(range(...))` when you need actual data.

```python
type(range(5))         # <class 'range'>
list(range(5))         # [0, 1, 2, 3, 4]
```

### When to use `range` vs list:

| Use Case                   | Use `range`            | Use `list`                     |
| -------------------------- | ---------------------- | ------------------------------ |
| Large sequence (efficient) | ✅ Yes                  | ❌ Memory costly                |
| Need all values at once    | ❌ Must convert to list | ✅ Already contains values      |
| Looping by index           | ✅ Common choice        | ✅ Also works via `enumerate()` |
