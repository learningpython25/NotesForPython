### What are top level value?

In Python, when you make a **shallow copy** of a container (like a list, dict, set), it **copies the container**, but **not the elements inside** if those elements are themselves mutable.

So **top-level values** refer to the **immediate elements inside** the container — not what those elements themselves point to.

---

### Example: Shallow vs Deep Copy

```python
import copy

original = [[1, 2], [ 3, 4], 5]

assigment = original # same storage; additional lable
shallow = original.copy() # different storage, new label -> only high level
deep = copy.deepcopy(original) # defferent stroage new label -> all levels -> deep level copy


print("ID of original", id(original)) # 123
print("ID of assigment", id(assigment)) # xxxx
print("ID of shallow", id(shallow)) # yyyy
print("ID of deep", id(deep)) # ZZZZ

original[0][0] = 999
original[2] = 888

print("original is: ", original) # 999, 2, 3, 4
print("assigment is: ", assigment) # 999, 2, 3, 4
print("shallow is: ", shallow) # 1, 2, 3, 4
print("deep is: ", deep) # 1, 2, 3, 4
```

#### What happened?

* `original.copy()` made a **shallow copy**:

  * It copied the **outer list**, but not the inner lists.
  * So `shallow[0]` and `original[0]` point to the **same inner list**.
* `copy.deepcopy()` copied **everything**, including the nested inner lists.

---

### Visualization

```
original   ──▶ [ ListA ──▶ [1, 2], ListB ──▶ [3, 4] ]
shallow    ──▶ [  ↑              ↑
                  └──────────────┘ (same inner lists)
deep       ──▶ [ NewListA ──▶ [1, 2], NewListB ──▶ [3, 4] ]
```

---

### Summary

| Copy Type    | Top-Level Container | Inner Elements                 |
| ------------ | ------------------- | ------------------------------ |
| `copy()`     | New object          | Same references (shared)       |
| `deepcopy()` | New object          | New copies (fully independent) |

