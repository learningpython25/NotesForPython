
- OOPs is all about *objects* and *classes*
- Each *object* is an instance of a *class*
- Variables of a class are usually referred to as *parameters, attibutes or data members*
- Functions of a class are usually referred to as *methods or member functions*
- The main purpose and reason behind Object Oriented design is
	- Modularity
	- Abstraction
		- This gives rise to ADT `Abstract Data Types`. Tell what it can do, but not how
	- Encapsulation



**Object-Oriented Programming (OOP)** is a programming paradigm that organizes code using **objects** and **classes**.

It helps model real-world entities and promotes **code reuse**, **modularity**, and **encapsulation**.

---

## Key Concepts of OOP

### 1. **Class**

A blueprint for creating objects.

```python
class Dog:
    pass
```

### 2. **Object**

An instance of a class.

```python
my_dog = Dog()
```

### 3. **Attributes**

Variables that belong to a class or object.

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

### 4. **Methods**

Functions defined inside a class.

```python
class Dog:
    def bark(self):
        print("Woof!")
```

---

## 🔹 Four Pillars of OOP

###  1. **Encapsulation**

* Hides internal state of the object.
* Protects data using **private/protected variables**.

```python
class BankAccount:
    def __init__(self):
        self.__balance = 0

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance
```

---

### 2. **Abstraction**

* Hides complex implementation and shows only necessary parts.
* Achieved using **abstract base classes**.

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        pass
```

---

### 3. **Inheritance**

* One class (child) inherits from another (parent).
* Promotes **code reuse**.

```python
class Animal:
    def speak(self):
        print("Makes sound")

class Dog(Animal):
    def speak(self):
        print("Barks")
```

---

### 4. **Polymorphism**

* Same interface, different implementations.

```python
for animal in [Dog(), Cat()]:
    animal.speak()  # Output differs based on the object
```

---

## Class vs Instance Variables

| Feature    | Class Variable    | Instance Variable             |
| ---------- | ----------------- | ----------------------------- |
| Defined at | Class level       | Inside constructor `__init__` |
| Shared by  | All instances     | Unique to each instance       |
| Example    | `species = "Dog"` | `self.name = name`            |

---

## Example OOP Structure

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

d = Dog("Buddy")
print(d.speak())  # Buddy says Woof!
```

