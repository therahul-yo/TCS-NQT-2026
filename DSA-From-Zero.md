# DSA (Data Structures & Algorithms) — From Zero

## 🤔 What is DSA?

- **Data Structure**: Ways to organize and store data
- **Algorithm**: Step-by-step instructions to solve a problem
- Think of it like: Data Structure = filing cabinet, Algorithm = finding a file

---

## 📊 Data Structures — What You Need to Know

### 1. Array (List in Python)
**What**: Ordered collection of items

```python
arr = [1, 2, 3, 4, 5]
```

**Operations & Time Complexity:**
| Operation | How | Time |
|-----------|-----|------|
| Access by index | `arr[0]` | O(1) ✅ |
| Search element | `x in arr` | O(n) |
| Add to end | `arr.append(x)` | O(1) ✅ |
| Remove from end | `arr.pop()` | O(1) ✅ |
| Insert at position | `arr.insert(i, x)` | O(n) |
| Delete at position | `arr.pop(i)` | O(n) |
| Sort | `arr.sort()` | O(n log n) |

**When to use**: When you need ordered data and fast access by position.

---

### 2. String
**What**: Sequence of characters (immutable array of chars)

```python
s = "hello"
```

**Operations:**
| Operation | How | Time |
|-----------|-----|------|
| Access by index | `s[0]` | O(1) |
| Length | `len(s)` | O(1) |
| Concatenation | `s1 + s2` | O(n) |
| Slice | `s[1:3]` | O(k) |
| Find substring | `s.find("ll")` | O(n) |
| Split | `s.split()` | O(n) |

**Note**: Strings are IMMUTABLE in Python — you can't change `s[0] = 'H'`

---

### 3. Dictionary (HashMap)
**What**: Key-value pairs (like a real dictionary: word → definition)

```python
d = {"name": "Rahul", "age": 22}
```

**Operations & Time Complexity:**
| Operation | How | Time |
|-----------|-----|------|
| Access by key | `d["name"]` | O(1) ✅ |
| Add/Update | `d["key"] = val` | O(1) ✅ |
| Delete | `del d["key"]` | O(1) ✅ |
| Check key exists | `"name" in d` | O(1) ✅ |
| Get all keys | `d.keys()` | O(n) |

**When to use**: When you need fast lookups (counting, grouping, mapping).

**Why O(1)?**: Uses hashing — jumps directly to the location, doesn't search.

---

### 4. Set
**What**: Collection of UNIQUE items (no duplicates)

```python
s = {1, 2, 3, 3, 4}  # {1, 2, 3, 4}
```

**Operations:**
| Operation | How | Time |
|-----------|-----|------|
| Add | `s.add(x)` | O(1) |
| Remove | `s.remove(x)` | O(1) |
| Check exists | `x in s` | O(1) ✅ |
| Union | `s1 | s2` | O(n) |
| Intersection | `s1 & s2` | O(n) |

**When to use**: Removing duplicates, fast membership checking.

---

### 5. Stack (LIFO — Last In, First Out)
**What**: Like a stack of plates — add/remove from top only

```python
stack = []
stack.append(1)     # Push (add to top)
stack.append(2)
top = stack.pop()   # Pop (remove from top) → 2
top = stack[-1]     # Peek (look at top) → 1
```

**Real-life**: Undo button, browser back button, function call stack

**When to use**: Parentheses matching, reverse order, backtracking.

---

### 6. Queue (FIFO — First In, First Out)
**What**: Like a line at a store — first person served first

```python
from collections import deque
queue = deque()
queue.append(1)      # Enqueue (add to back)
queue.append(2)
front = queue.popleft()  # Dequeue (remove from front) → 1
front = queue[0]         # Peek (look at front) → 2
```

**Real-life**: Print queue, task scheduling, BFS traversal

**When to use**: Processing items in order, breadth-first search.

---

## 🧠 Algorithms — What You Need to Know

### 1. Linear Search (Brute Force)
**What**: Check every element one by one

```python
def linear_search(arr, target):
    for i, num in enumerate(arr):
        if num == target:
            return i
    return -1
```

**Time**: O(n) — worst case checks all elements
**When to use**: Unsorted array, small data

---

### 2. Binary Search
**What**: Divide sorted array in half repeatedly

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
```

**Time**: O(log n) — much faster than linear!
**Requirement**: Array MUST be sorted
**Example**: Finding a word in a dictionary

---

### 3. Sorting

#### Built-in Sort (Use This!)
```python
arr = [3, 1, 4, 1, 5]
arr.sort()              # In-place: [1, 1, 3, 4, 5]
sorted_arr = sorted(arr) # Returns new list
```

#### Bubble Sort (Understand concept)
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr
```

**Time**: O(n²) — slow, but easy to understand

#### Understanding Sorting
| Algorithm | Best | Average | Worst | Space |
|-----------|------|---------|-------|-------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) |
| Python sort() | O(n) | O(n log n) | O(n log n) | O(n) |

**For TCS**: Just use `arr.sort()` — it uses TimSort (O(n log n))

---

### 4. Recursion
**What**: A function that calls itself

