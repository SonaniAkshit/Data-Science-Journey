# 🧠 Python File handling, error handling, modules, comprehensions

---

### 1. **File Handling**

#### 🟢 What:

File handling means **reading from and writing to files** (like `.txt`, `.csv`, `.json`, etc.) using Python.
It allows your programs to **store, access, and manage data persistently** — outside the program’s memory.

#### 🔵 Why (in Data Science):

* You’ll constantly work with data files — CSV datasets, logs, configuration files, etc.
* Python file handling helps you import datasets, save model outputs, and log your results.
* Example: reading training data, saving predictions, or exporting cleaned data.

#### 🟣 How:

You use Python’s built-in `open()` function to handle files.
Modes:

* `'r'` → read
* `'w'` → write (overwrite)
* `'a'` → append
* `'rb'`, `'wb'` → binary

**Example:**

```python
# Write to a file
with open("data.txt", "w") as f:
    f.write("Hello Akshit!")

# Read from a file
with open("data.txt", "r") as f:
    content = f.read()
    print(content)
```

✅ The `with` keyword auto-closes files (good practice).

---

### 2. **Error Handling (Exception Handling)**

#### 🟢 What:

Error handling in Python refers to using `try-except` blocks to **gracefully manage runtime errors** instead of crashing the program.

#### 🔵 Why (in Data Science):

When processing datasets, you may encounter:

* Missing files
* Wrong data formats
* Divide-by-zero or invalid conversions

Error handling ensures your data pipeline **doesn’t stop** and **handles exceptions intelligently**.

#### 🟣 How:

Use `try-except`, and optionally `finally` or `else`.

**Example:**

```python
try:
    num = int(input("Enter a number: "))
    print(10 / num)
except ValueError:
    print("Invalid input! Please enter a number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
finally:
    print("Process completed.")
```

✅ This ensures robustness in data pipelines and model training scripts.

---

### 3. **Modules**

#### 🟢 What:

A **module** is a file containing Python code — functions, classes, or variables — that you can **import and reuse**.
Even Python’s standard libraries (`math`, `os`, `json`, `random`, etc.) are modules.

#### 🔵 Why (in Data Science):

* Keeps your code **modular, organized, and reusable**.
* You’ll often create modules for cleaning, visualization, or model-building functions.
* Also allows you to use **third-party data science libraries** like `numpy`, `pandas`, `matplotlib`.

#### 🟣 How:

You can **import** modules or create your own.

**Example 1 – Importing Built-in Modules:**

```python
import math
print(math.sqrt(25))
```

**Example 2 – Custom Module:**
*File: math_utils.py*

```python
def square(x):
    return x**2
```

*Use in main program:*

```python
import math_utils
print(math_utils.square(4))
```

✅ This structure is used everywhere — from simple scripts to large ML projects.

---

### 4. **Comprehensions (List, Dict, Set Comprehensions)**

#### 🟢 What:

Comprehensions are **shortcuts for creating collections (lists, dicts, sets)** in a clean, one-line syntax — instead of using loops.

#### 🔵 Why (in Data Science):

* Makes code **faster, cleaner, and more readable**.
* Commonly used for **data transformations** like filtering, squaring, mapping values, etc.
* Example: quickly processing all dataset entries in one line.

#### 🟣 How:

**List Comprehension:**

```python
squares = [x**2 for x in range(5)]
```

**Dict Comprehension:**

```python
squares_dict = {x: x**2 for x in range(5)}
```

**Set Comprehension:**

```python
unique_lengths = {len(word) for word in ["Akshit", "Data", "Science"]}
```

✅ Comprehensions are Pythonic and extremely efficient — used heavily in Pandas, Numpy, and ML preprocessing.

---

### ⚡ Quick Summary Table

| Concept            | What It Is            | Why Important (Data Science)  | How Used                        |
| ------------------ | --------------------- | ----------------------------- | ------------------------------- |
| **File Handling**  | Reading/writing files | Load datasets, save results   | `open()`, `with open()`         |
| **Error Handling** | Manage runtime errors | Prevent data pipeline crashes | `try-except`                    |
| **Modules**        | Reusable code files   | Modular project structure     | `import`, `from ... import ...` |
| **Comprehensions** | One-line loops        | Fast data transformation      | `[x for x in data if ...]`      |

---


## 🧠 Deep Topics:

**File Handling, Error Handling, Modules, Comprehensions**
---

### 🗂️ 1. File Handling

**🔹 What:**
File handling allows Python programs to **read, write, and manage files** (like `.csv`, `.txt`, `.json`, etc.).

**🔹 Why (for Data Science):**
Most datasets are stored in **files** — CSVs, JSON logs, Excel sheets, or text files.
Data scientists need to read/write files efficiently to:

* Load datasets for analysis (`open()`, `read()`, or using libraries like `pandas.read_csv()`)
* Save processed or cleaned data
* Log outputs or intermediate results

**🔹 How:**

* Open file → `file = open('data.txt', 'r')`
* Read → `file.read()` or `file.readlines()`
* Write → `file.write("Hello")`
* Close → `file.close()`
* Or use `with open('data.txt', 'r') as f:` (auto-closes file safely)

