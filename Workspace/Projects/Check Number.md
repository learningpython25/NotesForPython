
```python
import math

def is_palindrome(n):
    """Check if the number is a palindrome."""
    return str(n) == str(n)[::-1]

def is_prime(n):
    """Check if the number is prime."""
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(math.sqrt(n)) + 1, 2):
        if n % i == 0:
            return False
    return True

def is_fibonacci(n):
    """Check if the number is a Fibonacci number using 5n^2 ± 4 trick."""
    def is_perfect_square(x):
        s = int(math.sqrt(x))
        return s * s == x

    return is_perfect_square(5 * n * n + 4) or is_perfect_square(5 * n * n - 4)

def is_factorial(n):
    """Check if the number is a factorial number."""
    i = 1
    fact = 1
    while fact < n:
        i += 1
        fact *= i
    return fact == n

```