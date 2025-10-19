# 🧠 Python Collections & Functions in Data Science

---

### 1. **Functions**

**Why:**
Functions make your code modular, reusable, and cleaner.
In Data Science, you often create functions to clean data, perform feature engineering, or calculate metrics.

**How used:**

* Defining reusable steps for data cleaning
* Creating metric calculators like accuracy or precision
* Wrapping repetitive model code

**Example:**

```python
def mean(values):
    return sum(values) / len(values)
```

---

### 2. **Lists**

**Why:**
Lists store ordered, changeable data — perfect for dataset rows, feature values, or predictions.

**How used:**

* Storing feature vectors
* Holding dataset column names
* Storing model outputs

**Example:**

```python
features = [5.1, 3.5, 1.4, 0.2]
```

---

### 3. **Tuples**

**Why:**
Tuples are immutable and faster than lists — good for fixed data like coordinates or model hyperparameters.

**How used:**

* Storing fixed-size records (e.g., (x, y) points)
* Returning multiple values from functions

**Example:**

```python
shape = (100, 200)
```

---

### 4. **Dictionaries**

**Why:**
Dictionaries store data as key-value pairs, making them essential for labeled data and mapping relationships.

**How used:**

* Column-to-value mapping
* Configuration dictionaries for ML models
* JSON-style dataset handling

**Example:**

```python
student = {"name": "Akshit", "marks": 88, "subject": "Maths"}
```

---

### 5. **Sets**

**Why:**
Sets handle unique, unordered elements — useful for removing duplicates and checking membership efficiently.

**How used:**

* Finding unique categories
* Set operations between data groups

**Example:**

```python
categories = {"A", "B", "C", "A"}  # Output: {'A', 'B', 'C'}
```

---

## 💼 50 Professional Interview Questions with Answers

*(Functions, Lists, Tuples, Dictionaries, Sets)*

---

### 🔹 **Functions (1–10)**

**1. What is a function in Python?**
A block of reusable code that performs a specific task, defined using the `def` keyword.

**2. How to define a function?**

```python
def greet(name):
    print("Hello", name)
```

**3. What is a return statement?**
It sends back a value from the function to the caller.

**4. What are positional and keyword arguments?**
Positional arguments depend on order; keyword arguments specify names.

**5. What is a default argument?**
Predefined value assigned to a parameter if no argument is passed.

**6. What are variable-length arguments?**
`*args` (non-keyword) and `**kwargs` (keyword arguments) allow passing unlimited values.

**7. What is recursion?**
A function calling itself until a base condition is met.

**8. What are lambda functions?**
Anonymous one-line functions using `lambda` keyword.

```python
square = lambda x: x**2
```

**9. What’s the use of `map()`, `filter()`, and `reduce()`?**
They apply a function to a sequence:

* `map()` → applies function to all elements
* `filter()` → filters elements
* `reduce()` → accumulates result

**10. What is a docstring?**
A string literal used to document a function’s purpose.

---

### 🔹 **Lists (11–20)**

**11. What is a list in Python?**
An ordered, mutable collection of items enclosed in `[]`.

**12. How do you create a list?**

```python
lst = [1, 2, 3]
```

**13. How to access elements in a list?**
Using index numbers: `lst[0]`, `lst[-1]`.

**14. How to slice a list?**

```python
lst[1:4]  # elements from index 1 to 3
```

**15. How to add elements to a list?**
Using `append()` or `extend()`.

**16. How to remove elements?**
`remove()`, `pop()`, or `del`.

**17. What does `list.sort()` do?**
Sorts the list in place.

**18. How to find length of a list?**
`len(lst)`

**19. How to iterate through a list?**

```python
for item in lst:
    print(item)
```

**20. How to copy a list safely?**
Use `lst.copy()` or `list(lst)` (not `=` which creates reference).

---

### 🔹 **Tuples (21–30)**

**21. What is a tuple?**
An ordered, immutable collection enclosed in parentheses `()`.

**22. Why are tuples faster than lists?**
They’re stored in a fixed-size memory structure and can’t change.

**23. How to create a tuple?**

```python
tup = (1, 2, 3)
```

**24. How to create a single-element tuple?**
Add a comma: `tup = (1,)`

**25. How to unpack a tuple?**

```python
a, b = (10, 20)
```

**26. Can tuples contain different data types?**
Yes — `(1, "Akshit", 3.14)`

**27. Can tuples be nested?**
Yes — `((1,2), (3,4))`

**28. What’s the main difference between list and tuple?**
List is mutable, tuple is immutable.

**29. Can tuples be used as dictionary keys?**
Yes, because tuples are hashable.

**30. How to count elements in a tuple?**
`tup.count(value)`

---

### 🔹 **Dictionaries (31–40)**

**31. What is a dictionary?**
An unordered collection of key-value pairs enclosed in `{}`.

**32. How to create a dictionary?**

```python
d = {"a": 1, "b": 2}
```

**33. How to access dictionary values?**
`d["a"]` or `d.get("a")`

**34. How to add a key-value pair?**
`d["c"] = 3`

**35. How to remove a key-value pair?**
`d.pop("a")` or `del d["a"]`

**36. How to loop through a dictionary?**

```python
for key, value in d.items():
    print(key, value)
```

**37. How to check if a key exists?**
`if "a" in d:`

**38. What are dictionary methods you should know?**
`keys()`, `values()`, `items()`, `update()`, `pop()`, `clear()`

**39. How to merge two dictionaries?**
`dict3 = {**dict1, **dict2}` or `dict1.update(dict2)`

**40. What happens if you access a missing key using []?**
It raises a `KeyError`.

---

### 🔹 **Sets (41–50)**

**41. What is a set in Python?**
An unordered collection of unique elements.

**42. How to create a set?**

```python
s = {1, 2, 3}
```

**43. What happens when duplicates are added to a set?**
They are ignored automatically.

**44. How to add elements?**
`s.add(4)`

**45. How to remove elements?**
`s.remove(2)` or `s.discard(2)`

**46. What’s the difference between `remove()` and `discard()`?**
`remove()` raises error if element not found; `discard()` doesn’t.

**47. How to perform union and intersection?**
`s1 | s2` (union), `s1 & s2` (intersection)

**48. How to find difference between two sets?**
`s1 - s2`

**49. What is a frozen set?**
An immutable version of a set — created using `frozenset()`.

**50. How are sets useful in Data Science?**
To find unique values, remove duplicates, and compare categories efficiently.

---