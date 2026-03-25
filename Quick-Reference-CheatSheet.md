# TCS NQT Quick Reference Cheat Sheet

## 📐 Math Formulas You MUST Know

### Powers & Roots
```
2¹=2    2²=4    2³=8    2⁴=16   2⁵=32   2⁶=64   2⁷=128  2⁸=256  2⁹=512  2¹⁰=1024
3¹=3    3²=9    3³=27   3⁴=81   3⁵=243
4¹=4    4²=16   4³=64   4⁴=256
5¹=5    5²=25   5³=125  5⁴=625
√2=1.414  √3=1.732  √5=2.236  √7=2.646  √10=3.162
```

### Squares (1-30)
```
1=1   2=4   3=9   4=16  5=25  6=36  7=49  8=64  9=81  10=100
11=121 12=144 13=169 14=196 15=225 16=256 17=289 18=324 19=361 20=400
21=441 22=484 23=529 24=576 25=625 26=676 27=729 28=784 29=841 30=900
```

### Cubes (1-15)
```
1=1   2=8   3=27  4=64  5=125 6=216 7=343 8=512 9=729 10=1000
11=1331 12=1728 13=2197 14=2744 15=3375
```

### Common Fractions
```
1/2=0.5=50%    1/3=0.333=33.33%    1/4=0.25=25%
1/5=0.2=20%    1/6=0.166=16.67%    1/7=0.142=14.28%
1/8=0.125=12.5%  1/9=0.111=11.11%    1/10=0.1=10%
1/11=0.09=9.09%  1/12=0.083=8.33%    1/15=0.066=6.67%
1/16=0.0625=6.25%  1/20=0.05=5%      1/25=0.04=4%
```

---

## 🔤 Alphabet Positions (MEMORIZE!)

```
A=1   B=2   C=3   D=4   E=5   F=6   G=7   H=8   I=9   J=10
K=11  L=12  M=13  N=14  O=15  P=16  Q=17  R=18  S=19  T=20
U=21  V=22  W=23  X=24  Y=25  Z=26

EJOTY = 5, 10, 15, 20, 25
Reverse: 27 - position
```

---

## 🧭 Directions
```
         N
      NW   NE
    W    •    E
      SW   SE
         S

Clockwise: N→E→S→W
Counter:   N→W→S→E
```

---

## ⏰ Clock Key Facts
- Minute hand: 6°/min
- Hour hand: 0.5°/min
- Relative speed: 5.5°/min
- 1 minute = 6° on clock face

---

## 🃏 Cards
- 52 cards total
- 4 suits: Hearts(♥), Diamonds(♦), Clubs(♣), Spades(♠)
- Each suit: A, 2-10, J, Q, K (13 cards)
- Red: Hearts + Diamonds (26)
- Black: Clubs + Spades (26)
- Face cards: J, Q, K (12 total)
- Honors: A, K, Q, J, 10 (20 total)

---

## 🎲 Dice
- Opposite faces sum to 7
- 1↔6, 2↔5, 3↔4
- 3 visible faces = 3 different numbers
- Total outcomes with 2 dice = 36

---

## 🐍 Python Cheat Sheet

### List Operations
```python
arr.append(x)      # Add to end
arr.pop()          # Remove from end
arr.pop(i)         # Remove at index i
arr.insert(i, x)   # Insert at index i
arr.sort()         # Sort in place
sorted(arr)        # Return sorted copy
arr.reverse()      # Reverse in place
arr.count(x)       # Count occurrences
arr.index(x)       # Find index
len(arr)           # Length
arr[::-1]          # Reverse copy
arr[::2]           # Every 2nd element
min(arr), max(arr), sum(arr)
```

### String Operations
```python
s.lower()          # Lowercase
s.upper()          # Uppercase
s.strip()          # Remove whitespace
s.split()          # Split into list
s.replace(a, b)    # Replace a with b
s.find(sub)        # Find substring
s.count(sub)       # Count substring
s.startswith(x)    # Check prefix
s.endswith(x)      # Check suffix
s.isdigit()        # All digits?
s.isalpha()        # All letters?
''.join(list)      # Join list to string
```

### Dictionary Operations
```python
d[key]             # Access value
d.get(key, default) # Safe access
d.keys()           # All keys
d.values()         # All values
d.items()          # Key-value pairs
d.pop(key)         # Remove key
key in d           # Check existence
```

### Input/Output
```python
# Single integer
n = int(input())

# Multiple integers on one line
a, b = map(int, input().split())

# List of integers
arr = list(map(int, input().split()))

# Multiple lines
for _ in range(n):
    x = int(input())

# Output
print(x)           # Print with newline
print(x, end="")   # Print without newline
print(*arr)        # Print list elements
print(f"{x:.2f}")  # Formatted (2 decimal)
```

---

## ⏱️ Time Complexity Cheat Sheet

| Operation | Time |
|-----------|------|
| Access array[i] | O(1) |
| Search array (unsorted) | O(n) |
| Binary Search (sorted) | O(log n) |
| Sort | O(n log n) |
| HashMap access | O(1) avg |
| Stack push/pop | O(1) |
| Queue enqueue/dequeue | O(1) |
| Linked List search | O(n) |
| Linked List insert | O(1) at head |
| Nested loop | O(n²) |

---

## 🎯 Last-Minute Checklist

Before exam:
- [ ] Know squares 1-30 and cubes 1-15
- [ ] Know alphabet positions (EJOTY)
- [ ] Practice 5 coding problems
- [ ] Do 1 full mock test
- [ ] Sleep well!

During exam:
- [ ] Read all questions first
- [ ] Start with easy ones
- [ ] Attempt ALL (no negative marking)
- [ ] Don't spend >1.5 min on aptitude
- [ ] Budget 45 min per coding question
- [ ] Check for edge cases in code
