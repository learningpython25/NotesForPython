The `keyboard` module allows **real-time keyboard input capture**, including:

* Detecting when a key is pressed or released
* Handling hotkeys and key combos
* Reading individual characters or full events

> ⚠️ Requires **admin/root** privileges on some systems (especially Linux/Windows).

---

### 🧱 Installation

```bash
pip install keyboard
```

---

### ✅ Basic Usage

```python
import keyboard

keyboard.wait('q')  # Wait until 'q' is pressed
print("You pressed Q!")
```

---

### 🔍 Detecting Single Key Press

```python
key = keyboard.read_key()
print(f"You pressed: {key}")
```

---

### 🧪 Read Full Key Events

```python
event = keyboard.read_event()
print(event.name)        # Key name (e.g., 'a', 'space', 'enter')
print(event.event_type)  # 'down' or 'up'
```

---

### 📋 Example: Simple Key Logger (live input)

```python
import keyboard

print("Press any key (press ESC to stop):")

while True:
    event = keyboard.read_event()
    if event.event_type == keyboard.KEY_DOWN:
        print(f"Pressed: {event.name}")
        if event.name == 'esc':
            break
```

---

### 🎯 Hotkeys (Keyboard Shortcuts)

```python
keyboard.add_hotkey('ctrl+alt+h', lambda: print("Hello!"))
keyboard.wait('esc')
```

> ✅ Useful for productivity scripts and automation.

---

### ✨ Typing Automation

```python
keyboard.write("Hello, this is typed by Python!", delay=0.1)
```

---

### 🔒 Block Keys or Suppress Input

```python
keyboard.block_key('windows')  # Disable Windows key
```

---

### 🔁 Check Key Press in Loop (non-blocking)

```python
if keyboard.is_pressed('a'):
    print("You held 'a'!")
```

---

### 🧠 Summary

| Function               | Description                                |
| ---------------------- | ------------------------------------------ |
| `read_key()`           | Waits for a keypress and returns the key   |
| `read_event()`         | Waits for any key event (press/release)    |
| `is_pressed('x')`      | Returns `True` if key is currently pressed |
| `wait('esc')`          | Waits for a specific key to be pressed     |
| `add_hotkey('ctrl+x')` | Binds a function to a hotkey combo         |
| `write('text')`        | Simulates typing                           |
| `block_key('alt')`     | Disables a key system-wide                 |

---

### ⚠️ Permissions & Limitations

* Needs admin/root privileges to work system-wide
* May not work in **IDEs or notebooks** — run in terminal
* Not cross-platform safe for GUI-based apps — use with care
