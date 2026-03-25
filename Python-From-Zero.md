# Python — From Zero to Hero (Complete Beginner Guide)

## 🚀 Getting Started

### What is Python?
- A programming language (like English for computers)
- Easy to read and write
- Used for: web dev, AI, data science, automation

### Your First Program
```python
print("Hello, World!")
```
This prints text to the screen. That's it!

---

## 📦 Variables — Storing Data

### What is a Variable?
A named box that holds a value.
```python
name = "Rahul"        # String (text)
age = 22              # Integer (whole number)
height = 5.9          # Float (decimal)
is_student = True     # Boolean (True/False)
```

### Rules for Naming
- Can use letters, numbers, underscore
- Cannot start with a number
- ❌ `2name`, `my-name`
- ✅ `name2`, `my_name`, `myName`

### Print Variables
```python
print(name)           # Output: Rahul
print("Age:", age)    # Output: Age: 22
print(f"I am {age}")  # Output: I am 22 (f-string)
```

---

## 🔢 Numbers & Math

### Basic Operations
```python
a = 10
b = 3

print(a + b)    # Addition: 13
print(a - b)    # Subtraction: 7
print(a * b)    # Multiplication: 30
print(a / b)    # Division: 3.333...
print(a // b)   # Floor Division: 3 (removes decimal)
print(a % b)    # Modulus (remainder): 1
print(a ** b)   # Power: 1000 (10³)
```

### Useful Math Functions
```python
abs(-5)         # Absolute value: 5
round(3.7)      # Round: 4
max(1, 5, 3)    # Maximum: 5
min(1, 5, 3)    # Minimum: 1
```

---

## 📝 Strings — Working with Text

### Creating Strings
```python
name = "Rahul"
message = 'Hello World'
multi = """This is
a multi-line
string"""
```

### String Operations
```python
s = "Hello World"

len(s)              # Length: 11
s[0]                # First char: 'H'
s[-1]               # Last char: 'd'
s[0:5]              # Slice: 'Hello'
s[::-1]             # Reverse: 'dlroW olleH'
s.upper()           # Uppercase: 'HELLO WORLD'
s.lower()           # Lowercase: 'hello world'
s.split()           # Split: ['Hello', 'World']
s.replace("Hello", "Hi")  # 'Hi World'
"Hello" in s        # Check if exists: True
s.count("l")        # Count: 3
s.find("World")     # Find position: 6
```

### String Formatting
```python
name = "Rahul"
age = 22

# Method 1: f-string (BEST)
print(f"My name is {name}, I am {age}")

# Method 2: format()
print("My name is {}, I am {}".format(name, age))

# Method 3: % (old style)
print("My name is %s, I am %d" % (name, age))
```

---

## 📋 Lists — Collections of Items

### Creating Lists
```python
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", True, 3.14]
empty = []
```

### List Operations
```python
fruits = ["apple", "banana", "cherry"]

# Access
fruits[0]           # 'apple'
fruits[-1]          # 'cherry'
fruits[1:3]         # ['banana', 'cherry']

# Modify
fruits.append("mango")      # Add to end
fruits.insert(1, "orange")  # Insert at index 1
fruits.remove("banana")     # Remove by value
fruits.pop()                # Remove last
fruits.pop(0)               # Remove at index 0

# Useful
len(fruits)                 # Length
"apple" in fruits           # Check existence
fruits.sort()               # Sort (alphabetical)
fruits.reverse()            # Reverse
fruits.count("apple")       # Count occurrences
fruits.index("cherry")      # Find index

# Combine
list1 = [1, 2, 3]
list2 = [4, 5, 6]
combined = list1 + list2    # [1, 2, 3, 4, 5, 6]
```

### List Comprehension (Powerful!)
```python
# Create list of squares
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]

# Filter even numbers
evens = [x for x in range(10) if x % 2 == 0]  # [0, 2, 4, 6, 8]

# Double all numbers
doubled = [x * 2 for x in [1, 2, 3]]  # [2, 4, 6]
```

---

## 📖 Dictionaries — Key-Value Pairs

### Creating Dictionaries
```python
student = {
    "name": "Rahul",
    "age": 22,
    "grade": "A"
}
empty = {}
```

### Dictionary Operations
```python
student = {"name": "Rahul", "age": 22}

# Access
student["name"]              # 'Rahul'
student.get("name")          # 'Rahul' (safer)
student.get("phone", "N/A") # 'N/A' (default)

# Modify
student["age"] = 23          # Update
student["phone"] = "12345"   # Add new key
del student["phone"]         # Delete key

# Useful
len(student)                 # Number of keys
"name" in student            # Check key exists
student.keys()               # All keys
student.values()             # All values
student.items()              # All key-value pairs
student.update({"age": 24, "city": "Chennai"})
```

