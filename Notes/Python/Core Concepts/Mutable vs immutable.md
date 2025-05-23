

- **Mutable objects** can be changed after they are created.
- **Immutable objects** cannot be changed after creation; any "modification" results in a new object.

---

### Immutable Types

- Immutable objects cannot be changed once they are created. 
- When we try to change an immutable object, Python creates a new object.

##### Common Immutable Types:
1. **Numbers**:
   - `int`, `float`, `complex`, `bool`
   - 
     ```python
     a = 5
     print(id(a))  # 140712942377584
     a += 1
     print(id(a))  # New ID → new object
     ```

1. **Strings**:
   - Strings are immutable, meaning that methods like `.replace()` or slicing always create new strings.
     ```python
     s = "hello"
     print(id(s))  # 140712942377584
     s = s + " world"
     print(id(s))  # New ID → new object
     ```

1. **Tuples**:
   - Tuples are immutable, but they can contain mutable objects inside them.
     ```python
     t = (1, 2, 3)
     print(id(t))  # 239485720
     t = t + (4,)
     print(id(t))  # New ID → new object
     ```

1. **Frozen Set**:
     ```python
     s = frozenset([1, 2, 3])
     print(id(s))  # 239485720
     s = frozenset([1, 2, 3, 4])
     print(id(s))  # New ID → new object
     ```

2. **Bytes**:
     ```python
     b = b'hello'
     print(id(b))  # 239485720
     b = b + b' world'
     print(id(b))  # New ID → new object
     ```

---

### Mutable Types

Mutable objects can be changed after they are created, meaning their contents can be modified in place.

##### Common Mutable Types:
1. **Lists**:
   - Lists are mutable, meaning you can add, remove, or change items in place.
     ```python
     lst = [1, 2, 3]
     print(id(lst))  # 239485720
     lst.append(4)
     print(id(lst))  # Same ID → modified in place
     ```

1. **Dictionaries**:
     ```python
     d = {'a': 1, 'b': 2}
     print(id(d))  # 239485720
     d['c'] = 3
     print(id(d))  # Same ID → modified in place
     ```

2. **Sets**:
     ```python
     s = {1, 2, 3}
     print(id(s))  # 239485720
     s.add(4)
     print(id(s))  # Same ID → modified in place
     ```

3. **Bytearrays**:
     ```python
     b = bytearray(b'hello')
     print(id(b))  # 239485720
     b.append(32)  # Append space (ASCII 32)
     print(id(b))  # Same ID → modified in place
     ```


---

### How is this useful?

##### 1. Function Arguments:
   - When passing mutable types to functions, any changes made to the object inside the function will **affect the original object** outside.
   - Immutable types will not affect the original object, since any modification creates a new object.

   Example:
   ```python
   def add_one(x):
       x += 1
       return x

   def append_one(lst):
       lst.append(1)
       return lst

   a = 5
   b = [0]
   add_one(a)    # 6, but a is still 5
   append_one(b) # [0, 1], b is modified
```

##### 2. Performance Considerations:

- Immutable objects are generally **memory-efficient** because they can be reused (e.g., `str` interning).
- Mutable objects offer **flexibility**, but they can lead to side effects when shared across functions.

##### 3. Hashing:

- Immutable objects are **hashable**, meaning they can be used as dictionary keys or set elements.
- Mutable objects are **not hashable** because their contents can change, making their hash values unreliable.

Example:

```python
hash("hello")    # ✅
hash([1, 2, 3])  # ❌ TypeError
```

---

### Important Notes

1. **Copying Objects**:
    - A **shallow copy** (e.g., using `copy.copy()`) only copies references for mutable objects, while a **deep copy** (e.g., using `copy.deepcopy()`) creates a copy of nested objects as well.
    - Immutable objects are safe from unintended changes, but mutable ones can be copied with references, causing side effects.
    
2. **Type Checking**:
    - Use `isinstance()` to check if an object is of a specific type (e.g., `isinstance(my_obj, list)`).
    - Be mindful of which types are mutable or immutable when deciding how to structure your code and design your data.


## 📚 **Quick Reference**

|Type|Mutable|Hashable|
|---|---|---|
|`int`|❌|✅|
|`float`|❌|✅|
|`str`|❌|✅|
|`tuple`|❌|✅ _(if elements are immutable)_|
|`list`|✅|❌|
|`dict`|✅|❌|
|`set`|✅|❌|
|`frozenset`|❌|✅|
