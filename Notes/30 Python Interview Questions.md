
#### Descriptive Questions
- **1. What are mutable and immutable types?**
	- **Mutable:** can be changed in-place (e.g., `list`, `dict`, `set`)
	- **Immutable:** cannot be changed after creation (e.g., `int`, `float`, `str`, `tuple`)




#### Technical Questions
- **2. What is the difference between `is` and `==` in Python?**
	- `==` checks **value equality** (do the variables hold the same value?)
	- `is` checks **object identity** (do they refer to the same object in memory?)
	
		```python
			a = [1, 2] 
			b = a 
			c = [1, 2]  
			print(a == c)  # True 
			print(a is c)  # False print(a is b)  # True
		```


- **3. How are Python arguments passed—by value or reference?**
	- Python uses **call-by-object-reference**:
	- Mutable objects can be modified inside a function.
	- Immutable objects cannot be changed (only reassigned).
		```python
			def modify(lst):
			    lst.append(4)
			
			a = [1, 2, 3]
			modify(a)
			print(a)  # [1, 2, 3, 4]
		```
  

---

- **4. What are Python decorators?**
	- Decorators are functions that modify the behavior of other functions or methods. They’re often used for logging, access control, timing, etc.
		```python
		def logger(func):
		    def wrapper():
		        print("Calling function...")
		        return func()
		    return wrapper
		
		@logger
		def say_hi():
		    print("Hi!")
		
		say_hi()
		```

#### Programmatic Questions