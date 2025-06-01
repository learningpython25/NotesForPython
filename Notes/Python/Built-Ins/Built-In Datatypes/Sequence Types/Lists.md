
* **ordered**, **mutable** 
* Lists can contain elements of different types (*int, str, float, even other lists)*.
* Created using square brackets `[]`
* Lists are **zero-indexed**.

  ```python
  my_list = [1, "apple", 3.14, True]
  ```

## Common List Methods

### Adding Elements

* `append(x)` – Adds item to the end
* `insert(i, x)` – Inserts item at index `i`
* `extend(iterable)` – Appends elements from another iterable

### Removing Elements

* `remove(x)` – Removes first occurrence of `x`
* `pop([i])` – Removes and returns item at index `i`; defaults to last
* `clear()` – Removes all items

### Other Useful Methods

* `index(x)` – Returns the index of the first occurrence
* `count(x)` – Returns number of occurrences of `x`
* `copy()` – Returns a shallow copy
* `reverse()` – Reverses the list in-place
* `sort()` – Sorts the list in-place (ascending by default)
* `sorted(my_list)` – Returns a new sorted list

## List Comprehensions

```python
[expression for item in iterable if condition]
```

- `expression`: The value to include in the new list.
- `item`: The variable representing each element in the iterable.
- `iterable`: The data source (e.g., list, range, string).
- `condition` (optional): A filter condition to include only certain elements.

**Basic Examples:**
```python
squares = [x*x for x in range(5)]  # [0, 1, 4, 9, 16]
evens = [x for x in range(10) if x % 2 == 0]  # [0, 2, 4, 6, 8]
words = [w.upper() for w in ["hello", "world"]]  # ['HELLO', 'WORLD']
```

**With Nested Loops:**
```python
pairs = [(x, y) for x in [1, 2] for y in [3, 4]]  # [(1, 3), (1, 4), (2, 3), (2, 4)]
```

**With Conditions:**
```python
div_by_3 = [x for x in range(20) if x % 3 == 0]
```

**Transforming Elements:**
```python
word_lengths = [len(word) for word in ["apple", "banana", "cherry"]]  # [5, 6, 6]
```

**Conditional Expression (if-else):**
```python
labels = ["even" if x % 2 == 0 else "odd" for x in range(5)]
# ['even', 'odd', 'even', 'odd', 'even']
```

**With Nested Lists:**
```python
matrix = [[1, 2], [3, 4], [5, 6]]
flattened = [num for row in matrix for num in row]  # [1, 2, 3, 4, 5, 6]
```


## Slicing
- **Slicing** allows you to access sub-parts of a list.
- Syntax: `[start:stop:step]`
    - `start`: the beginning index (inclusive)
    - `stop`: the ending index (exclusive)
    - `step`: the stride or jump (default is 1)

```python
my_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
my_list[1:4]      # [1, 2, 3]
my_list[:3]       # [0, 1, 2]
my_list[::2]      # [0, 2, 4, 6, 8]
my_list[1::2]     # [1, 3, 5, 7, 9]
my_list[::-1]     # Reversed list [9, 8, ..., 0]
my_list[-3:]      # Last 3 elements [7, 8, 9]
my_list[:-3]      # Everything except last 3 [0 to 6]
```

**Notes**
- If `start` is omitted, it defaults to the beginning.
- If `stop` is omitted, it defaults to the end.
- If `step` is negative, slicing moves in reverse.
- Slicing **does not modify** the original list. It returns a new list

- Use `[::-1]` to reverse a list.
- Use slicing to copy a list: `new_list = old_list[:]`

## Nested Lists

* A list can contain other lists as elements.

  ```python
  matrix = [[1, 2], [3, 4], [5, 6]]
  print(matrix[0][1])  # 2
  ```
* Useful for representing 2D structures (like grids, matrices)
```python
for row in matrix:
  for item in row:
	  print(item)
```

