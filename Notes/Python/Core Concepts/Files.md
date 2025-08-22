
Python provides built-in support for reading and writing text files using the `open()` function. Always ensure proper closing of files or use `with` blocks.

---

## 📘 `open()` Syntax

```python
open(file, mode='r', encoding=None)
```

| Mode   | Description              |
| ------ | ------------------------ |
| `'r'`  | Read (default)           |
| `'w'`  | Write (truncates file)   |
| `'a'`  | Append                   |
| `'x'`  | Create (fails if exists) |
| `'r+'` | Read and write           |
| `'t'`  | Text mode (default)      |
| `'b'`  | Binary mode              |

---

## 📖 Reading Files

### 📌 Read Entire File

```python
with open('sample.txt', 'r') as file:
    data = file.read()
    print(data)
```

### 📌 Read Line-by-Line

```python
with open('sample.txt', 'r') as file:
    for line in file:
        print(line.strip())
```

### 📌 `readlines()` vs `readline()`

```python
lines = file.readlines()  # Returns list of lines
line1 = file.readline()   # Reads one line at a time
```

---

## ✍️ Writing Files

### 📌 Overwrite File with `'w'`

```python
with open('output.txt', 'w') as file:
    file.write("Hello, world!\n")
    file.write("Second line")
```

> ⚠️ Using `'w'` will **overwrite** the file if it exists.

### 📌 Append to File with `'a'`

```python
with open('log.txt', 'a') as file:
    file.write("New entry\n")
```

---

## 🧼 Ensuring Proper File Closure

### ✅ Best Practice: `with` Context Manager

```python
with open('file.txt', 'r') as f:
    content = f.read()
# File is automatically closed here
```

---

## 📜 Specifying Encoding

```python
with open('file.txt', 'r', encoding='utf-8') as f:
    content = f.read()
```

Use `utf-8` for cross-platform and non-ASCII safe I/O.

---

## 🧪 Example: Copy Text File

```python
with open('source.txt', 'r') as src, open('dest.txt', 'w') as dst:
    for line in src:
        dst.write(line)
```

---

## ❗ Common Errors

| Error                | Reason                                |
| -------------------- | ------------------------------------- |
| `FileNotFoundError`  | File doesn't exist in `'r'` mode      |
| `PermissionError`    | Writing to a protected file/directory |
| `UnicodeDecodeError` | Wrong encoding used while reading     |

---

## ✅ Summary

* Use `'r'` to read, `'w'` to overwrite, `'a'` to append
* Use `with open(...)` to avoid manual closing
* Always handle encoding for non-ASCII files