### Counting with Dictionary
```python
text = "programming"
freq = {}
for char in text:
    freq[char] = freq.get(char, 0) + 1
# freq = {'p': 1, 'r': 2, 'o': 1, 'g': 2, 'a': 1, 'm': 2, 'i': 1, 'n': 1}
```

---

## 🔀 Conditionals — Making Decisions

### if, elif, else
```python
age = 18

if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")
```

### Comparison Operators
```python
a == b    # Equal
a != b    # Not equal
a > b     # Greater than
a < b     # Less than
a >= b    # Greater or equal
a <= b    # Less or equal
```

### Logical Operators
```python
x and y   # Both must be True
x or y    # At least one True
not x     # Opposite of x

age = 20
has_id = True
if age >= 18 and has_id:
    print("Can enter")
```

### One-Line If
```python
x = 10
result = "even" if x % 2 == 0 else "odd"
```

---

## 🔄 Loops — Repeating Things

### For Loop
```python
# Loop through list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Loop through range
for i in range(5):        # 0, 1, 2, 3, 4
    print(i)

for i in range(1, 6):     # 1, 2, 3, 4, 5
    print(i)

for i in range(0, 10, 2): # 0, 2, 4, 6, 8
    print(i)

# Loop with index
for i, fruit in enumerate(fruits):
    print(f"{i}: {fruit}")
```

### While Loop
```python
count = 0
while count < 5:
    print(count)
    count += 1  # Don't forget to update!
```

### Loop Control
```python
for i in range(10):
    if i == 3:
        continue  # Skip 3
    if i == 7:
        break     # Stop at 7
    print(i)
# Output: 0, 1, 2, 4, 5, 6
```

---

## 📦 Functions — Reusable Code

### Creating Functions
```python
def greet(name):
    return f"Hello, {name}!"

message = greet("Rahul")
print(message)  # "Hello, Rahul!"
```

### Function with Default Parameters
```python
def greet(name="World"):
    return f"Hello, {name}!"

greet()           # "Hello, World!"
greet("Rahul")    # "Hello, Rahul!"
```

### Multiple Return Values
```python
def min_max(arr):
    return min(arr), max(arr)

lo, hi = min_max([3, 1, 4, 1, 5])
print(lo, hi)  # 1, 5
```

### Lambda Functions (One-Line)
```python
square = lambda x: x ** 2
print(square(5))  # 25

add = lambda a, b: a + b
print(add(3, 4))  # 7
```

---

## ⚠️ Error Handling

### Try-Except
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")

# Catch any error
try:
    x = int("hello")
except Exception as e:
    print(f"Error: {e}")
```

---

## 📥 Input/Output

### Reading Input
```python
# Simple input
name = input("Enter name: ")

# Integer input
age = int(input("Enter age: "))

# Multiple inputs
a, b = map(int, input("Enter two numbers: ").split())

# List of integers
arr = list(map(int, input().split()))

# Multiple lines
n = int(input())
for _ in range(n):
    x = int(input())
```

### Output Formatting
```python
x = 3.14159
print(f"{x:.2f}")      # 3.14 (2 decimal places)
print(f"{x:.0f}")      # 3 (no decimal)
print(f"{10:05d}")      # 00010 (pad with zeros)
print(f"{'hi':>10}")    # '        hi' (right align)
```

---

## 🔧 Built-in Functions Cheat Sheet

```python
# Type checking
type(x)              # Get type
isinstance(x, int)   # Check type

# Conversion
int("42")            # String to int
str(42)              # Int to string
float("3.14")        # String to float
list("hello")        # ['h', 'e', 'l', 'l', 'o']
tuple([1, 2, 3])     # (1, 2, 3)
set([1, 1, 2, 2])    # {1, 2}

# Iteration
range(5)             # 0, 1, 2, 3, 4
enumerate([a, b])    # (0, a), (1, b)
zip([1,2], [a,b])    # (1,a), (2,b)
reversed([1,2,3])    # 3, 2, 1

# Aggregation
sum([1, 2, 3])       # 6
max([1, 2, 3])       # 3
min([1, 2, 3])       # 1
len([1, 2, 3])       # 3
sorted([3,1,2])      # [1, 2, 3]

# Other
abs(-5)              # 5
round(3.7)           # 4
pow(2, 3)            # 8
```
