
**Abstract Base Classes (ABCs)** are classes that **cannot be instantiated directly**. They are meant to be **inherited**, and they define a **common interface** for other classes.

They are used to **enforce a contract** — ensuring that child classes implement specific methods.

---

### Why use ABCs?

* To define a **blueprint** for other classes.
* To provide a **consistent API** across subclasses.
* To enforce the implementation of **certain methods** in derived classes.

---

### How to Create an Abstract Base Class

You need:

1. The `abc` module
2. `ABC` as the base class
3. Decorator `@abstractmethod` for methods that must be overridden

```python
from abc import ABC, abstractmethod

class Animal(ABC):  # Abstract Base Class
    @abstractmethod
    def make_sound(self):  # Abstract Method
        pass
```

> 🔒 **You cannot instantiate `Animal`** unless `make_sound()` is implemented.

---

### Usage Example

```python
class Dog(Animal):
    def make_sound(self):
        return "Woof!"

class Cat(Animal):
    def make_sound(self):
        return "Meow"

# Valid
dog = Dog()
print(dog.make_sound())  # Output: Woof!

# Invalid
# animal = Animal()  # ❌ TypeError: Can't instantiate abstract class
```

---

### Summary

| Concept                      | Description                                           |
| ---------------------------- | ----------------------------------------------------- |
| `ABC`                        | Base class for defining abstract base classes         |
| `@abstractmethod`            | Marks a method that **must be implemented**           |
| Cannot instantiate           | Abstract classes **cannot be directly instantiated**  |
| Can include concrete methods | ABCs **can also have regular (non-abstract) methods** |
