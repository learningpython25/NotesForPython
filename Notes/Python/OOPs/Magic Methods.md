
* Special methods with double underscores (e.g., `__init__`, `__str__`, `__add__`)
* Used to **customize object behavior**

---

### Common Examples

```python
class Book:
    def __init__(self, pages):
        self.pages = pages

    def __str__(self):
        return f"Book with {self.pages} pages"

    def __add__(self, other):
        return Book(self.pages + other.pages)

b1 = Book(100)
b2 = Book(150)

print(b1)        # Book with 100 pages
b3 = b1 + b2
print(b3.pages)  # 250
```

---

###  Other Magic Methods

| Method        | Purpose                     |
| ------------- | --------------------------- |
| `__init__`    | Constructor                 |
| `__str__`     | Human-readable string       |
| `__repr__`    | Developer-facing string     |
| `__len__`     | Supports `len(obj)`         |
| `__eq__`      | Equality check (`==`)       |
| `__lt__`      | Less than (`<`)             |
| `__getitem__` | Indexing support (`obj[i]`) |

---
