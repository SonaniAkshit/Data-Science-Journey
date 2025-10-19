# 🧠 Python Object-Oriented Programming (OOP)

---

## 💡 What is OOP?

**OOP (Object-Oriented Programming)** is a paradigm that structures code around **objects** and **classes**, rather than functions alone.
Objects combine **data (attributes)** and **behavior (methods)** together — making code reusable, modular, and scalable.

---

## 🔹 Why OOP for Data Science?

In data science, you often build **pipelines**, **custom models**, and **data structures**.
OOP helps you:

* Structure complex ML or ETL code cleanly
* Build reusable components (data loaders, preprocessors, model wrappers)
* Reduce redundancy and improve collaboration

For example: you can create a `DataCleaner` class or `ModelTrainer` class with methods like `train()`, `evaluate()`, `save()` etc.

---

## 🔸 Core OOP Concepts in Python

---

### 1. **Class and Object**

**What:**
A class is a **blueprint**; an object is an **instance** of that class.

**How (Code):**

```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

    def show(self):
        print(f"{self.color} {self.brand}")

# Object
car1 = Car("Tesla", "Red")
car1.show()
```

**Why (Data Science):**
You can model datasets or models as objects (e.g., `Dataset`, `NeuralNetwork`), each having properties and functions.

---

### 2. **`__init__` Constructor**

**What:**
Special method called automatically when creating an object — used for initialization.

**How:**

```python
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks
```

**Why:**
Automatically prepares object with required parameters (like data files, models, etc.) at creation.

---

### 3. **Instance Variables & Methods**

**What:**
Variables & methods tied to a specific object (accessed with `self`).

**How:**

```python
class Person:
    def __init__(self, name):
        self.name = name
```

**Why:**
Every dataset/model instance can maintain its own state or parameters.

---

### 4. **Class Variables & Methods**

**What:**
Variables shared by all instances.
Use `@classmethod` for class-level operations.

**How:**

```python
class Employee:
    company = "Google"  # class variable
    def __init__(self, name):
        self.name = name
```

**Why:**
For global constants (e.g., learning rate, model version, etc.) shared across all objects.

---

### 5. **Static Methods**

**What:**
Methods that do not depend on instance or class variables.

**How:**

```python
class MathOps:
    @staticmethod
    def square(x):
        return x*x
```

**Why:**
Useful for data utility functions like scaling, normalization, etc.

---

### 6. **Encapsulation**

**What:**
Hiding internal data from direct modification; achieved using `_` or `__` prefix.

**How:**

```python
class Account:
    def __init__(self):
        self.__balance = 1000
```

**Why:**
Protect sensitive data like configurations, API keys, or credentials in ML pipelines.

---

### 7. **Inheritance**

**What:**
Allows a class to use methods and attributes of another class.

**How:**

```python
class Animal:
    def speak(self):
        print("Animal sound")

class Dog(Animal):
    def speak(self):
        print("Bark")
```

**Why:**
Create specialized classes (e.g., `LinearRegression`, `LogisticRegression`) that inherit from a base `Model` class.

---

### 8. **Polymorphism**

**What:**
Same method name, different implementations depending on class.

**How:**

```python
for animal in [Dog(), Cat()]:
    animal.speak()
```

**Why:**
You can handle different ML models or datasets uniformly.

---

### 9. **Abstraction**

**What:**
Hiding implementation details; only showing essential info.

**How:**

```python
from abc import ABC, abstractmethod
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass
```

**Why:**
Create base classes for models or data pipelines with mandatory method definitions.

---

### 10. **Magic (Dunder) Methods**

**What:**
Built-in double-underscore methods like `__str__`, `__len__`, `__add__`, etc.

**How:**

```python
class Vector:
    def __init__(self, x):
        self.x = x
    def __add__(self, other):
        return self.x + other.x
```

**Why:**
Allows custom behavior for data objects (e.g., vector addition, matrix operations).

---

### 11. **Composition**

**What:**
Using objects of one class inside another.

**How:**

```python
class Engine:
    def start(self): print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()
```

**Why:**
Modularizes code (e.g., `Pipeline` having `Preprocessor`, `Model`, `Evaluator`).

---

### 12. **Object Introspection**

**What:**
Inspecting object properties/methods dynamically (`type()`, `dir()`, `id()`, etc.)

**How:**

```python
print(type(car1))
print(dir(car1))
```

**Why:**
Useful for debugging large codebases or checking model attributes dynamically.

---

---

# 🎯 50 Interview Questions & Professional Answers

---

## 📘 **OOP Basics (Q1–Q10)**

**Q1. What is OOP?**
**A:** OOP stands for Object-Oriented Programming, focusing on creating objects that contain both data and methods.

---

**Q2. What is a class in Python?**
**A:** A class is a user-defined blueprint for creating objects with specific attributes and methods.

---

**Q3. What is an object?**
**A:** An instance of a class — a real implementation of the blueprint.

---

**Q4. What is `self` in Python classes?**
**A:** `self` refers to the current instance of the class — used to access attributes and methods.

---

**Q5. What is a constructor?**
**A:** The `__init__()` method that automatically executes when an object is created.

---

**Q6. Can you have multiple constructors in Python?**
**A:** Python supports only one `__init__`, but you can use default arguments or class methods to simulate multiple constructors.

---

**Q7. What are instance variables?**
**A:** Variables unique to each object; defined inside `__init__`.

---

**Q8. What is a class variable?**
**A:** A variable shared among all class objects.

---

