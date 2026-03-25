# Coding Problems — Easy to Medium (Step by Step)

## 🟢 Level 1: Absolute Beginner (Start Here!)

### Problem 1: Print Hello World
```python
print("Hello, World!")
```

### Problem 2: Add Two Numbers
```python
a = int(input())
b = int(input())
print(a + b)
```

### Problem 3: Even or Odd
```python
n = int(input())
if n % 2 == 0:
    print("Even")
else:
    print("Odd")
```

### Problem 4: Find Largest of Three
```python
a, b, c = map(int, input().split())
print(max(a, b, c))
# OR without max():
if a >= b and a >= c:
    print(a)
elif b >= a and b >= c:
    print(b)
else:
    print(c)
```

### Problem 5: Multiplication Table
```python
n = int(input())
for i in range(1, 11):
    print(f"{n} x {i} = {n * i}")
```

---

## 🟢 Level 2: Basic Loops & Conditions

### Problem 6: Sum of N Numbers
```python
n = int(input())
total = 0
for i in range(1, n + 1):
    total += i
print(total)
# OR shortcut: n * (n + 1) // 2
```

### Problem 7: Factorial
```python
n = int(input())
result = 1
for i in range(1, n + 1):
    result *= i
print(result)
```

### Problem 8: Check Prime
```python
n = int(input())
if n < 2:
    print("Not Prime")
else:
    is_prime = True
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            is_prime = False
            break
    print("Prime" if is_prime else "Not Prime")
```

### Problem 9: Fibonacci Series (First N)
```python
n = int(input())
a, b = 0, 1
for _ in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

### Problem 10: Reverse a Number
```python
n = int(input())
rev = 0
while n > 0:
    rev = rev * 10 + n % 10
    n //= 10
print(rev)
```

---

## 🟡 Level 3: Arrays

### Problem 11: Find Maximum in Array
```python
arr = list(map(int, input().split()))
max_val = arr[0]
for num in arr:
    if num > max_val:
        max_val = num
print(max_val)
```

### Problem 12: Find Minimum in Array
```python
arr = list(map(int, input().split()))
min_val = arr[0]
for num in arr:
    if num < min_val:
        min_val = num
print(min_val)
```

### Problem 13: Sum of Array Elements
```python
arr = list(map(int, input().split()))
print(sum(arr))
```

### Problem 14: Reverse Array
```python
arr = list(map(int, input().split()))
print(arr[::-1])
# OR in-place:
left, right = 0, len(arr) - 1
while left < right:
    arr[left], arr[right] = arr[right], arr[left]
    left += 1
    right -= 1
print(arr)
```

### Problem 15: Count Even and Odd
```python
arr = list(map(int, input().split()))
even = odd = 0
for num in arr:
    if num % 2 == 0:
        even += 1
    else:
        odd += 1
print(f"Even: {even}, Odd: {odd}")
```

### Problem 16: Second Largest Element
```python
arr = list(map(int, input().split()))
first = second = float('-inf')
for num in arr:
    if num > first:
        second = first
        first = num
    elif num > second and num != first:
        second = num
print(second)
```

### Problem 17: Remove Duplicates
```python
arr = list(map(int, input().split()))
seen = set()
result = []
for num in arr:
    if num not in seen:
        seen.add(num)
        result.append(num)
print(result)
# OR: list(dict.fromkeys(arr))
```

### Problem 18: Rotate Array by K
```python
arr = list(map(int, input().split()))
k = int(input())
k = k % len(arr)
arr[:] = arr[-k:] + arr[:-k]
print(arr)
```

### Problem 19: Check if Sorted
```python
arr = list(map(int, input().split()))
is_sorted = True
for i in range(len(arr) - 1):
    if arr[i] > arr[i + 1]:
        is_sorted = False
        break
print("Sorted" if is_sorted else "Not Sorted")
```

### Problem 20: Linear Search
```python
arr = list(map(int, input().split()))
target = int(input())
found = -1
for i, num in enumerate(arr):
    if num == target:
        found = i
        break
