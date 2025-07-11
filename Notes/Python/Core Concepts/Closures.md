### Closure = Function + Remembered Enclosing Values

A **closure** lets an inner function **remember values** from its outer function, even **after the outer function has finished executing**.

---

### 🧪 Example: `adder(n)` returns a function that adds `n` to its input

```python
def adder(n):
    def add(x):
        return x + n
    return add
```

---

### ✅ Usage

```python
add5 = adder(5)
add10 = adder(10)

print(add5(2))   # 7 → 2 + 5
print(add10(2))  # 12 → 2 + 10
```

* `add5` remembers `n = 5`
* `add10` remembers `n = 10`
* Both are closures that "close over" the variable `n`

---

### 🔍 What's Happening Internally

Each returned function has its own copy of the enclosed `n`:

```python
print(add5.__closure__[0].cell_contents)   # 5
print(add10.__closure__[0].cell_contents)  # 10
```
