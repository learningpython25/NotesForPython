
Below are the types of imports:
- `import math, sys`
- `from math import pi, sin`
- `from math import *`

**with alias**
- `import math as m`
- `from math import pi as p, sin as s`


**module vs package**
- module is a kind of container filled with functions
- pakcage is folder/dirctory of such modules


`__pycache__`
- it gets created when a module is imported for the first time
- When Python imports a module for the first time, it **translates its contents into a somewhat compiled shape**.
- it's internal Python **semi-compiled code**

`__name__`
- **in-built variable** available in the module scope of python namespace
- Moreover, each source file uses its own, separate version of the variable - it isn't shared between modules.
- When you run a file directly, its `__name__` variable is set to `__main__`;

`#!`
- The line starting with `#!` has many names - it may be called _shabang_, _shebang_, _hashbang_, _poundbang_ or even _hashpling_ 
- For Unix and Unix-like OSs (including MacOS) such a line **instructs the OS how to execute the contents of the file** 

`__init__.py`
- any folder containig the init.py will be treated as a package '
- This file will be executed when the folder containing this file is imported independent of its children being copied or not

`__doc__`
gives the doc string of a a function or class or module