---

### ⚠️ 2. Error Handling

**🔹 What:**
Error handling helps **manage runtime errors** gracefully using `try`, `except`, `finally`, and `raise`.

**🔹 Why (for Data Science):**
When working with huge datasets, APIs, or user inputs — errors are **unavoidable**.
For example:

* A file may not exist (`FileNotFoundError`)
* Data may be missing (`KeyError`, `ValueError`)
* A network may fail when fetching data

Good error handling ensures your **data pipeline doesn’t crash** and can provide meaningful messages.

**🔹 How:**

```python
try:
    data = open("data.csv")
except FileNotFoundError:
    print("File not found. Please check the path.")
finally:
    print("Operation complete.")
```

You can also raise your own errors with `raise ValueError("Invalid input")`.

---

### 📦 3. Modules

**🔹 What:**
A **module** is a file containing Python code — functions, variables, or classes — that you can **reuse**.

**🔹 Why (for Data Science):**
Data scientists use tons of **Python modules/libraries** like:

* `math`, `os`, `sys` → built-in modules
* `numpy`, `pandas`, `matplotlib`, `seaborn` → data science libraries
  These modules make it easier to perform **complex operations with few lines of code**.

**🔹 How:**

* Importing a module → `import math`
* Using → `math.sqrt(16)`
* From specific function → `from math import sqrt`
* Custom module → write `mymodule.py`, then `import mymodule`

You can even install external ones using `pip install numpy`.

---

### ⚡ 4. Comprehensions

**🔹 What:**
Comprehensions are **concise ways to create lists, sets, or dictionaries** using a single line of code.

**🔹 Why (for Data Science):**
When cleaning or transforming data, comprehensions make code **faster, shorter, and more readable** — crucial when dealing with large datasets.

**🔹 How:**

```python
# List comprehension
squares = [x**2 for x in range(10)]

# Dictionary comprehension
square_dict = {x: x**2 for x in range(5)}

# Set comprehension
unique = {x for x in [1,2,2,3]}
```

They are faster than normal loops and ideal for filtering or transforming data columns.

---

✅ **Summary Table:**

| Topic          | What It Does               | Why It’s Important for Data Science | Example                |
| -------------- | -------------------------- | ----------------------------------- | ---------------------- |
| File Handling  | Manage files (read/write)  | Work with datasets & logs           | `open('data.csv')`     |
| Error Handling | Handle runtime errors      | Prevent pipeline crashes            | `try...except`         |
| Modules        | Reusable code/library      | Use powerful DS tools               | `import pandas as pd`  |
| Comprehensions | Short data creation syntax | Fast transformations                | `[x**2 for x in data]` |

---


# 🧠 Python Interview Q&A – File Handling | Error Handling | Modules | Comprehensions


## 📁 **File Handling (Q1–Q15)**

**Q1. What is file handling in Python?**
**A:** File handling allows Python programs to read, write, and manipulate external files (like `.txt`, `.csv`, `.json`) using built-in functions such as `open()`, `read()`, and `write()`.

---

**Q2. What are the different modes in file handling?**
**A:**

* `'r'`: Read (default)
* `'w'`: Write (overwrites existing file)
* `'a'`: Append (adds data to file end)
* `'r+'`: Read and write
* `'b'`: Binary mode
  Example: `open("data.txt", "rb")`.

---

**Q3. What is the purpose of the `with` statement in file handling?**
**A:** It automatically closes the file after the block executes — even if an error occurs.

```python
with open("data.txt", "r") as f:
    data = f.read()
```

---

**Q4. How can you read a large file efficiently?**
**A:** Use a loop with `readline()` or iterate directly over the file object:

```python
for line in open("large.txt"):
    process(line)
```

---

**Q5. How do you write data into a file?**
**A:**

```python
with open("output.txt", "w") as f:
    f.write("Data Science is awesome!")
```

---

**Q6. How do you append data to an existing file?**
**A:** Use `'a'` mode:

```python
with open("log.txt", "a") as f:
    f.write("\nNew entry added.")
```

---

**Q7. How can you read all lines at once?**
**A:** Use `readlines()`:

```python
lines = open("data.txt").readlines()
```

---

**Q8. What happens if you open a non-existent file in read mode?**
**A:** It raises a `FileNotFoundError`.

---

**Q9. How do you check if a file exists before opening it?**
**A:**

```python
import os
if os.path.exists("data.txt"):
    print("File found.")
```

---

**Q10. How do you handle binary files in Python?**
**A:** Use `'rb'` or `'wb'` mode — commonly for images or audio files.

```python
with open("image.png", "rb") as file:
    data = file.read()
```

---

**Q11. How to read a CSV file in Python?**
**A:** Using built-in `csv` module or Pandas:

```python
import pandas as pd
data = pd.read_csv("data.csv")
```

---

**Q12. What’s the difference between `read()` and `readlines()`?**
**A:**

* `read()` → Returns entire file content as one string.
* `readlines()` → Returns list of lines.

---

**Q13. How can you delete a file using Python?**
**A:**

