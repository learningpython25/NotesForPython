**1. Can you explain about the Python programming language?**

* Python is a *high-level, interpreted* programming language known for its *simplicity and readability*.
* It supports *multiple paradigms*: object-oriented, procedural, and functional programming.
* Comes with a *large standard library* and strong community support, making it versatile.
* Widely used in *web development, data science, automation, AI/ML, and scripting*.
* Python’s *dynamic typing* and *automatic memory management* make it beginner-friendly.
* Popular frameworks/libraries: *Django, Flask, Pandas, NumPy, TensorFlow*.

**2. Can you explain about Git?**

* Git is a *distributed version control system* used to track changes in source code.
* It enables *collaboration* by allowing multiple developers to work on the same project.
* Key operations: *commit (save changes), branch (create isolated environments), merge (combine code), clone (copy repo), and push/pull (sync with remote repo)*.
* Every developer has a *full copy of the repository*, which makes it resilient and fast.
* Supports workflows like *feature branching, pull requests, and code reviews*.
* Platforms like *GitHub, GitLab, and Bitbucket* host Git repositories with collaboration tools.

**3. Can you explain about PIP?**

* *PIP* stands for *Pip Installs Packages* (or *Pip Installs Python*).
* It is the *official package manager* for Python.
* Allows developers to install, upgrade, and remove external *libraries and dependencies*.
* Packages are downloaded from the *Python Package Index (PyPI)*.
* Common commands:

  * `pip install package_name`
  * `pip list`
  * `pip freeze > requirements.txt`
* Helps manage project dependencies effectively.


**4. Can you explain the major data types in Python?**

* *Numeric* → `int`, `float`, `complex` (used for numbers and calculations).
* *Sequence* → `list`, `tuple`, `range` (ordered collections).
* *Text* → `str` (used for handling text/strings).
* *Set Types* → `set`, `frozenset` (unordered collections of unique elements).
* *Mapping* → `dict` (key-value pairs).
* *Boolean* → `bool` (`True`/`False`).
* Python also supports *NoneType* (`None`) to represent null values.


**5. Can you explain any three modules in Python? (`re`, `os`, `sys`)***

* *`re` (Regular Expressions):*
  * Provides support for *pattern matching and text searching*.
  * Example: `re.findall("\d+", "abc123xyz")` → `['123']`.

* *`os` (Operating System):*
  * Interacts with the *operating system* (file handling, environment variables, paths).
  * Example: `os.listdir()` → lists files in a directory.

* *`sys` (System-specific parameters):*
  * Gives access to *Python interpreter variables* and functions.
  * Example: `sys.argv` → list of command-line arguments passed to a script.

---

# SET 2
**6. What are virtual environments in Python and why do we use them?**

* A *virtual environment* isolates Python dependencies for a project.
* Prevents *conflicts* between package versions across projects.
* Tools: `venv` (built-in) and `virtualenv`.
* Example: `python -m venv env && source env/bin/activate`.
* Keeps the global Python installation *clean*.
* Essential for deployment and team-based projects.

**7. Can you explain exception handling in Python?**

* Handled using *try-except-finally* blocks.
* Prevents program crashes when errors occur.
* Example:

  ```python
  try:
      x = 1 / 0
  except ZeroDivisionError:
      print("Cannot divide by zero")
  finally:
      print("Execution finished")
  ```
* `finally` executes whether an exception occurred or not.
* We can also use `raise` to throw custom exceptions.
* Best practice: catch *specific exceptions*.

**8. What is the difference between list, tuple, and set?**

* *List* → Ordered, mutable, allows duplicates (`[1,2,3]`).
* *Tuple* → Ordered, immutable, allows duplicates (`(1,2,3)`).
* *Set* → Unordered, mutable, no duplicates (`{1,2,3}`).
* Lists are best for *general collections*.
* Tuples are best for *fixed data* (like coordinates).
* Sets are best for *fast membership tests*.

**9. What are Pandas and how is it useful in data analysis?**