```python
# Factorial: 5! = 5 × 4 × 3 × 2 × 1 = 120
def factorial(n):
    if n <= 1:      # Base case (STOP)
        return 1
    return n * factorial(n - 1)  # Recursive call

print(factorial(5))  # 120
```

**Key**: ALWAYS need a base case (when to stop), or it runs forever!

**How it works:**
```
factorial(5)
  → 5 × factorial(4)
    → 4 × factorial(3)
      → 3 × factorial(2)
        → 2 × factorial(1)
          → 1 (base case)
        → 2 × 1 = 2
      → 3 × 2 = 6
    → 4 × 6 = 24
  → 5 × 24 = 120
```

**When to use**: Trees, divide-and-conquer, mathematical patterns

---

### 5. Two Pointers
**What**: Use two pointers moving toward each other or same direction

```python
# Check if array has pair that sums to target
def two_sum_sorted(arr, target):
    left, right = 0, len(arr) - 1
    while left < right:
        current_sum = arr[left] + arr[right]
        if current_sum == target:
            return True
        elif current_sum < target:
            left += 1
        else:
            right -= 1
    return False
```

**Time**: O(n) — much better than nested loops O(n²)
**When to use**: Sorted arrays, palindromes, pair problems

---

### 6. Sliding Window
**What**: Move a "window" over data to find patterns

```python
# Find max sum of k consecutive elements
def max_sum_subarray(arr, k):
    window_sum = sum(arr[:k])
    max_sum = window_sum
    for i in range(k, len(arr)):
        window_sum += arr[i] - arr[i-k]  # Slide window
        max_sum = max(max_sum, window_sum)
    return max_sum
```

**Time**: O(n) — instead of O(n×k) with nested loops
**When to use**: Subarray/substring problems

---

### 7. Hashing (Using Dictionary)
**What**: Use dictionary for O(1) lookups

```python
# Find if array has duplicates
def has_duplicates(arr):
    seen = set()
    for num in arr:
        if num in seen:
            return True
        seen.add(num)
    return False
```

**Time**: O(n) — each lookup is O(1)
**When to use**: Counting, finding duplicates, grouping

---

## 📏 Time Complexity — How Fast is Your Code?

### What is Big O?
Measures how code performance scales with input size.

| Big O | Name | Example | Speed |
|-------|------|---------|-------|
| O(1) | Constant | Array access | ⚡ Fastest |
| O(log n) | Logarithmic | Binary search | 🚀 Fast |
| O(n) | Linear | Single loop | 🏃 Good |
| O(n log n) | Linearithmic | Sorting | 🚶 OK |
| O(n²) | Quadratic | Nested loops | 🐌 Slow |
| O(2ⁿ) | Exponential | Recursive fibonacci | 🐢 Very slow |

### How to Calculate
```python
# O(1) — No loops
x = arr[0]

# O(n) — Single loop
for x in arr:
    print(x)

# O(n²) — Nested loop
for x in arr:
    for y in arr:
        print(x, y)

# O(log n) — Halving each time
while n > 1:
    n = n // 2

# O(n log n) — Loop with halving
for i in range(n):
    j = 1
    while j < n:
        j *= 2
```

### Rule of Thumb
- Nested loop → O(n²)
- Single loop → O(n)
- No loop, direct access → O(1)
- Halving/doubling → O(log n)

---

## 🎯 Common Problem Patterns

### Pattern 1: Frequency Count
```python
# Count occurrences of each element
from collections import Counter
freq = Counter(arr)
# freq[element] = count
```

### Pattern 2: Two Sum
```python
# Find two numbers that add up to target
def two_sum(arr, target):
    seen = {}
    for i, num in enumerate(arr):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
```

### Pattern 3: Reverse
```python
# Reverse array/string
arr[::-1]  # For copy
# Or two-pointer swap for in-place
```

### Pattern 4: Sliding Window
```python
# Find subarray with condition
window_start = 0
for window_end in range(len(arr)):
    # Add arr[window_end] to window
    # Shrink window if needed
    # Update result
```

### Pattern 5: Prefix Sum
```python
# Fast range sum queries
prefix = [0] * (len(arr) + 1)
for i in range(len(arr)):
    prefix[i+1] = prefix[i] + arr[i]
# Sum from i to j = prefix[j+1] - prefix[i]
```

---

## ✅ DSA Checklist for TCS NQT

### Must Know (Day 1-4)
- [ ] Array operations (access, append, sort)
- [ ] String operations (slice, reverse, count)
- [ ] Dictionary (create, access, count)
- [ ] Linear search
- [ ] Using built-in sort

### Should Know (Day 5-6)
- [ ] Binary search
- [ ] Two pointer technique
- [ ] Frequency counting with HashMap
- [ ] Basic recursion (factorial, fibonacci)

### Nice to Know (Day 7)
- [ ] Sliding window
- [ ] Stack/Queue operations
- [ ] Set operations

### Don't Need (Skip for TCS)
- ❌ Trees, Graphs
- ❌ Advanced DP
- ❌ Linked Lists
- ❌ Complex sorting algorithms
