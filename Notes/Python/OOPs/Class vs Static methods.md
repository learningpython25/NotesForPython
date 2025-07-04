### `@classmethod`

* Receives **class (`cls`)** as the first argument.
* Can **access or modify class-level data**.
* Useful for **alternative constructors** or factory methods.

```python
class Person:
    count = 0

    def __init__(self, name):
        self.name = name
        Person.count += 1

    @classmethod
    def total_people(cls):
        return cls.count

p1 = Person("Alice")
p2 = Person("Bob")
print(Person.total_people())  # 2
```

---

### `@staticmethod`

* Receives **no `self` or `cls`**.
* Like a **normal function**, just namespaced inside a class.
* Used when the method doesn’t need object or class context.

```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b

print(Math.add(3, 4))  # 7
```

