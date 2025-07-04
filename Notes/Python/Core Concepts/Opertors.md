
*pydocs*: https://docs.python.org/3/library/operator.html


Python supports several types of operators:

1. **Arithmetic Operators**
2. **Comparison (Relational) Operators**
3. **Assignment Operators**
4. **Logical Operators**
5. **Bitwise Operators**
6. **Membership Operators**
7. **Identity Operators**
8. **Unary Operators (e.g., `-x`, `+x`, `not`)**

---

## 1. ➕ Arithmetic Operators

| Operator | Description         | Example  | Result |
| -------- | ------------------- | -------- | ------ |
| `+`      | Addition            | `3 + 2`  | `5`    |
| `-`      | Subtraction         | `3 - 2`  | `1`    |
| `*`      | Multiplication      | `3 * 2`  | `6`    |
| `/`      | Division (float)    | `3 / 2`  | `1.5`  |
| `//`     | Floor Division      | `3 // 2` | `1`    |
| `%`      | Modulus (remainder) | `3 % 2`  | `1`    |
| `**`     | Exponentiation      | `2 ** 3` | `8`    |

### Notes:

* `//` gives the largest integer less than or equal to the result.
* `/` always returns `float`.

---

## 2. 🧮 Comparison (Relational) Operators

| Operator | Description              | Example  | Result |
| -------- | ------------------------ | -------- | ------ |
| `==`     | Equal to                 | `3 == 3` | `True` |
| `!=`     | Not equal to             | `3 != 2` | `True` |
| `>`      | Greater than             | `3 > 2`  | `True` |
| `<`      | Less than                | `2 < 3`  | `True` |
| `>=`     | Greater than or equal to | `3 >= 3` | `True` |
| `<=`     | Less than or equal to    | `2 <= 3` | `True` |

---

## 3. 📝 Assignment Operators

| Operator | Description             | Example               | Equivalent To |       |         |     |
| -------- | ----------------------- | --------------------- | ------------- | ----- | ------- | --- |
| `=`      | Assign value            | `x = 5`               | -             |       |         |     |
| `+=`     | Add and assign          | `x += 3`              | `x = x + 3`   |       |         |     |
| `-=`     | Subtract and assign     | `x -= 3`              | `x = x - 3`   |       |         |     |
| `*=`     | Multiply and assign     | `x *= 3`              | `x = x * 3`   |       |         |     |
| `/=`     | Divide and assign       | `x /= 3`              | `x = x / 3`   |       |         |     |
| `//=`    | Floor divide and assign | `x //= 3`             | `x = x // 3`  |       |         |     |
| `%=`     | Modulus and assign      | `x %= 3`              | `x = x % 3`   |       |         |     |
| `**=`    | Exponentiate and assign | `x **= 2`             | `x = x ** 2`  |       |         |     |
| `&=`     | Bitwise AND and assign  | `x &= y`              | `x = x & y`   |       |         |     |
| \`       | =\`                     | Bitwise OR and assign | \`x           | = y\` | \`x = x | y\` |
| `^=`     | Bitwise XOR and assign  | `x ^= y`              | `x = x ^ y`   |       |         |     |
| `>>=`    | Right shift and assign  | `x >>= 1`             | `x = x >> 1`  |       |         |     |
| `<<=`    | Left shift and assign   | `x <<= 1`             | `x = x << 1`  |       |         |     |

---

## 4. 🧠 Logical Operators

Used for boolean logic (`True`/`False`).

| Operator | Description | Example          | Result  |
| -------- | ----------- | ---------------- | ------- |
| `and`    | Logical AND | `True and False` | `False` |
| `or`     | Logical OR  | `True or False`  | `True`  |
| `not`    | Logical NOT | `not True`       | `False` |

---

## 5. 🧮 Bitwise Operators

Operate on **binary (bit-level)** representations of integers.

| Operator | Description          | Example  | Result (binary)         |     |       |                 |
| -------- | -------------------- | -------- | ----------------------- | --- | ----- | --------------- |
| `&`      | AND                  | `5 & 3`  | `101 & 011` → `001` (1) |     |       |                 |
| \`       | \`                   | OR       | \`5                     | 3\` | \`101 | 011`→`111\` (7) |
| `^`      | XOR                  | `5 ^ 3`  | `101 ^ 011` → `110` (6) |     |       |                 |
| `~`      | NOT (1's complement) | `~5`     | `-6` (inverts bits)     |     |       |                 |
| `<<`     | Left shift           | `5 << 1` | `1010` (10)             |     |       |                 |
| `>>`     | Right shift          | `5 >> 1` | `10` (2)                |     |       |                 |

---

## 6. 🔎 Membership Operators

Used to test **presence of a value in a sequence**.

| Operator | Description        | Example            | Result |
| -------- | ------------------ | ------------------ | ------ |
| `in`     | Exists in sequence | `'a' in 'apple'`   | `True` |
| `not in` | Does not exist     | `4 not in [1,2,3]` | `True` |

---

## 7. 🧬 Identity Operators

Check if **two variables reference the same object** (not just same value).

| Operator | Description            | Example      | Result       |
| -------- | ---------------------- | ------------ | ------------ |
| `is`     | Same object (identity) | `a is b`     | `True/False` |
| `is not` | Not the same object    | `a is not b` | `True/False` |

```python
a = [1, 2]
b = [1, 2]
a == b     # True  (same value)
a is b     # False (different objects)
```

---

## 8. ➖ Unary Operators

Operate on a single operand.

| Operator | Description | Example    | Result  |
| -------- | ----------- | ---------- | ------- |
| `+`      | Unary plus  | `+5`       | `5`     |
| `-`      | Unary minus | `-5`       | `-5`    |
| `not`    | Logical NOT | `not True` | `False` |

---

## 🧪 Operator Precedence (Highest to Lowest)

| Level | Operators                                                        |    |
| ----- | ---------------------------------------------------------------- | -- |
| 1     | `()` (parentheses)                                               |    |
| 2     | `**` (exponentiation)                                            |    |
| 3     | `+x`, `-x`, `~x` (unary plus, minus, bitwise NOT)                |    |
| 4     | `*`, `/`, `//`, `%`                                              |    |
| 5     | `+`, `-`                                                         |    |
| 6     | `<<`, `>>`                                                       |    |
| 7     | `&`                                                              |    |
| 8     | `^`                                                              |    |
| 9     | \`                                                               | \` |
| 10    | `in`, `not in`, `is`, `is not`, `<`, `<=`, `>`, `>=`, `!=`, `==` |    |
| 11    | `not`                                                            |    |
| 12    | `and`                                                            |    |
| 13    | `or`                                                             |    |
| 14    | `=`, `+=`, `-=`, etc. (assignment operators, lowest precedence)  |    |
