


| **Type** | **Mutable** | **Ordered** | **Indexable** | **Duplicates** | **Init**        |
| -------- | ----------- | ----------- | ------------- | -------------- | --------------- |
| *list*   | ✅ mutable   | ✅ ordered   | ✅ indexable   | ✅ yes          | `l = [1]`       |
| *set*    | ✅ mutable   | ❌ unordered | ❌ unindexable | ❌ no           | `s={a}`         |
| *tuple*  | ❌ immutable | ✅ ordered   | ✅ indexable   | ✅ yes          | `t=(1,)`        |
| *dict*   | ✅ mutable   | ✅ ordered   | ✅ indexable   | ❌ no           | `d={1:2}`       |
| *str*    | ❌ immutable | ✅ ordered   | ✅ indexable   | ✅ yes          | `str=''`        |
| *range*  | ❌ immutable | ✅ ordered   | ✅ indexable   | ✅ yes          | `range(1,10,2)` |

### All List Based Methods

| Method      | `list` | `tuple` | `range` | `set` | `dict` |
| ----------- | ------ | ------- | ------- | ----- | ------ |
| `append()`  | ✅      | ❌       | ❌       | ❌     | ❌      |
| `extend()`  | ✅      | ❌       | ❌       | ❌     | ❌      |
| `insert()`  | ✅      | ❌       | ❌       | ❌     | ❌      |
| `remove(x)` | ✅      | ❌       | ❌       | ✅     | ❌      |
| `pop()`     | ✅      | ❌       | ❌       | ✅     | ✅      |
| `clear()`   | ✅      | ❌       | ❌       | ✅     | ✅      |
| `reverse()` | ✅      | ❌       | ❌       | ❌     | ❌      |
| `sort()`    | ✅      | ❌       | ❌       | ❌     | ❌      |
| `copy()`    | ✅      | ❌       | ❌       | ✅     | ✅      |
| `index(x)`  | ✅      | ✅       | ❌       | ❌     | ❌      |
| `count(x)`  | ✅      | ✅       | ❌       | ❌     | ❌      |

### Set Only Methods
| Method                   | `set` |
| ------------------------ | ----- |
| `add(x)`                 | ✅     |
| `discard(x)`             | ✅     |
| `union()`                | ✅     |
| `intersection()`         | ✅     |
| `difference()`           | ✅     |
| `symmetric_difference()` | ✅     |
| `issubset()`             | ✅     |
| `issuperset()`           | ✅     |
| `isdisjoint()`           | ✅     |

### Dict Only Methods

|Method|`dict`|
|---|---|
|`get(key)`|✅|
|`keys()`|✅|
|`values()`|✅|
|`items()`|✅|
|`update()`|✅|
|`setdefault()`|✅|
|`pop(key)`|✅|
|`popitem()`|✅|
|`fromkeys()`|✅|