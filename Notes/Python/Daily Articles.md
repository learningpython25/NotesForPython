
> [!abstract]
> **List of Articles**
> 1. https://realpython.com/instance-class-and-static-methods-demystified/
> 2. https://www.thepythoncodingstack.com/p/python-duck-typing-functions-classes-callables
> 3. https://wiingy.com/learn/python/encapsulation-in-python/
> 4. https://www.freecodecamp.org/news/whats-in-a-python-s-name-506262fe61e8/
> 5. https://www.scaler.com/topics/python/args-and-kwargs-in-python/
> 6. https://www.datacamp.com/tutorial/functional-programming-vs-object-oriented-programming
> 7. https://www.thepythoncodingstack.com/p/iterators-in-python-data-structure-6
> 8. https://wiingy.com/learn/python/first-class-functions-in-python/
> 9. https://hackernoon.com/understanding-the-underscore-of-python-309d1a029edc
> 10. https://www.freecodecamp.org/news/compiled-versus-interpreted-languages/
> 11. https://www.programiz.com/python-programming/exception-handling
> 12. https://thenewstack.io/packing-and-unpacking-in-python/

#### Packing and Unpacking
**On which side iterable object is available on unpacking?**
- Right Side `a, b = list(1,2)`

**Is packing and unpacking works on dictionaries?**
- Yes. By default keys are unpacked
- `a,b = {"a": 13, "b": 14}`
- `a,b = {"a": 13, "b": 14}.values`

#### Exception Handling
**How many except blocks are allowed in a try catch block?**
- Infinite

**When does the finally block get executed?**
- `finally` block gets executed independent of exception/success

#### Compiled Vs Interpreted
**Which is more efficient?**
- Compiled. Human readable code is turned into machine readable code.
**Examples of compiled and interpreted languages?**
- Compiled: C, C++, Java
- Interpreted: JavaScript, Python, Shell(sh, bash, ksh)
**Is python Interpreted or compiled?**
- Compatible with both


**What is functional programming?**
**What is Object Oriented Programming?**
**Q: Choose will work best for below: OOP or FP?**
1. You’re building a turn-based chess game where pieces move, capture, and interact. Each piece has rules and history of moves is tracked.
2. You’re writing a script to load a CSV, clean data, compute totals and averages, and generate a report — no long-term state or interactivity required.
3. You’re building a full-stack blogging platform with `User`, `Post`, `Comment`, and `Tag` entities, and need features like authentication, edit history, and relationships between objects.
**Q: A function that takes another function as an argument or returns one is called a __ function.**  
- Higher Order Function


