**Multiple Inheritance** means a class can inherit from **more than one parent class**.

```python
class Child(Parent1, Parent2):
    pass
```

* The child class gets **attributes and methods** from **all parent classes**.
* Python handles this using the **Method Resolution Order (MRO)**.

---

## Basic Example

```python
class Father:
    def skills(self):
        return "Gardening, Driving"

class Mother:
    def skills(self):
        return "Cooking, Painting"

class Child(Father, Mother):
    pass

c = Child()
print(c.skills())
```

> 🎯 **Output:**

```
Gardening, Driving
```

> 📌 Python uses **MRO** and picks `skills()` from the **first parent** (`Father`) listed.

---

## Overriding in Child Class

```python
class Child(Father, Mother):
    def skills(self):
        return "Programming, " + super().skills()

c = Child()
print(c.skills())
```

> 🎯 **Output:**

```
Programming, Gardening, Driving
```

---

## MRO (Method Resolution Order)

You can check the order Python follows using:

```python
print(Child.__mro__)
```

> 🎯 **Output:**

```
(<class '__main__.Child'>, <class '__main__.Father'>, <class '__main__.Mother'>, <class 'object'>)
```

---

## Diamond Problem & MRO

### 🔸 Diamond Inheritance

```python
class A:
    def show(self):
        print("A")

class B(A):
    def show(self):
        print("B")

class C(A):
    def show(self):
        print("C")

class D(B, C):
    pass

d = D()
d.show()
```

> 🎯 **Output:**

```
B
```

> ✅ Python resolves this via **C3 Linearization** (left-to-right depth-first).

```python
print(D.__mro__)
```

> 🎯 Output:

```
(<class '__main__.D'>, <class '__main__.B'>, <class '__main__.C'>, <class '__main__.A'>, <class 'object'>)
```

---

## Summary

* Python supports multiple inheritance directly.
* MRO helps Python decide **which method to call first**.
* You can use `super()` to extend the behavior of parent classes.
