##### 1. How do you get the current working directory in Python?

**Answer:**

```python
import os
print(os.getcwd())
```

##### 2. How do you list all files and folders in a directory?

**Answer:**

```python
import os
print(os.listdir("path/to/folder"))
```

##### 3. How do you join a folder path and filename correctly in Python?

**Answer:**

```python
import os
full_path = os.path.join("folder", "file.txt")
print(full_path)
```

##### 4. How do you check if a file exists?

**Answer:**

```python
import os
print(os.path.exists("file.txt"))
```

##### 5. How do you check if a path is a file or folder?

**Answer:**

```python
import os
print(os.path.isfile("path"))
print(os.path.isdir("path"))
```


---

## re

Online Quiz: https://runestone.academy/ns/books/published/py4e-int/regex/hp-practice.html

```py
import re

import re

# 1. Find all the letter "a"
text1 = "apple banana cat"
result1 = re.findall(r"a", text1)
print("1:", result1)
# ['a', 'a', 'a', 'a', 'a', 'a']


# 2. Find all digits
text2 = "Room 1 is upstairs, room 2 is downstairs."
result2 = re.findall(r"[0-9]", text2)
print("2:", result2)
# ['1', '2']


# 3. Find all words "cat"
text3 = "The cat chased another cat."
result3 = re.findall(r"cat", text3)
print("3:", result3)
# ['cat', 'cat']


# 4. Find all capital letters
text4 = "My Name Is Sam."
result4 = re.findall(r"[A-Z]", text4)
print("4:", result4)
# ['M', 'N', 'I', 'S']


# 5. Find all 2-digit numbers
text5 = "He is 15 years old and she is 20."
result5 = re.findall(r"\b\d{2}\b", text5)
print("5:", result5)
# ['15', '20']


```