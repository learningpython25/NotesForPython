
# 🔁 Iterators in Python

An **iterator** is an object that allows you to **traverse a sequence one element at a time** using the built-in `next()` function.

---

## 🧠 Key Concepts

* **Iterable**: Any object you can loop over (`for x in obj`)
* **Iterator**: Object with `__iter__()` and `__next__()` methods
* `iter(obj)` turns an iterable into an iterator
* `next(obj)` fetches the next item, raises `StopIteration` when done

---

## 🧪 Basic Example

```python
nums = [1, 2, 3]
it = iter(nums)         # Get iterator
print(next(it))         # → 1
print(next(it))         # → 2
print(next(it))         # → 3
print(next(it))         # Raises StopIteration
```

---

## 🔁 Behind the Scenes of a `for` Loop

```python
for x in iterable:
    # internally does:
    it = iter(iterable)
    while True:
        try:
            x = next(it)
            # do something with x
        except StopIteration:
            break
```

---

## 🧱 Creating a Custom Iterator

You can define your own iterator class by implementing `__iter__()` and `__next__()`.

```python
class Counter:
    def __init__(self, max_val):
        self.i = 0
        self.max = max_val

    def __iter__(self):
        return self

    def __next__(self):
        if self.i < self.max:
            self.i += 1
            return self.i
        else:
            raise StopIteration

for num in Counter(3):
    print(num)  # 1 2 3
```

---

## ⚠️ Important Notes

* An iterator **remembers its state** (where it left off).
* Iterators are **consumed once**; you cannot reset them unless you create a new one.
* Not all iterables are iterators (e.g., lists, tuples are iterable but not iterators until passed to `iter()`)

---

## ✅ Use Cases

* Efficient looping over large data streams
* Reading files line by line
* Custom sequence logic
* Lazy evaluation

---

## 🆚 Iterable vs Iterator

| Feature            | Iterable              | Iterator                  |
| ------------------ | --------------------- | ------------------------- |
| Has `__iter__()`   | ✅                     | ✅                         |
| Has `__next__()`   | ❌                     | ✅                         |
| Used in `for` loop | ✅                     | ✅                         |
| Example            | `list`, `str`, `dict` | `iter(list)`, file object |
