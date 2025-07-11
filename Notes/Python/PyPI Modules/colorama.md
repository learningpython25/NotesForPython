`colorama` is a Python module used to **print colored text** in the terminal (cross-platform, including Windows).

It supports:

* **Foreground text colors**
* **Style formatting (bold, dim, reset, etc.)**

---

### 🧱 Installation

```bash
pip install colorama
```

---

### 🧪 Basic Setup

```python
from colorama import Fore, Style, init
init(autoreset=True)  # Automatically reset color after each print
```

> Without `autoreset=True`, you'd have to use `Style.RESET_ALL` manually after each color segment.

---

### 🎨 Foreground Colors

```python
print(Fore.RED + "This is red")
print(Fore.GREEN + "This is green")
print(Fore.YELLOW + "This is yellow")
print(Fore.CYAN + "This is cyan")
print(Fore.WHITE + "Back to white")
```

---

### ✨ Style Options

```python
print(Style.BRIGHT + Fore.BLUE + "Bright blue text")
print(Style.DIM + "Dimmed text")
print(Style.NORMAL + "Normal style")
print(Style.RESET_ALL + "Reset all styles and colors")
```

---

### 🎯 Full Example

```python
from colorama import Fore, Style, init

init(autoreset=True)

print(Fore.RED + "Error: Something went wrong!")
print(Fore.GREEN + "Success: Everything is fine.")
print(Style.BRIGHT + Fore.YELLOW + "Warning: Be careful!")
print("This is normal text.")
```

---

### 🧠 Good to Know

| Element      | Usage Example                          |
| ------------ | -------------------------------------- |
| `Fore.COLOR` | `Fore.RED`, `Fore.GREEN`, etc.         |
| `Style`      | `Style.BRIGHT`, `Style.RESET_ALL`      |
| `init()`     | Enables color support on all platforms |

---

### ⚠️ Windows Support

On Windows, `colorama.init()` wraps the console to enable ANSI escape codes (used for colors). It’s a must for colored output to work consistently.
