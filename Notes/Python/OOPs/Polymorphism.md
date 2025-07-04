## What is Polymorphism?

**Polymorphism** means “many forms.”
In programming, it refers to the ability of different **objects** to respond to the **same method call** in a way specific to their type.

---

## Why Use Polymorphism?

* Promotes **flexibility** and **extensibility**
* Simplifies **interface design**
* Avoids excessive conditionals (`if/else`, `type()` checks)

---

## Types of Polymorphism in Python

### 1. **Duck Typing (Dynamic Typing)**

"If it walks like a duck and quacks like a duck, it’s a duck."

```python
class Cat:
    def speak(self):
        return "Meow"

class Dog:
    def speak(self):
        return "Woof"

def animal_sound(animal):
    print(animal.speak())

# Output
animal_sound(Cat())   # Meow
animal_sound(Dog())   # Woof
```

---

### 2. **Method Overriding (In Inheritance)**

```python
class Animal:
    def speak(self):
        return "Some sound"

class Dog(Animal):
    def speak(self):
        return "Bark"

class Cat(Animal):
    def speak(self):
        return "Meow"

animals = [Dog(), Cat()]

for a in animals:
    print(a.speak())

# Output:
# Bark
# Meow
```

* Base class defines a method (`speak`)
* Subclasses **override** it with specific behavior

---

### 3. **Built-in Polymorphism (Function Overloading-Like Behavior)**

```python
print(len("Hello"))    # 5 (string)
print(len([1, 2, 3]))   # 3 (list)
print(len({'a': 1}))    # 1 (dict)
```

* `len()` behaves differently depending on the object type

---

### 4. **Operator Overloading (Magic Methods)**

```python
class Book:
    def __init__(self, pages):
        self.pages = pages

    def __add__(self, other):
        return self.pages + other.pages

b1 = Book(100)
b2 = Book(150)

print(b1 + b2)  # 250
```

* `+` is **overloaded** to work with custom objects using `__add__`

---

## Summary 

| Type                   | Description                      | Example       |
| ---------------------- | -------------------------------- | ------------- |
| Duck Typing            | Same method name, any object     | `speak()`     |
| Method Overriding      | Inheritance-based redefinition   | `Dog.speak()` |
| Built-in Function Poly | Function behaves based on input  | `len()`       |
| Operator Overloading   | Magic methods redefine operators | `__add__`     |

---

## Benefits of Polymorphism

* Cleaner and more **abstract** code
* Avoids redundant function names like `draw_circle()`, `draw_square()`
* Lets you treat different objects **uniformly**
