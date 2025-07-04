
### Encapsulation

> **Encapsulation = Hiding *data*** (internal state)
> It’s about **restricting access** to internal variables or methods of a class and exposing only what’s necessary.

* Achieved using **private (`_var`, `__var`) or protected** attributes/methods.
* Provides **data protection** and ensures **controlled access**.

#### Example:

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner        # public
        self.__balance = balance  # private

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def get_balance(self):
        return self.__balance
```

* You **cannot access `__balance` directly** from outside.
* You **must use `get_balance()`**, which is controlled.

---

### Abstraction

> **Abstraction = Hiding *implementation details***
> It focuses on **exposing essential features only**, without showing *how* they are implemented.

* Implemented via **classes, interfaces (abstract base classes)**, and **methods that are expected to be overridden**.
* Promotes **simplicity** and **flexibility** in code.

#### Example:

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius * self.radius
```

* The user knows every shape will have an `area()` method but **doesn’t care how it is calculated**.
* The implementation of `area()` is **abstracted** away.

---

### Summary 

| Feature      | Encapsulation                  | Abstraction                          |
| ------------ | ------------------------------ | ------------------------------------ |
| Hides        | Internal data                  | Internal implementation              |
| Focus        | Data protection                | Functionality design                 |
| Access       | Uses private/protected members | Uses abstract classes and interfaces |
| Goal         | Restrict unauthorized access   | Reduce complexity for users          |
| Python Tools | `_var`, `__var`, methods       | `abc` module, `@abstractmethod`      |