print(found)  # Index or -1 if not found
```

---

## 🟡 Level 4: Strings

### Problem 21: Reverse String
```python
s = input()
print(s[::-1])
```

### Problem 22: Check Palindrome
```python
s = input().lower().replace(" ", "")
if s == s[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

### Problem 23: Count Vowels and Consonants
```python
s = input().lower()
vowels = "aeiou"
v = c = 0
for char in s:
    if char.isalpha():
        if char in vowels:
            v += 1
        else:
            c += 1
print(f"Vowels: {v}, Consonants: {c}")
```

### Problem 24: Character Frequency
```python
s = input()
freq = {}
for char in s:
    freq[char] = freq.get(char, 0) + 1
for char, count in freq.items():
    print(f"{char}: {count}")
```

### Problem 25: Check Anagram
```python
s1 = input().lower().replace(" ", "")
s2 = input().lower().replace(" ", "")
if sorted(s1) == sorted(s2):
    print("Anagram")
else:
    print("Not Anagram")
```

### Problem 26: First Non-Repeating Character
```python
s = input()
freq = {}
for char in s:
    freq[char] = freq.get(char, 0) + 1
for char in s:
    if freq[char] == 1:
        print(char)
        break
else:
    print("None")
```

### Problem 27: Count Words in String
```python
s = input()
words = s.split()
print(len(words))
```

### Problem 28: Capitalize First Letter of Each Word
```python
s = input()
print(s.title())
# OR manual:
words = s.split()
result = " ".join(word[0].upper() + word[1:] for word in words)
print(result)
```

---

## 🟠 Level 5: Number Problems

### Problem 29: GCD (Greatest Common Divisor)
```python
a, b = map(int, input().split())
while b:
    a, b = b, a % b
print(a)
```

### Problem 30: LCM (Least Common Multiple)
```python
a, b = map(int, input().split())
def gcd(x, y):
    while y:
        x, y = y, x % y
    return x
lcm = (a * b) // gcd(a, b)
print(lcm)
```

### Problem 31: Sum of Digits
```python
n = int(input())
total = 0
while n > 0:
    total += n % 10
    n //= 10
print(total)
```

### Problem 32: Armstrong Number
```python
n = int(input())
digits = str(n)
power = len(digits)
if n == sum(int(d) ** power for d in digits):
    print("Armstrong")
else:
    print("Not Armstrong")
```

### Problem 33: Print All Primes Up to N
```python
n = int(input())
for num in range(2, n + 1):
    is_prime = True
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            is_prime = False
            break
    if is_prime:
        print(num, end=" ")
```

---

## 🟠 Level 6: HashMap Problems

### Problem 34: Two Sum
```python
arr = list(map(int, input().split()))
target = int(input())
seen = {}
for i, num in enumerate(arr):
    complement = target - num
    if complement in seen:
        print(seen[complement], i)
        break
    seen[num] = i
```

### Problem 35: Most Frequent Element
```python
from collections import Counter
arr = list(map(int, input().split()))
freq = Counter(arr)
print(freq.most_common(1)[0][0])
```

### Problem 36: Group Anagrams
```python
from collections import defaultdict
words = input().split()
groups = defaultdict(list)
for word in words:
    key = ''.join(sorted(word))
    groups[key].append(word)
for group in groups.values():
    print(group)
```

### Problem 37: Find Duplicates in Array
```python
arr = list(map(int, input().split()))
seen = set()
duplicates = set()
for num in arr:
    if num in seen:
        duplicates.add(num)
    seen.add(num)
print(list(duplicates))
```

---

## 🔴 Level 7: Sorting & Searching

### Problem 38: Binary Search
```python
arr = list(map(int, input().split()))
target = int(input())
left, right = 0, len(arr) - 1
result = -1
while left <= right:
    mid = (left + right) // 2
    if arr[mid] == target:
        result = mid
        break
    elif arr[mid] < target:
        left = mid + 1
    else:
        right = mid - 1
print(result)
```

### Problem 39: Count Occurrences in Sorted Array
```python
arr = list(map(int, input().split()))
target = int(input())
count = 0
for num in arr:
    if num == target:
        count += 1
    elif num > target:
        break
print(count)
```

### Problem 40: Find Peak Element
```python
arr = list(map(int, input().split()))
for i in range(len(arr)):
    if (i == 0 or arr[i] >= arr[i-1]) and (i == len(arr)-1 or arr[i] >= arr[i+1]):
        print(arr[i])
        break
```

---

## 🔴 Level 8: Basic DP

### Problem 41: Fibonacci (DP)
```python
n = int(input())
if n <= 1:
    print(n)
else:
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    print(b)
```

### Problem 42: Climbing Stairs
```python
# How many ways to reach step n (1 or 2 steps at a time)
n = int(input())
if n <= 2:
    print(n)
else:
    a, b = 1, 2
    for _ in range(3, n + 1):
        a, b = b, a + b
    print(b)
```

### Problem 43: Maximum Subarray Sum (Kadane's)
```python
arr = list(map(int, input().split()))
max_sum = current = arr[0]
for num in arr[1:]:
    current = max(num, current + num)
    max_sum = max(max_sum, current)
print(max_sum)
```

### Problem 44: Coin Change (Minimum Coins)
```python
def min_coins(coins, amount):
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0
    for i in range(1, amount + 1):
        for coin in coins:
            if coin <= i:
                dp[i] = min(dp[i], dp[i - coin] + 1)
    return dp[amount] if dp[amount] != float('inf') else -1

coins = [1, 5, 10, 25]
amount = int(input())
print(min_coins(coins, amount))
```

---

## 📝 Solutions Template for TCS

### Standard Input Template
```python
# Read number of test cases
t = int(input())

for _ in range(t):
    # Read inputs
    n = int(input())
    arr = list(map(int, input().split()))
    
    # Solve
    result = your_solution(arr)
    
    # Print output
    print(result)
```

### Function Template
```python
def solve(arr):
    # Your logic here
    return result

# Read and call
n = int(input())
arr = list(map(int, input().split()))
print(solve(arr))
```

---

## 🎯 Practice Order (Do in This Order!)

1. Problems 1-5 (Variables & basics)
2. Problems 6-10 (Loops & conditions)
3. Problems 11-20 (Arrays)
4. Problems 21-28 (Strings)
5. Problems 29-33 (Number problems)
6. Problems 34-37 (HashMap)
7. Problems 38-40 (Searching)
8. Problems 41-44 (Basic DP)

**Do at least 5 problems per day for the next 8 days!**
