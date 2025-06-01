
A **tuple** is an **immutable**, ordered sequence of elements. Tuples can contain **mixed data types**, including other tuples.

```python
t = (1, 2, 3)
```

* Single-element tuple **must have a trailing comma**:

```python
t1 = (5,)  # ✅ This is a tuple
t2 = (5)   # ❌ This is just an integer
```

### Characteristics:

| Property             | Description                                                          |
| -------------------- | -------------------------------------------------------------------- |
| **Immutable**        | Cannot be changed after creation                                     |
| **Ordered**          | Maintains insertion order                                            |
| **Indexable**        | Can access items using indices                                       |
| **Hashable**         | ✅ If all its elements are hashable (can be dict keys or set members) |
| **Iterable**         | Can be iterated with loops                                           |
| **Allow Duplicates** | ✅ Yes                                                                |

---

### Common Operations:

```python
t = (10, 20, 30)

t[1]         # 20
len(t)       # 3
t[:2]        # (10, 20)
(1, 2) + (3,)  # (1, 2, 3)
(2,) * 3     # (2, 2, 2)
```

---

### Tuple Packing and Unpacking:

```python
# Packing
t = 1, 2, 3  # Equivalent to (1, 2, 3)

# Unpacking
a, b, c = t  # a=1, b=2, c=3

# Extended unpacking
a, *rest = (1, 2, 3, 4)  # a=1, rest=[2,3,4]
```

### Immutability caveat:

If a tuple contains **mutable objects**, those objects can still be modified:

```python
t = (1, [2, 3])
t[1].append(4)
print(t)  # (1, [2, 3, 4]) ← tuple is same, but list inside changed
```