```python
import os
os.remove("data.txt")
```

---

**Q14. How do you rename a file?**
**A:**

```python
os.rename("old.txt", "new.txt")
```

---

**Q15. Why is file handling important for data scientists?**
**A:** Because most datasets are file-based (CSV, JSON, Excel). File handling allows you to load, process, and save data efficiently.

---

## ⚠️ **Error Handling (Q16–Q27)**

**Q16. What is error handling in Python?**
**A:** It’s the process of managing exceptions at runtime to prevent program crashes using `try-except` blocks.

---

**Q17. Difference between syntax errors and exceptions?**
**A:**

* **Syntax Error** → Mistake in code structure.
* **Exception** → Error occurs during program execution (e.g., division by zero).

---

**Q18. What is the purpose of `try-except` block?**
**A:** To execute risky code safely:

```python
try:
    print(10/0)
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

---

**Q19. How can you handle multiple exceptions?**
**A:**

```python
try:
    ...
except (ValueError, TypeError):
    ...
```

---

**Q20. What is the `finally` block used for?**
**A:** It executes code **whether an exception occurs or not** — commonly used for closing files or cleaning up resources.

---

**Q21. What is the `else` block in exception handling?**
**A:** Runs only when no exception occurs.

```python
try:
    x = 10/2
except:
    print("Error")
else:
    print("Success")
```

---

**Q22. What does `raise` do in Python?**
**A:** It manually triggers an exception.

```python
raise ValueError("Invalid Input")
```

---

**Q23. How to catch all exceptions?**
**A:**

```python
try:
    ...
except Exception as e:
    print(e)
```

---

**Q24. Why should you not use a bare `except`?**
**A:** It hides all errors (even critical ones) and makes debugging difficult.

---

**Q25. What is custom exception handling?**
**A:** Creating your own exception class.

```python
class InvalidAge(Exception): pass
```

---

**Q26. Why is error handling critical in data pipelines?**
**A:** To ensure failures (like missing files, null data) are logged and do not stop the entire ETL or ML pipeline.

---

**Q27. How can you log exceptions?**
**A:** Using `logging` module instead of just printing errors.

---

## 📦 **Modules (Q28–Q38)**

**Q28. What are modules in Python?**
**A:** Files containing reusable code (functions, variables, classes).

---

**Q29. Difference between module and package?**
**A:**

* **Module:** Single `.py` file.
* **Package:** Collection of modules with an `__init__.py` file.

---

**Q30. How do you import a module?**
**A:** `import math` or `from math import sqrt`.

---

**Q31. What is `__name__ == "__main__"` used for?**
**A:** To check if a file is run directly or imported as a module.

---

**Q32. How to list all functions inside a module?**
**A:**

```python
import math
dir(math)
```

---

**Q33. How do you install external Python modules?**
**A:** `pip install numpy`

---

**Q34. How do you create your own module?**
**A:** Save your code as `mymodule.py` and import it in another file using `import mymodule`.

---

**Q35. What is the difference between `import module` and `from module import *`?**
**A:**

* `import module` → Must use prefix (`module.function()`)
* `from module import *` → Imports everything directly (not recommended).

---

**Q36. What are some essential Python modules for Data Science?**
**A:** `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`.

---

**Q37. How do you reload a module without restarting Python?**
**A:**

```python
import importlib
importlib.reload(module_name)
```

---

**Q38. Why are modules important in large data projects?**
**A:** They organize reusable code into logical units, improving maintainability and teamwork.

---

## ⚡ **Comprehensions (Q39–Q50)**

**Q39. What are comprehensions in Python?**
**A:** Compact syntax for creating new sequences (lists, sets, dicts) from existing iterables.

---

**Q40. Syntax of list comprehension?**
**A:** `[expression for item in iterable if condition]`

---

**Q41. Example: create list of squares from 1–10.**
**A:** `[x**2 for x in range(1,11)]`

---

**Q42. What is dictionary comprehension?**
**A:** `{key: value for key, value in iterable}`

---

**Q43. Example: create dict of numbers and their cubes.**
**A:** `{x: x**3 for x in range(1,6)}`

---

**Q44. What is set comprehension?**
**A:** `{expression for item in iterable}` → creates a set of unique values.

---

**Q45. Can you use if-else in a comprehension?**
**A:** Yes.

```python
["Even" if x%2==0 else "Odd" for x in range(5)]
```

---

**Q46. What is a nested comprehension?**
**A:** A comprehension inside another.

```python
[[x*y for x in range(3)] for y in range(3)]
```

---

**Q47. Why are comprehensions faster than loops?**
**A:** They are optimized in C-level implementation and reduce overhead of repeated function calls.

---

**Q48. Can you use comprehension with functions?**
**A:** Yes.

```python
[len(word) for word in ["data","science"]]
```

---

**Q49. What are the benefits of comprehensions?**
**A:** Faster execution, cleaner syntax, and better readability for simple transformations.

---

**Q50. Why are comprehensions preferred in data preprocessing?**
**A:** They allow filtering, transformation, and cleaning of datasets in one line — crucial for quick data manipulation before modeling.

---