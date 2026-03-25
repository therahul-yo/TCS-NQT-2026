# Coding Section — Concepts, Patterns & Practice

## 📋 TCS NQT Coding Section Overview
- **2 questions, 90 minutes**
- **Languages allowed**: C, C++, Java, Python
- **Difficulty**: Easy to Medium
- **This section decides**: Ninja vs Digital vs Prime!

---

## 🔢 Arrays — Most Common Topic

### Essential Problems

#### 1. Two Sum (Very Common)
```python
def two_sum(arr, target):
    seen = {}
    for i, num in enumerate(arr):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []
# Time: O(n), Space: O(n)
```

#### 2. Reverse Array
```python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    return arr
# Time: O(n), Space: O(1)
```

#### 3. Rotate Array by K positions
```python
def rotate_array(arr, k):
    k = k % len(arr)
    arr[:] = arr[-k:] + arr[:-k]
    return arr
# OR using reverse method (in-place):
def rotate_array(arr, k):
    k = k % len(arr)
    arr.reverse()
    arr[:k] = reversed(arr[:k])
    arr[k:] = reversed(arr[k:])
    return arr
```

#### 4. Find Maximum/Minimum
```python
def find_max(arr):
    max_val = arr[0]
    for num in arr:
        if num > max_val:
            max_val = num
    return max_val
# Or simply: max(arr)
```

#### 5. Second Largest Element
```python
def second_largest(arr):
    first = second = float('-inf')
    for num in arr:
        if num > first:
            second = first
            first = num
        elif num > second and num != first:
            second = num
    return second
# Time: O(n), Space: O(1)
```

#### 6. Remove Duplicates
```python
def remove_duplicates(arr):
    return list(dict.fromkeys(arr))  # preserves order
# OR
def remove_duplicates(arr):
    seen = set()
    result = []
    for num in arr:
        if num not in seen:
            seen.add(num)
            result.append(num)
    return result
```

---

## 📝 Strings — Very Common

### Essential Problems

#### 1. Palindrome Check
```python
def is_palindrome(s):
    s = s.lower().replace(" ", "")
    return s == s[::-1]
# OR without slicing:
def is_palindrome(s):
    s = s.lower().replace(" ", "")
    left, right = 0, len(s) - 1
    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1
    return True
```

#### 2. Anagram Check
```python
def is_anagram(s1, s2):
    return sorted(s1.lower()) == sorted(s2.lower())
# OR using Counter:
from collections import Counter
def is_anagram(s1, s2):
    return Counter(s1.lower()) == Counter(s2.lower())
```

#### 3. Character Frequency
```python
def char_frequency(s):
    freq = {}
    for char in s:
        freq[char] = freq.get(char, 0) + 1
    return freq
# OR: Counter(s)
```

#### 4. Reverse String
```python
def reverse_string(s):
    return s[::-1]
# OR manual:
def reverse_string(s):
    result = ""
    for char in s:
        result = char + result
    return result
```

#### 5. Count Vowels and Consonants
```python
def count_vc(s):
    vowels = "aeiouAEIOU"
    v = c = 0
    for char in s:
        if char.isalpha():
            if char in vowels:
                v += 1
            else:
                c += 1
    return v, c
```

#### 6. First Non-Repeating Character
```python
def first_unique(s):
    from collections import Counter
    freq = Counter(s)
    for char in s:
        if freq[char] == 1:
            return char
    return None
```

---

## 🔢 Number Theory

### Essential Problems

#### 1. Check Prime
```python
def is_prime(n):
    if n < 2:
        return False
    if n < 4:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True
# Time: O(√n)
```

#### 2. Fibonacci
```python
def fibonacci(n):
    if n <= 1:
        return n
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b
# Time: O(n), Space: O(1)
```

#### 3. Factorial
```python
def factorial(n):
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result
# OR recursive:
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)
```

#### 4. GCD/LCM
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

def lcm(a, b):
    return (a * b) // gcd(a, b)
```

#### 5. Sum of Digits
```python
def digit_sum(n):
    total = 0
    n = abs(n)
    while n > 0:
        total += n % 10
        n //= 10
    return total
