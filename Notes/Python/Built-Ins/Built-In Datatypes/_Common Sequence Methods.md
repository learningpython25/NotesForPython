
* `list`
* `tuple`
* `str`
* `range`
* `bytes`
* `bytearray`

### Common Sequence Operations

| **Operation**           | **Syntax / Description**             |
| ----------------------- | ------------------------------------ |
| `len(seq)`              | Returns the length                   |
| `min(seq)` / `max(seq)` | Returns the smallest/largest element |
| `sum(seq)`              | Sums elements (numeric types only)   |
| `sorted(seq)`           | Returns a sorted version             |
| `reversed(seq)`         | Returns a reverse iterator           |
| `enumerate(seq)`        | Returns index-value pairs            |
| `zip(seq1, seq2, ...)`  | Combines sequences element-wise      |
| `in` / `not in`         | Membership check                     |
| `+`                     | Concatenation                        |
| `*`                     | Repetition                           |
| `for x in seq`          | Iteration                            |


| **Method**  | **Description**                     |
| ----------- | ----------------------------------- |
| `.count(x)` | Count occurrences of `x`            |
| `.index(x)` | Return first index of `x`           |
| `.copy()`   | Return a shallow copy (only `list`) |
## Special Functions / Built-ins for Sequences

* **`any(seq)`** – True if any element is truthy
	* `any(list(map(lambda x: x % 2 == 0, [1,2,3, 4])))`
* **`all(seq)`** – True if all elements are truthy
	- `all(list(map(lambda x: x % 2 == 0, [1,2,3, 4])))`
* **`map(func, seq)`**
	* `list(map(lambda x: x+2, [1, 1]))`
* **`filter(func, seq)`**
	* `list(filter(lambda x: x % 2 == 0, [1,2,3, 4]))`
* **`range(start, stop, step)`**
	* 
* `list()`, `tuple()`, `str()` – type conversions


### Mutable Sequence Types

_t_ is any **iterable** object 
_x_ is an arbitrary object
_n_ is an integer

| Operation                 | Result                                                                                      |
| ------------------------- | ------------------------------------------------------------------------------------------- |
| `s[i] = x`                | item _i_ of _s_ is replaced by _x_                                                          |
| `s[i:j] = t`              | slice of _s_ from _i_ to _j_ is replaced by the contents of the iterable _t_                |
| `del s[i:j]`              | same as `s[i:j] = []`                                                                       |
| `s[i:j:k] = t`            | the elements of `s[i:j:k]` are replaced by those of _t_                                     |
| `del s[i:j:k]`            | removes the elements of `s[i:j:k]` from the list                                            |
| `s.append(x)`             | appends _x_ to the end of the sequence (same as `s[len(s):len(s)] = [x]`)                   |
| `s.clear()`               | removes all items from _s_ (same as `del s[:]`)                                             |
| `s.copy()`                | creates a shallow copy of _s_ (same as `s[:]`)                                              |
| `s.extend(t)` or `s += t` | extends _s_ with the contents of _t_ (for the most part the same as `s[len(s):len(s)] = t`) |
| `s *= n`                  | updates _s_ with its contents repeated _n_ times                                            |
| `s.insert(i, x)`          | inserts _x_ into _s_ at the index given by _i_ (same as `s[i:i] = [x]`)                     |
| `s.pop()` <br>`s.pop(i)`  | retrieves the item at _i_ and also removes it from _s_                                      |
| `s.remove(x)`             | removes the first item from _s_ where `s[i]` is equal to _x_                                |
| `s.reverse()`             | reverses the items of _s_ in place                                                          |