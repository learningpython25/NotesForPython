| Variable Type         | Defined Where                    | Shared By                       |
| --------------------- | -------------------------------- | ------------------------------- |
| **Instance Variable** | Inside `__init__()` using `self` | Only that specific object       |
| **Class Variable**    | Directly inside the class        | Shared across **all instances** |

---

## Instance Variable

* Belongs **only to the object** (instance)
* Defined as `self.variable`
* Different for each object

```python
class Dog:
    def __init__(self, name):
        self.name = name  # instance variable

d1 = Dog("Buddy")
d2 = Dog("Max")

print(d1.name)  # Buddy
print(d2.name)  # Max
```

> 🎯 **Output:**

```
Buddy
Max
```

---

## Class Variable

* Belongs to the **class itself**
* Defined **outside any method** in the class
* Shared by **all instances**

```python
class Dog:
    species = "Canine"  # class variable

    def __init__(self, name):
        self.name = name  # instance variable

d1 = Dog("Buddy")
d2 = Dog("Max")

print(d1.species)  # Canine
print(d2.species)  # Canine
```

> 🎯 **Output:**

```
Canine
Canine
```

---

## 🔁 Shadowing Class Variable (Creating Instance Variable with Same Name)

```python
d1.species = "Wolf"  # This creates a new instance variable, doesn't change class var

print(d1.species)  # Wolf
print(d2.species)  # Canine
print(Dog.species) # Canine
```

> 🎯 **Output:**

```
Wolf
Canine
Canine
```

---

## 🧪 Inspecting Internals

```python
print(d1.__dict__)
print(Dog.__dict__)
```

> 🎯 **Output:**

```
{'name': 'Buddy', 'species': 'Wolf'}
{'__module__': '__main__', 'species': 'Canine', ...}
```

---

## 📌 Summary Table

| Feature            | Instance Variable         | Class Variable                 |
| ------------------ | ------------------------- | ------------------------------ |
| Belongs to         | One object                | The class                      |
| Defined in         | `__init__` via `self.var` | At class level                 |
| Stored in          | `object.__dict__`         | `class.__dict__`               |
| Shared across      | ❌ No                      | ✅ Yes                          |
| Can be overridden? | ✅ Yes                     | ✅ But creates new instance var |
