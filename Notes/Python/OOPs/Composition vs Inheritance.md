### ✅ Inheritance – "is-a" Relationship

```python
class Animal:
    def speak(self):
        return "Some sound"

class Dog(Animal):
    def speak(self):
        return "Bark"

d = Dog()
print(d.speak())  # Bark
```

* `Dog` **is a** type of `Animal`
* Reuse via method overriding

---

### ✅ Composition – "has-a" Relationship

```python
class Engine:
    def start(self):
        return "Engine started"

class Car:
    def __init__(self):
        self.engine = Engine()  # has-a Engine

    def start(self):
        return self.engine.start() + " in Car"

c = Car()
print(c.start())  # Engine started in Car
```

* `Car` **has a** `Engine`
* Flexible, avoids tight coupling from inheritance

---

## 📌 When to Use

| Pattern     | Use When                       |
| ----------- | ------------------------------ |
| Inheritance | Subclass **is-a** superclass   |
| Composition | One class **uses/has** another |