**Q9. How do you create a static method?**
**A:** Use `@staticmethod` decorator.

---

**Q10. What is encapsulation?**
**A:** Restricting access to internal variables using `_` or `__` to protect data.

---

## 🧩 **Inheritance & Polymorphism (Q11–Q25)**

**Q11. What is inheritance?**
**A:** Deriving a new class from an existing one to reuse code.

---

**Q12. What are types of inheritance in Python?**
**A:** Single, Multiple, Multilevel, Hierarchical, and Hybrid.

---

**Q13. What’s the syntax for inheritance?**
**A:**

```python
class Child(Parent):
    pass
```

---

**Q14. What is method overriding?**
**A:** Redefining a parent class method in a child class.

---

**Q15. What is polymorphism?**
**A:** Same method name with different behaviors in different classes.

---

**Q16. How is polymorphism implemented in Python?**
**A:** Through method overriding or operator overloading.

---

**Q17. What is operator overloading?**
**A:** Using special methods like `__add__` to define custom operations between objects.

---

**Q18. What are abstract classes?**
**A:** Classes that cannot be instantiated; define abstract methods that must be implemented in subclasses.

---

**Q19. What is the purpose of `super()`?**
**A:** To call a parent class method or constructor.

---

**Q20. Can Python support multiple inheritance?**
**A:** Yes, a class can inherit from multiple parent classes.

---

**Q21. How to check if a class inherits another?**
**A:** Using `issubclass(Child, Parent)` or `isinstance(obj, Class)`.

---

**Q22. Why is polymorphism important in ML pipelines?**
**A:** Different models (Regression, DecisionTree, etc.) can be called with the same `fit()` or `predict()` interface.

---

**Q23. What is the difference between inheritance and composition?**
**A:** Inheritance extends a class; composition uses a class inside another.

---

**Q24. Can you override `__str__`?**
**A:** Yes, to return a readable string for your object.

---

**Q25. What happens if you don’t call `super().__init__()` in child?**
**A:** Parent attributes won’t initialize.

---

## 🧱 **Encapsulation, Abstraction, Magic Methods (Q26–Q40)**

**Q26. What is name mangling in Python?**
**A:** Python internally renames private attributes with `_ClassName__attribute`.

---

**Q27. How do you define private variables?**
**A:** Prefix with double underscores: `__balance`.

---

**Q28. What is abstraction?**
**A:** Hiding implementation details using abstract base classes.

---

**Q29. What is `ABC` module?**
**A:** Used for defining abstract base classes.

---

**Q30. What is a magic method?**
**A:** Predefined methods with `__` syntax (e.g., `__len__`, `__add__`, `__str__`).

---

**Q31. Example of `__str__` method?**
**A:**

```python
def __str__(self):
    return f"Name: {self.name}"
```

---

**Q32. What is `__repr__`?**
**A:** Returns an official string representation of the object (used for debugging).

---

**Q33. What’s the difference between `__eq__` and `__add__`?**
**A:** `__eq__` defines equality (`==`), `__add__` defines addition (`+`).

---

**Q34. What is multiple inheritance’s challenge?**
**A:** Ambiguity in method resolution; Python uses MRO (Method Resolution Order).

---

**Q35. What is `super()`’s role in MRO?**
**A:** Ensures the next parent method in MRO is called properly.

---

**Q36. What is `dir()` used for?**
**A:** Lists all available attributes and methods of an object.

---

**Q37. What is `hasattr()` and `getattr()`?**
**A:** Used to dynamically check or fetch attributes from objects.

---

**Q38. Can you delete an object in Python?**
**A:** Yes, using `del object_name`.

---

**Q39. How does garbage collection work?**
**A:** Python automatically frees memory for unreferenced objects.

---

**Q40. What is duck typing?**
**A:** “If it walks like a duck, it’s a duck” — Python focuses on object behavior, not type.

---

## 🔧 **Advanced + Data Science (Q41–Q50)**

**Q41. How OOP improves ML project structure?**
**A:** Helps organize code into reusable model classes and preprocessing modules.

---

**Q42. Example of class in ML pipeline?**
**A:**

```python
class Model:
    def train(self): pass
    def predict(self): pass
```

---

**Q43. How can inheritance simplify model training?**
**A:** A base `Model` class can define `fit()`, `evaluate()`, and each subclass customizes them.

---

**Q44. Why is encapsulation critical in pipelines?**
**A:** Prevents unauthorized changes to sensitive configurations (e.g., data paths, credentials).

---

**Q45. How can OOP help build reusable ETL pipelines?**
**A:** Each stage (Extract, Transform, Load) can be separate classes with shared parent logic.

---

**Q46. Why are abstract classes used in ML projects?**
**A:** Define a uniform structure for all models (e.g., all must implement `train()` and `predict()`).

---

**Q47. How does polymorphism enable model switching?**
**A:** You can switch models easily as long as they share same interface.

---

**Q48. What OOP features are used in sklearn library?**
**A:** Classes, inheritance, encapsulation — every model (like `LinearRegression`) inherits from a common estimator base class.

---

**Q49. Why prefer OOP over functional programming in ML?**
**A:** OOP is better for large, modular, maintainable systems; functions alone are fine for small scripts.

---

**Q50. How would you design a `DataPreprocessor` class?**
**A:**

```python
class DataPreprocessor:
    def __init__(self, df):
        self.df = df
    def clean(self):
        ...
    def normalize(self):
        ...
```

This modularizes and reuses preprocessing steps efficiently.

---