```

#### 6. Armstrong Number
```python
def is_armstrong(n):
    digits = str(n)
    power = len(digits)
    return n == sum(int(d) ** power for d in digits)
```

---

## 📊 Sorting & Searching

### Bubble Sort
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr
# Time: O(n²)
```

### Binary Search
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
# Time: O(log n) — Array must be sorted!
```

### Linear Search
```python
def linear_search(arr, target):
    for i, num in enumerate(arr):
        if num == target:
            return i
    return -1
# Time: O(n)
```

---

## 🗺️ HashMap / Dictionary — Very Useful

### Common Patterns

#### 1. Count Occurrences
```python
from collections import Counter
counts = Counter(arr)
# counts[element] = frequency
```

#### 2. Group Anagrams
```python
def group_anagrams(words):
    groups = {}
    for word in words:
        key = ''.join(sorted(word))
        if key not in groups:
            groups[key] = []
        groups[key].append(word)
    return list(groups.values())
```

#### 3. Two Sum with HashMap
```python
def two_sum(arr, target):
    seen = {}
    for i, num in enumerate(arr):
        if target - num in seen:
            return [seen[target - num], i]
        seen[num] = i
```

#### 4. Find Duplicates
```python
def find_duplicates(arr):
    seen = set()
    duplicates = set()
    for num in arr:
        if num in seen:
            duplicates.add(num)
        seen.add(num)
    return list(duplicates)
```

---

## 💡 Basic DP (Dynamic Programming)

### 1. Climbing Stairs (Classic!)
```python
def climb_stairs(n):
    if n <= 2:
        return n
    a, b = 1, 2
    for _ in range(3, n + 1):
        a, b = b, a + b
    return b
# Same as fibonacci!
```

### 2. Maximum Subarray Sum (Kadane's Algorithm)
```python
def max_subarray(arr):
    max_sum = current = arr[0]
    for num in arr[1:]:
        current = max(num, current + num)
        max_sum = max(max_sum, current)
    return max_sum
# Time: O(n)
```

### 3. Longest Common Subsequence
```python
def lcs(s1, s2):
    m, n = len(s1), len(s2)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if s1[i-1] == s2[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])
    return dp[m][n]
```

---

## 📚 Stack & Queue Basics

### Stack (LIFO)
```python
stack = []
stack.append(1)    # push
stack.pop()        # pop (returns 1)
stack[-1]          # peek/top
len(stack)         # size
```

### Queue (FIFO)
```python
from collections import deque
queue = deque()
queue.append(1)     # enqueue
queue.popleft()     # dequeue
queue[0]            # front
```

### Common: Balanced Parentheses
```python
def is_balanced(s):
    stack = []
    pairs = {')': '(', '}': '{', ']': '['}
    for char in s:
        if char in '({[':
            stack.append(char)
        elif char in ')}]':
            if not stack or stack[-1] != pairs[char]:
                return False
            stack.pop()
    return len(stack) == 0
```

---

## 🔗 Linked List Basics

### Node Definition
```python
class Node:
    def __init__(self, val):
        self.val = val
        self.next = None
```

### Reverse Linked List
```python
def reverse(head):
    prev = None
    current = head
    while current:
        next_node = current.next
        current.next = prev
        prev = current
        current = next_node
    return prev
```

### Find Middle
```python
def find_middle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
    return slow
```

---

## 🎯 Exam Day Coding Tips

1. **Start with the easier question** — read both first
2. **Handle edge cases**: empty input, single element, negative numbers
3. **Test with given examples** before submitting
4. **If stuck, try brute force first** — then optimize
5. **Use built-in functions** when allowed (sort, max, min, Counter)
6. **Time management** — don't spend 60+ min on one problem
7. **Partial marks** — even a brute force solution gets some marks
8. **Input/Output** — read from stdin, print to stdout

### Standard I/O Template
```python
# Reading input
n = int(input())
arr = list(map(int, input().split()))
# OR for multiple lines:
for _ in range(n):
    line = input().split()

# Output
print(result)
```
