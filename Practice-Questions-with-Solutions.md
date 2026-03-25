# TCS NQT — Practice Questions with Solutions

## 📊 Numerical Ability Practice

### Q1. Percentages
**A number is increased by 20% and then decreased by 20%. What is the net change?**

**Solution:**
Let number = 100
After 20% increase: 100 × 1.20 = 120
After 20% decrease: 120 × 0.80 = 96
Net change = 96 - 100 = -4 = **4% decrease**

**Shortcut**: Net effect = a + b + ab/100 = 20 + (-20) + (20×-20)/100 = 0 - 4 = **-4%**

---

### Q2. Time & Work
**A can complete a work in 12 days, B in 18 days. How many days will they take together?**

**Solution:**
LCM of 12, 18 = 36 (total work)
A's efficiency = 36/12 = 3 per day
B's efficiency = 36/18 = 2 per day
Together = 3 + 2 = 5 per day
Time = 36/5 = **7.2 days**

---

### Q3. Profit & Loss
**A shopkeeper sells an article at 10% profit. If he had bought it for 10% less and sold for ₹20 less, he would have gained 25%. Find the cost price.**

**Solution:**
Let CP = x
SP = 1.1x (10% profit)
New CP = 0.9x
New SP = 1.1x - 20
Profit = 25% of 0.9x = 0.225x
So: 1.1x - 20 = 0.9x + 0.225x
1.1x - 20 = 1.125x
-20 = 0.025x
x = 800
**CP = ₹800**

---

### Q4. Time, Speed & Distance
**A train 150m long passes a platform 350m long in 25 seconds. What is the speed of the train in km/hr?**

**Solution:**
Total distance = 150 + 350 = 500m
Time = 25 seconds
Speed = 500/25 = 20 m/s
Speed in km/hr = 20 × 18/5 = **72 km/hr**

---

### Q5. Averages
**The average of 5 numbers is 27. If one number is excluded, the average becomes 25. Find the excluded number.**

**Solution:**
Sum of 5 numbers = 27 × 5 = 135
Sum of 4 numbers = 25 × 4 = 100
Excluded number = 135 - 100 = **35**

---

## 🧠 Reasoning Practice

### Q6. Number Series
**Find the next number: 2, 6, 12, 20, 30, ?**

**Solution:**
Differences: 4, 6, 8, 10, ? → increasing by 2
Next difference = 12
Answer = 30 + 12 = **42**

---

### Q7. Blood Relations
**Pointing to a man, a woman said, "His mother is the only daughter of my mother." How is the woman related to the man?**

**Solution:**
"Only daughter of my mother" = the woman herself
So: "His mother is [the woman]"
The woman is the **mother** of the man.

---

### Q8. Coding-Decoding
**If COMPUTER is coded as DPNQVUFS, how is PRINTER coded?**

**Solution:**
C→D (+1), O→P (+1), M→N (+1)... each letter +1
P→Q, R→S, I→J, N→O, T→U, E→F, R→S
Answer: **QSJOUFS**

---

## 💻 Coding Practice

### Q9. Python — Find Maximum in Array
```python
arr = [12, 45, 7, 89, 23, 56]
max_val = arr[0]
for num in arr:
    if num > max_val:
        max_val = num
print(max_val)  # Output: 89
```

---

### Q10. Python — Check Palindrome
```python
def is_palindrome(s):
    s = s.lower().replace(" ", "")
    return s == s[::-1]

print(is_palindrome("racecar"))  # True
print(is_palindrome("hello"))    # False
```

---

### Q11. Python — Fibonacci Series
```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b

fibonacci(10)  # Output: 0 1 1 2 3 5 8 13 21 34
```

---

### Q12. Python — Count Character Frequency
```python
from collections import Counter

s = "programming"
freq = Counter(s)
for char, count in freq.most_common():
    print(f"{char}: {count}")
# Output: r:2, g:2, m:2, p:1, o:1, a:1, i:1, n:1
```

---

### Q13. Python — Second Largest Element
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

print(second_largest([12, 45, 7, 89, 23]))  # Output: 45
```

---

### Q14. Python — Check Prime
```python
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

print(is_prime(17))  # True
print(is_prime(15))  # False
```

---

## 🔥 Rapid Fire (Quick Mental Math)

1. 15% of 240 = **36**
2. 3/8 as percentage = **37.5%**
3. LCM of 12 and 18 = **36**
4. HCF of 24 and 36 = **12**
5. 2^10 = **1024**
6. 15² = **225**
7. √144 = **12**
8. 125 × 8 = **1000**
9. Average of 10, 20, 30, 40, 50 = **30**
10. 30% of 150 = **45**

---

## ✅ Answer Key

| Q | Answer |
|---|--------|
| 1 | 4% decrease |
| 2 | 7.2 days |
| 3 | ₹800 |
| 4 | 72 km/hr |
| 5 | 35 |
| 6 | 42 |
| 7 | Mother |
| 8 | QSJOUFS |
| 9-14 | See code |
