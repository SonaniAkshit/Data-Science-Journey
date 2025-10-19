# 🧠 Python Basics in Data Science

### 1. **Variables**

**Why:**
Variables are the building blocks of any Python program. They store data that you later manipulate or analyze.
**How in Data Science:**
Used to store dataset paths, configuration values, model parameters, and results like mean, accuracy, etc.

**Example:**

```python
dataset_path = "sales_data.csv"
learning_rate = 0.01
```

---

### 2. **Data Types**

**Why:**
Each type (int, float, string, bool, list, dict, etc.) defines how data behaves. Understanding types ensures correct operations on data.
**How in Data Science:**
When analyzing data, you must convert between numeric, categorical, and text types for cleaning and model training.

**Example:**

```python
age = 25          # int
height = 5.8      # float
is_male = True    # bool
name = "Akshit"   # string
```

---

### 3. **Conditionals**

**Why:**
Conditionals let you control logic flow — “if this, then that.”
**How in Data Science:**
Used in feature engineering, decision making, and error handling.

**Example:**

```python
if accuracy > 0.9:
    print("Excellent model!")
else:
    print("Needs improvement.")
```

---

### 4. **Loops**

**Why:**
Loops are used to repeat actions efficiently without rewriting code.
**How in Data Science:**
Used to iterate through datasets, run multiple model tests, or process rows in a DataFrame.

**Example:**

```python
for col in df.columns:
    print(col, df[col].isnull().sum())
```

---

### 5. **Input/Output**

**Why:**
Every project interacts with data — from reading files to displaying outputs.
**How in Data Science:**
Used to import datasets (CSV, JSON), display summaries, and save analysis results.

**Example:**

```python
name = input("Enter your name: ")
print(f"Welcome, {name}")
```

---

## 💼 50 Professional Python Interview Questions with Answers

(Covering Variables, Loops, Conditionals, I/O, Data Types)

---

### 🔹 **Variables (1–10)**

**1. What is a variable in Python?**
A variable is a named memory location used to store data that can change during program execution.

**2. How do you declare a variable in Python?**
Simply assign a value:

```python
x = 10
name = "Akshit"
```

**3. What are variable naming rules in Python?**

* Must start with a letter or underscore.
* Cannot start with a number.
* Cannot use special characters or keywords.

**4. What is dynamic typing in Python?**
Python automatically assigns data type at runtime, so you don’t need to declare it.

**5. What is variable scope?**
The area in which a variable is accessible — global, local, or nonlocal.

**6. How to check variable type?**
Using `type()` function:

```python
type(x)
```

**7. What are global variables?**
Variables defined outside a function, accessible throughout the program.

**8. What are local variables?**
Variables declared inside a function, accessible only within it.

**9. What happens if you assign a new value to a variable?**
The old value is overwritten and replaced with the new one.

**10. What is the difference between mutable and immutable variables?**
Mutable objects can change (e.g., lists), while immutable objects cannot (e.g., strings, tuples).

---

### 🔹 **Data Types (11–20)**

**11. What are Python’s built-in data types?**
`int`, `float`, `bool`, `str`, `list`, `tuple`, `set`, `dict`, `complex`.

**12. How do you convert data types in Python?**
Using casting functions like `int()`, `float()`, `str()`.

**13. What is a list?**
A mutable, ordered collection of elements.

```python
fruits = ["apple", "banana", "cherry"]
```

**14. What is a tuple?**
An immutable, ordered collection.

```python
data = (10, 20, 30)
```

**15. What is a set?**
An unordered collection of unique elements.

```python
ids = {1, 2, 3, 2}  # Output: {1, 2, 3}
```

**16. What is a dictionary?**
A key-value mapping structure.

```python
student = {"name": "Akshit", "age": 22}
```

**17. What’s the difference between list and tuple?**
List is mutable; tuple is immutable.

**18. How can you check data type?**
Use `type(variable)`.

**19. What are numeric data types in Python?**
`int`, `float`, `complex`.

**20. How to convert a string number to integer?**

```python
int("25")  # returns 25
```

---

### 🔹 **Conditionals (21–30)**

**21. What are conditional statements?**
Used to execute blocks of code based on conditions (`if`, `elif`, `else`).

**22. What’s the syntax for an if statement?**

```python
if condition:
    statement
```

**23. What’s the difference between `if` and `elif`?**
`elif` checks the next condition only if previous conditions are false.

**24. Can you use `if` without `else`?**
Yes, `else` is optional.

**25. How to write a nested if statement?**

```python
if x > 0:
    if x < 10:
        print("Single digit positive number")
```

**26. What is a ternary operator in Python?**
A single-line if-else:

```python
msg = "Even" if num % 2 == 0 else "Odd"
```

**27. Can you use logical operators in conditions?**
Yes — `and`, `or`, `not`.

**28. What happens if condition evaluates to non-boolean?**
Python treats non-zero or non-empty as True.

**29. What is `pass` used for?**
It acts as a placeholder for empty blocks.

**30. What is `assert` used for?**
Used to test if a condition is true; raises an error otherwise.

---

### 🔹 **Loops (31–40)**

**31. What types of loops exist in Python?**
`for` and `while`.

**32. How does a for loop work?**
Iterates over a sequence (like list, tuple, string).

**33. Example of a for loop:**

```python
for i in range(5):
    print(i)
```

**34. Example of a while loop:**

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

**35. What is the difference between for and while loops?**
For loop is used with known iterations; while loop with conditions.

**36. What does `break` do?**
Exits the loop immediately.

**37. What does `continue` do?**
Skips current iteration and moves to next.

**38. What is a nested loop?**
A loop inside another loop.

**39. What happens if the while loop condition is always true?**
It creates an infinite loop.

**40. What’s the use of `else` in loops?**
Executes when the loop completes normally without `break`.

---

### 🔹 **Input/Output (41–50)**

**41. How to take user input in Python?**
Using `input()` function.

**42. What type does `input()` return?**
Always returns a string.

**43. How to read integer input?**

```python
age = int(input("Enter age: "))
```

**44. How to print output?**
Using `print()` function.

**45. How to format output in Python 3?**
Using f-strings:

```python
print(f"Name: {name}, Age: {age}")
```

**46. How to read a file?**

```python
with open("data.txt", "r") as f:
    print(f.read())
```

**47. How to write to a file?**

```python
with open("data.txt", "w") as f:
    f.write("Hello!")
```

**48. What does `with open()` do?**
Automatically closes the file after use.

**49. How to print without newline?**

```python
print("Hello", end=" ")
print("World")
```

**50. How to print multiple variables together?**

```python
print(name, age, city)
```

---