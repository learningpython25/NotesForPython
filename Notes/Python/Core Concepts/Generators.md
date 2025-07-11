A **generator** is a special type of iterator that allows you to **yield items one at a time** using the `yield` keyword instead of returning them all at once.

---

### 🔄 Generator vs Normal Function

| Normal Function              | Generator Function                           |
| ---------------------------- | -------------------------------------------- |
| Uses `return`                | Uses `yield`                                 |
| Returns once                 | Can pause and resume                         |
| Stores full result in memory | Generates items on the fly (lazy evaluation) |

---

### 🧪 Example: Simple Generator

```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

gen = count_up_to(3)
print(next(gen))  # 1
print(next(gen))  # 2
print(next(gen))  # 3
```

---

### ⚙️ Use Cases

* Reading large files line-by-line
* Streaming data
* Lazy evaluation (memory efficient)
* Custom iterable objects

---

### 🧵 Generator Expression (like list comprehension)

```python
squares = (x*x for x in range(5))
print(next(squares))  # 0
print(next(squares))  # 1
```

> ✅ Use `()` instead of `[]` for generator expression.

---

### 🚫 StopIteration Exception

A generator **automatically raises `StopIteration`** when it runs out of items.

```python
gen = count_up_to(2)
for num in gen:
    print(num)
# Output: 1, 2
```

---

### 🔍 Checkpoint: When to use generators?

✅ Use them when:

* You **don’t need all results at once**
* You're processing **large datasets**
* You want **cleaner, memory-safe code**

---

### 🔄 Converting to List (if needed)

```python
gen = count_up_to(3)
print(list(gen))  # [1, 2, 3]
```

---

### 💡 Advanced: Generator with `send()`

```python
def greeter():
    name = yield "What's your name?"
    yield f"Hello, {name}!"

g = greeter()
print(next(g))         # What's your name?
print(g.send("Alice")) # Hello, Alice!
```
