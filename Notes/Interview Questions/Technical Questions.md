## Day 1

###### 1. What is `__name__` in Python? Where is it used?
* `__name__` is a special built-in variable in Python.
* It tells you whether a file is being **run directly** or **imported as a module**.
* Commonly used in:

  ```python
  if __name__ == "__main__":
      # This block runs only when the file is executed directly
  ```

---

###### 2. What are dunders in Python? Give some examples.
* **"Dunders"** = **"Double Underscores"**, e.g., `__name__`, `__init__`, `__str__`
* They are special (often built-in) **magic methods** or variables.
* Examples:
  * `__init__()` → Constructor for classes
  * `__str__()` → String representation of an object
  * `__len__()` → Returns length when `len(obj)` is called
  * `__name__` → Module name or `"__main__"`

---

##### Single Liners

###### 3. How do you get the path of the executing file in Python?

```python
import os; print(os.path.abspath(__file__))
```

---
###### 4. How do you get the information of an installed package?

```bash
pip show package_name
```


## Day 2
###### 5. What is version control (Git)?
- **Version control** is a system that tracks changes in files over time.
- **Git** is a **distributed version control system** that lets multiple developers collaborate, track file history, and manage changes efficiently.
- Key benefits:
    - Revert to previous versions
    - Branching and merging for feature development
    - Collaboration and backup
###### 6. Explain the Git Commands - status, log, init, add, push, clone, branch?
| Command               | Description                                                                          |
| --------------------- | ------------------------------------------------------------------------------------ |
| `git init`            | Initializes a new Git repository in the current folder                               |
| `git status`          | Shows the current state of the working directory (staged, modified, untracked files) |
| `git add <file>`      | Stages changes (adds to staging area)                                                |
| `git commit -m "msg"` | Commits the staged changes with a message                                            |
| `git push`            | Pushes commits to the remote repository (e.g., GitHub)                               |
| `git clone <url>`     | Downloads (clones) a remote repository to local                                      |
| `git branch`          | Lists all branches or creates a new one                                              |
| `git log`             | Shows commit history                                                                 |

###### 7. What is the difference between Git and GitHub?
|Git|GitHub|
|---|---|
|A **tool** used locally to manage version control|A **platform** to host Git repositories online|
|Works offline|Requires internet for pushing/pulling|
|CLI-based (command-line)|GUI + cloud-based interface|
|Maintains history and collaboration locally|Enables global collaboration & sharing|

###### 8. What are different ways to use `import` in python?
```python
import math                      # Imports the whole module
from math import sqrt            # Imports only the sqrt function
from math import *               # Imports everything (not recommended)
import math as m                 # Imports module with alias
```

###### 9. What is PIP? Explain PIP commands?
- **PIP** = _Pip Installs Packages_
- It's Python’s default package manager for installing libraries from **PyPI** (Python Package Index).

|Command|Description|
|---|---|
|`pip install <pkg>`|Install a package|
|`pip uninstall <pkg>`|Uninstall a package|
|`pip list`|List all installed packages|
|`pip show <pkg>`|Show details about a package|
|`pip freeze`|Show installed packages in `pkg==version` format|
|`pip install -r requirements.txt`|Install packages from a file|