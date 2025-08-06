
>[!important] **dunders** = Double Underscores

##  Object Initialization and Construction

| Method     | Purpose                                    |
| ---------- | ------------------------------------------ |
| `__init__` | Constructor, initializes instance          |
| `__new__`  | Allocates memory, called before `__init__` |
| `__del__`  | Destructor, called when object is deleted  |

---

##  String Representation

| Method       | Purpose                                            |
| ------------ | -------------------------------------------------- |
| `__str__`    | Returns human-readable string (e.g., `print(obj)`) |
| `__repr__`   | Returns official string representation             |
| `__format__` | Used with `format()`                               |
| `__bytes__`  | Returns byte representation                        |

---

##  Comparison and Ordering

| Method   | Purpose                    |
| -------- | -------------------------- |
| `__eq__` | Equal `==`                 |
| `__ne__` | Not equal `!=`             |
| `__lt__` | Less than `<`              |
| `__le__` | Less than or equal `<=`    |
| `__gt__` | Greater than `>`           |
| `__ge__` | Greater than or equal `>=` |

---

##  Arithmetic Operators

| Method         | Operator  |
| -------------- | --------- |
| `__add__`      | `+`       |
| `__sub__`      | `-`       |
| `__mul__`      | `*`       |
| `__matmul__`   | `@`       |
| `__truediv__`  | `/`       |
| `__floordiv__` | `//`      |
| `__mod__`      | `%`       |
| `__pow__`      | `**`      |
| `__neg__`      | Unary `-` |
| `__pos__`      | Unary `+` |
| `__abs__`      | `abs()`   |

---

##  Bitwise Operators

| Method       | Operator |    |
| ------------ | -------- | -- |
| `__and__`    | `&`      |    |
| `__or__`     | \`       | \` |
| `__xor__`    | `^`      |    |
| `__invert__` | `~`      |    |
| `__lshift__` | `<<`     |    |
| `__rshift__` | `>>`     |    |

---

##  Type Conversion

| Method        | Function                 |
| ------------- | ------------------------ |
| `__int__`     | `int()`                  |
| `__float__`   | `float()`                |
| `__complex__` | `complex()`              |
| `__bool__`    | `bool()`                 |
| `__index__`   | Used in slicing/indexing |

---

##  Length, Size, and Container Behavior

| Method         | Purpose             |
| -------------- | ------------------- |
| `__len__`      | `len()`             |
| `__getitem__`  | Indexing `obj[key]` |
| `__setitem__`  | Assign to index     |
| `__delitem__`  | Delete item         |
| `__contains__` | `in` keyword        |
| `__iter__`     | Iteration           |
| `__next__`     | For iterators       |

---

##  Context Managers

| Method      | Purpose                  |
| ----------- | ------------------------ |
| `__enter__` | On entering `with` block |
| `__exit__`  | On exiting `with` block  |

---

##  Attribute Access

| Method             | Purpose                         |
| ------------------ | ------------------------------- |
| `__getattr__`      | Called for undefined attributes |
| `__getattribute__` | Called for all attribute access |
| `__setattr__`      | Assign attribute                |
| `__delattr__`      | Delete attribute                |
| `__dir__`          | Customize `dir()`               |

---

##  Callable and Descriptor Behavior

| Method       | Purpose                  |
| ------------ | ------------------------ |
| `__call__`   | Makes an object callable |
| `__get__`    | Descriptor get           |
| `__set__`    | Descriptor set           |
| `__delete__` | Descriptor delete        |

---

##  Miscellaneous

| Method            | Purpose                       |
| ----------------- | ----------------------------- |
| `__hash__`        | Returns hash value            |
| `__sizeof__`      | Returns size in bytes         |
| `__class__`       | Access to object's class      |
| `__doc__`         | Object's docstring            |
| `__name__`        | Name of module/function/class |
| `__module__`      | Module where defined          |
| `__annotations__` | Type annotations              |

