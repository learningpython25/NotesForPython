


* A **set** is an **unordered**, **mutable**, and **unindexed** collection of **unique** elements.
* Initialized using curly braces `{}` or  `set()` 
* Duplicates are **automatically removed**.

```python
my_set = {1, 2, 3, 3, 4}   # {1, 2, 3, 4}
empty_set = set()         # Note: {} creates an empty dict, not a set
```

## Properties

* `Unordered` → No indexing or slicing
* `Mutable` → Can add/remove elements
* *Elements must be immutable* (numbers, strings, tuples)

### Adding Elements

* `add(x)` – Adds a single element
* `update(iterable)` – Adds multiple elements from iterable

```python
s = {1, 2}
s.add(3)           # {1, 2, 3}
s.update([4, 5])   # {1, 2, 3, 4, 5}
```

### Removing Elements

* `remove(x)` – Removes `x`; raises error if not found
* `discard(x)` – Removes `x`; does nothing if not found
* `pop()` – Removes and returns an arbitrary element
* `clear()` – Removes all elements

```python
s.remove(2)
s.discard(10)  # Safe, no error
s.pop()
s.clear()
```

### Set Operations

#### Union

* `set1 | set2` or `set1.union(set2)`

```python
{1, 2} | {2, 3}        # {1, 2, 3}
```

#### Intersection

* `set1 & set2` or `set1.intersection(set2)`

```python
{1, 2} & {2, 3}        # {2}
```

#### Difference

* `set1 - set2` or `set1.difference(set2)`

```python
{1, 2, 3} - {2}        # {1, 3}
```

#### Symmetric Difference

* `set1 ^ set2` or `set1.symmetric_difference(set2)`

```python
{1, 2} ^ {2, 3}        # {1, 3}
```

## Other Methods

* `copy()` – Shallow copy
* `len(set)` – Number of elements
* `in` keyword – Check membership
* `isdisjoint(other)` – True if no common elements
* `issubset(other)` – True if all elements are in `other`
* `issuperset(other)` – True if all `other`'s elements are in set

```python
s = {1, 2, 3}
s2 = {2, 3}
s.issuperset(s2)  # True
```

# Frozenset

* Immutable version of a set: `frozenset()`
* Supports all read-only operations (like union, intersection)
* Useful for dict keys or set of sets

```python
fs = frozenset([1, 2, 3])
```

## Summary Table

| Operation            | Syntax              | Description                  |                      |
| -------------------- | ------------------- | ---------------------------- | -------------------- |
| Add                  | `set.add(x)`        | Add single element           |                      |
| Update               | `set.update(iter)`  | Add multiple elements        |                      |
| Remove               | `set.remove(x)`     | Remove, error if not found   |                      |
| Discard              | `set.discard(x)`    | Remove, safe if not found    |                      |
| Pop                  | `set.pop()`         | Remove arbitrary element     |                      |
| Clear                | `set.clear()`       | Empty the set                |                      |
| Union                | \`set1              | set2\`                       | Combine all elements |
| Intersection         | `set1 & set2`       | Common elements              |                      |
| Difference           | `set1 - set2`       | Elements in set1 not in set2 |                      |
| Symmetric Difference | `set1 ^ set2`       | Elements in either, not both |                      |
| Subset               | `set1 <= set2`      | Check if subset              |                      |
| Superset             | `set1 >= set2`      | Check if superset            |                      |
| Disjoint             | `set1.isdisjoint()` | Check if no overlap          |                      |


| Feature            | `set` | `frozenset` |
| ------------------ | ----- | ----------- |
| Mutable            | ✅     | ❌           |
| Hashable           | ❌     | ✅           |
| Usable as dict key | ❌     | ✅           |
