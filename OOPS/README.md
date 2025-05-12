# Object Oriented Programming (OOPS) in Python

Object Oriented Programming (OOP) is a programming paradigm that organizes code using objects and classes. It helps reduce code complexity, increases reusability, and makes programs more secure and maintainable.

## Table of Contents
- [What is OOP?](#what-is-oop)
- [Class and Object](#class-and-object)
- [The `self` Keyword](#the-self-keyword)
- [The `__init__` Method (Constructor)](#the-__init__-method-constructor)
- [Four Pillars of OOP](#four-pillars-of-oop)
  - [Inheritance](#inheritance)
  - [Abstraction](#abstraction)
  - [Encapsulation](#encapsulation)
  - [Polymorphism](#polymorphism)
- [Types of Methods](#types-of-methods)
- [Practice Examples](#practice-examples)

---

## What is OOP?
- **Object Oriented Programming** is a way to structure code using objects (instances of classes).
- **Benefits:**
  - Reduces code complexity
  - Promotes code reusability
  - Enhances security
  - Makes code easier to maintain
- **Four Pillars:**
  - Inheritance
  - Abstraction
  - Encapsulation
  - Polymorphism

---

## Class and Object
- **Class:** Blueprint for creating objects. Defines properties (attributes) and behaviors (methods).
- **Object:** Instance of a class. Represents a real-world entity.

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

my_car = Car('Toyota', 'Corolla')
print(my_car.brand)  # Output: Toyota
```

---

## The `self` Keyword
- Refers to the current instance of the class.
- Used to access variables and methods within the class.
- Not a reserved word, but a convention.

```python
class Example:
    def show(self):
        print('This is self:', self)
```

---

## The `__init__` Method (Constructor)
- Special method called when an object is created.
- Used to initialize instance variables.

```python
class Person:
    def __init__(self, name):
        self.name = name

p = Person('Alice')
print(p.name)  # Output: Alice
```

---

## Four Pillars of OOP

### Inheritance
- Allows a class (child) to inherit properties and methods from another class (parent).
- Promotes code reuse.

```python
class Animal:
    def speak(self):
        print('Animal speaks')

class Dog(Animal):
    def speak(self):
        print('Dog barks')

d = Dog()
d.speak()  # Output: Dog barks
```

**Types of Inheritance:**
- Single
- Multiple
- Multilevel
- Hierarchical

### Abstraction
- Hides complex implementation details and shows only the necessary features.
- Achieved using abstract classes and methods (with `abc` module).

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        return 3.14 * 5 * 5
```

### Encapsulation
- Restricts direct access to some of an object's components.
- Achieved by using private variables and methods (prefix with `__`).

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # private variable
    def get_balance(self):
        return self.__balance

acc = BankAccount(1000)
print(acc.get_balance())  # Output: 1000
# print(acc.__balance)  # Error
```

**Name Mangling:**
- Access private members: `object._ClassName__privatevar`

### Polymorphism
- Means 'many forms'.
- Same method name behaves differently in different classes.
- Achieved via method overriding.

```python
class Bird:
    def fly(self):
        print('Bird can fly')

class Ostrich(Bird):
    def fly(self):
        print('Ostrich cannot fly')

b = Bird()
o = Ostrich()
b.fly()  # Output: Bird can fly
o.fly()  # Output: Ostrich cannot fly
```

---

## Types of Methods
- **Instance Method:** Uses `self`, operates on instance variables.
- **Class Method:** Uses `@classmethod` and `cls`, operates on class variables.
- **Static Method:** Uses `@staticmethod`, does not operate on instance/class variables.

```python
class Demo:
    class_var = 'class variable'
    def instance_method(self):
        print('Instance method')
    @classmethod
    def class_method(cls):
        print('Class method:', cls.class_var)
    @staticmethod
    def static_method():
        print('Static method')
```

---

## Practice Examples
Try creating your own classes and objects, and experiment with inheritance, encapsulation, abstraction, and polymorphism!

---

**Happy Learning OOPS in Python!**