* *Pandas* is a Python library for *data manipulation and analysis*.
* Provides *DataFrame* and *Series* structures for tabular data.
* Handles CSV, Excel, SQL, JSON imports/exports easily.
* Common operations: filtering, grouping, merging, pivoting.
* Example:

  ```python
  import pandas as pd
  df = pd.read_csv("data.csv")
  print(df.head())
  ```
* Widely used in *ETL pipelines, reporting, and data cleaning*.



# SET 3

**10. What are Python’s key features?**

* Interpreted: code runs line by line, no compilation needed.
* High-level: developer-friendly with easy syntax.
* Dynamically typed: no need to declare variable types.
* Object-oriented + functional programming support.
* Large standard library (e.g., `os`, `sys`, `re`).
* Cross-platform and widely used in web, AI, data analysis.

**11. What are Python’s built-in data structures?**

* *List* → ordered, mutable collection.
* *Tuple* → ordered, immutable collection.
* *Set* → unordered, unique elements.
* *Dictionary* → key-value pairs.
* Together, they form the foundation for most Python programs.

**12. What are Python functions and why use them?**

* Functions are reusable blocks of code defined with `def`.
* Promote *code reuse* and *modularity*.
* Can take parameters and return values.
* Example:

  ```python
  def add(a, b): return a+b
  ```
* Supports default arguments, keyword arguments, and variable arguments (`*args`, `*kwargs`).
* Helps write *clean, maintainable* programs.

**13. What are Python classes and objects?**

* *Class*: blueprint for creating objects.
* *Object*: instance of a class, with attributes & methods.
* Python supports OOP concepts: inheritance, encapsulation, polymorphism.
* Example:

  ```python
  class Car:
      def __init__(self, brand):
          self.brand = brand
  ```
* Classes improve *organization* in large projects.
* Widely used in backend frameworks (Flask, Django).

**14. What are Python’s conditional statements and loops?**

* Conditionals: `if`, `elif`, `else` for decision-making.
* Loops:

  * `for` → iterate over sequences.
  * `while` → repeat until condition is false.
* Support `break`, `continue`, `pass`.
* Example:

  ```python
  for i in range(5): print(i)
  ```
* Core control flow building blocks.

**15. What are Python’s operators?**

* *Arithmetic*: `+ - * / // % *`.
* *Comparison*: `== != > < >= <=`.
* *Logical*: `and, or, not`.
* *Assignment*: `= += -=`.
* *Identity*: `is, is not`.
* *Membership*: `in, not in`.
* Used everywhere from conditions to calculations.

**16. What is Python’s `with` statement and context managers?**

* Used to manage *resources* like files, DB connections.
* Ensures proper cleanup (close files, release locks).
* Example:

  ```python
  with open("file.txt") as f:
      data = f.read()
  ```
* Equivalent to `try-finally` but cleaner.
* Custom context managers possible with `__enter__` & `__exit__`.
* Improves *robustness* and avoids leaks.

**17. What are Python’s built-in functions you use often?**

* `len()` → length of object.
* `type()` → data type.
* `print()` → display output.
* `range()` → generate sequences.
* `enumerate()` → iterate with index.
* `zip()` → combine iterables.
* These are basics every dev uses daily.

**18. What are Python modules and packages?**

* *Module*: a `.py` file containing functions/classes (e.g., `math.py`).
* *Package*: collection of modules with an `__init__.py`.
* Helps organize large projects into reusable components.
* Import styles: `import os`, `from math import sqrt`.
* Python has both *standard library* and *third-party packages (via pip)*.
* Encourages modular, reusable code.

**19. What are Python’s mutable vs immutable types?**

* *Mutable* → can change in place (list, dict, set).
* *Immutable* → cannot change in place (int, float, str, tuple).
* Example:

  ```python
  s = "hi"; s[0] = "H"  # ❌ error
  ```
* Important for memory efficiency & performance.
* Helps avoid bugs in function arguments.
* Also affects hashability (e.g., dict keys must be immutable).
