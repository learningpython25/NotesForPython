
*pydocs:* https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex

1. **`int`** – Integer values
2. **`float`** – Floating-point (decimal) numbers
3. **`complex`** – Complex numbers with real and imaginary parts

---

### 1. `int` (Integer)

* Whole numbers without a decimal point.
* Can be **positive**, **negative**, or **zero**.
* **Arbitrary precision** (no overflow like in C/C++).


```python
a = 10
b = -50
c = 0
d = 12345678901234567890  # Python handles big integers
```

```python
5 + 3       # 8
10 - 4      # 6
7 * 6       # 42
8 // 3      # 2 (integer division)
8 % 3       # 2 (modulo) -> remainder
2 ** 4      # 8 (power) 2*2*2*2
```

---

### 2. `float` (Floating Point)

* Numbers with decimal points.
* Follows IEEE 754 double-precision by default (64-bit).
* Includes **scientific notation** (`1.5e3` → 1500.0).


```python
a = 3.14
b = -0.001
c = 2.0
d = 1.5e3     # 1500.0
```


```python
10.5 + 4.3    # 14.8
3.5 * 2       # 7.0
7 / 2         # 3.5 (float division)
```

* Floating-point arithmetic may introduce **precision errors**:

```python
0.1 + 0.2  # 0.30000000000000004
```

---

### 3. `complex` (Complex Numbers)

* Numbers with **real** and **imaginary** parts.
* Syntax: `a + bj` (note: `j` is used for the imaginary unit in Python).
* Native support for complex arithmetic.


```python
a = 2 + 3j
b = -1.5 + 0.5j
```


```python
z = 4 + 5j
z.real      # 4.0
z.imag      # 5.0
abs(z)      # √(4² + 5²) = 6.4031...
```


```python
(2 + 3j) + (1 - 1j)    # (3 + 2j)
(2 + 3j) * (1 + 1j)    # (-1 + 5j)
```


## Type Conversions

```python
int(5.7)         # 5
float(10)        # 10.0
complex(2)       # (2+0j)
complex(2, 3)    # (2+3j)
```

## Type Checking

```python
type(10)         # <class 'int'>
type(3.14)       # <class 'float'>
type(2 + 3j)     # <class 'complex'>
```

## Summary 

| Feature        | `int`       | `float`            | `complex`              |
| -------------- | ----------- | ------------------ | ---------------------- |
| Precision      | Exact       | Approximate (IEEE) | Exact real & imaginary |
| Decimal        | ❌ No        | ✅ Yes              | ✅ Yes (imaginary)      |
| Imaginary Part | ❌ No        | ❌ No               | ✅ Yes                  |
| Mutable        | ❌ Immutable | ❌ Immutable        | ❌ Immutable            |
| Size limit     | Unlimited   | \~15-17 digits     | Unlimited (complex)    |
| Literal Syntax | `10`        | `10.5`, `1e3`      | `2 + 3j`               |

