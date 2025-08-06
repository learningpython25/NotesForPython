
```python
# First Declaration
def empty():
    pass


# Second
def empty():
    print("Function Second")
empty()
    
    
# Third
def greet(name):
    print(name)
    
greet("John")

#Fourth 
def add(a, b):
    return a + b
sum = add(10, 15)
print(sum)


### PRACTISE EXAMPLE

# - FUNCTION 1
def add(a,b):
    return a + b
result = add(1,1)
print(result)

# - FUNCTION 2
def sub(a,b):
    return a - b
result = sub(1,1)
print(result)

# - FUNCTION 3
def mul(a,b, c):
    return a * b *c
result = mul(1,1, 1)
print(result)

# - FUNCTION 4
def is_positive(a):
    if a > 0:
        return "positive"
    return "negative"
result = is_positive(1)
print(result)

# - FUNCTION 5
def leapyear(a):
    if a % 4 == 0:
        return "leap"
    return "not leap"
result = leapyear(100)
print(result)




```