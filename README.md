# Python Programming Exercises For Practice (150 Questions)

<img width="750" height="1000" alt="image" src="https://github.com/user-attachments/assets/b8281da2-e807-4ef3-ae34-653e03ea5c17" />

## Basic Exercises (1-50)

### 1. Find numbers divisible by 7 but not multiple of 5
```python
l = []
for i in range(2000, 3201):
    if (i % 7 == 0) and (i % 5 != 0):
        l.append(str(i))
print(','.join(l))
```

### 2. Factorial Calculation
```python
def fact(x):
    if x == 0:
        return 1
    return x * fact(x - 1)

x = int(input())
print(fact(x))
```

### 3. Generate Dictionary with Squares
```python
n = int(input())
d = dict()
for i in range(1, n + 1):
    d[i] = i * i
print(d)
```

### 4. List and Tuple from Comma-Separated Numbers
```python
values = input()
l = values.split(",")
t = tuple(l)
print(l)
print(t)
```

### 5. String Input/Output Class
```python
class InputOutString(object):
    def __init__(self):
        self.s = ""
    
    def getString(self):
        self.s = input()
    
    def printString(self):
        print(self.s.upper())

strObj = InputOutString()
strObj.getString()
strObj.printString()
```

### 6. Formula Calculation
```python
import math
c = 50
h = 30
value = []
items = [x for x in input().split(',')]
for d in items:
    value.append(str(int(round(math.sqrt(2 * c * float(d) / h))))
print(','.join(value))
```

### 7. 2D Array Generation
```python
input_str = input()
dimensions = [int(x) for x in input_str.split(',')]
rowNum = dimensions[0]
colNum = dimensions[1]
multilist = [[0 for col in range(colNum)] for row in range(rowNum)]

for row in range(rowNum):
    for col in range(colNum):
        multilist[row][col] = row * col

print(multilist)
```

### 8. Sort Words Alphabetically
```python
items = [x for x in input().split(',')]
items.sort()
print(','.join(items))
```

### 9. Capitalize Lines
```python
lines = []
while True:
    s = input()
    if s:
        lines.append(s.upper())
    else:
        break

for sentence in lines:
    print(sentence)
```

### 10. Remove Duplicates and Sort
```python
s = input()
words = [word for word in s.split(" ")]
print(" ".join(sorted(list(set(words)))))
```

## Intermediate Exercises (51-100)

### 51. Rectangle Area Calculation
```python
class Rectangle(object):
    def __init__(self, l, w):
        self.length = l
        self.width = w
    
    def area(self):
        return self.length * self.width

aRectangle = Rectangle(2, 10)
print(aRectangle.area())
```

### 52. Shape and Square Classes
```python
class Shape(object):
    def __init__(self):
        pass
    
    def area(self):
        return 0

class Square(Shape):
    def __init__(self, l):
        Shape.__init__(self)
        self.length = l
    
    def area(self):
        return self.length * self.length

aSquare = Square(3)
print(aSquare.area())
```

### 68. Binary Search
```python
import math

def bin_search(li, element):
    bottom = 0
    top = len(li) - 1
    index = -1
    
    while top >= bottom and index == -1:
        mid = int(math.floor((top + bottom) / 2.0))
        if li[mid] == element:
            index = mid
        elif li[mid] > element:
            top = mid - 1
        else:
            bottom = mid + 1
    
    return index

li = [2, 5, 7, 9, 11, 17, 222]
print(bin_search(li, 11))
print(bin_search(li, 12))
```

### 78. Execution Time Measurement
```python
from timeit import Timer
t = Timer("for i in range(100):1+1")
print(t.timeit())
```

### 94. Chinese Puzzle (Chickens and Rabbits)
```python
def solve(numheads, numlegs):
    ns = 'No solutions!'
    for i in range(numheads + 1):
        j = numheads - i
        if 2 * i + 4 * j == numlegs:
            return i, j
    return ns, ns

numheads = 35
numlegs = 94
solutions = solve(numheads, numlegs)
print(solutions)
```

## Mathematical Exercises (101-130)

### 110. GCD Calculation
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

print(gcd(48, 18))
```

### 111. LCM Calculation
```python
def lcm(a, b):
    return abs(a * b) // gcd(a, b)

print(lcm(12, 18))
```

### 118. Fibonacci Series
```python
def fibonacci(n):
    a, b = 0, 1
    result = []
    for _ in range(n):
        result.append(a)
        a, b = b, a + b
    return result

print(fibonacci(10))
```

### 125. Quadratic Equation Roots
```python
import math

def quadratic_roots(a, b, c):
    discriminant = b**2 - 4 * a * c
    if discriminant < 0:
        return "No real roots"
    root1 = (-b + math.sqrt(discriminant)) / (2 * a)
    root2 = (-b - math.sqrt(discriminant)) / (2 * a)
    return root1, root2

print(quadratic_roots(1, -3, 2))
```

### 131. Triangle Area using Heron's Formula
```python
import math

def triangle_area_heron(a, b, c):
    s = (a + b + c) / 2
    return math.sqrt(s * (s - a) * (s - b) * (s - c))

print(triangle_area_heron(3, 4, 5))
```

## Advanced Exercises (131-150)

### 140. Compound Interest
```python
def compound_interest(principal, rate, time, frequency):
    return principal * (1 + rate / frequency) ** (frequency * time)

print(compound_interest(1000, 0.05, 10, 1))
```

### 142-147. Number System Conversions
```python
# Decimal to Binary
def decimal_to_binary(n):
    return bin(n)[2:]

# Binary to Decimal
def binary_to_decimal(b):
    return int(b, 2)

# Decimal to Hexadecimal
def decimal_to_hex(n):
    return hex(n)[2:]

# Hexadecimal to Decimal
def hex_to_decimal(h):
    return int(h, 16)

# Decimal to Octal
def decimal_to_octal(n):
    return oct(n)[2:]

# Octal to Decimal
def octal_to_decimal(o):
    return int(o, 8)

print(decimal_to_binary(10))
print(binary_to_decimal('1010'))
print(decimal_to_hex(255))
print(hex_to_decimal('ff'))
print(decimal_to_octal(64))
print(octal_to_decimal('100'))
```

### 148-149. ASCII Conversions
```python
# Character to ASCII
def char_to_ascii(c):
    return ord(c)

# ASCII to Character
def ascii_to_char(n):
    return chr(n)

print(char_to_ascii('A'))
print(ascii_to_char(65))
```

### 150. Random Password Generator
```python
import random
import string

def generate_password(length):
    chars = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choice(chars) for _ in range(length))

print(generate_password(12))
```

## Utility Functions

### List Operations
```python
# Sum of list elements
def sum_list(lst):
    return sum(lst)

# Find maximum in list
def find_max(lst):
    return max(lst)

# Find minimum in list
def find_min(lst):
    return min(lst)

# Find second largest
def second_largest(lst):
    return sorted(set(lst))[-2]

# Count vowels in string
def count_vowels(s):
    vowels = 'aeiouAEIOU'
    count = 0
    for char in s:
        if char in vowels:
            count += 1
    return count

# Check palindrome
def is_palindrome(s):
    return s == s[::-1]

# Remove punctuation
import string
def remove_punctuation(s):
    return s.translate(str.maketrans('', '', string.punctuation))
```

### Mathematical Functions
```python
import math

# Check perfect square
def is_perfect_square(n):
    return int(n**0.5)**2 == n

# Find factors
def factors(n):
    return [i for i in range(1, n + 1) if n % i == 0]

# Sum of digits
def sum_digits(n):
    return sum(int(d) for d in str(n))

# Check Armstrong number
def is_armstrong(n):
    digits = [int(d) for d in str(n)]
    return sum(d**3 for d in digits) == n

# Factorial using recursion
def factorial(n):
    return 1 if n == 0 else n * factorial(n - 1)
```

These exercises cover a wide range of Python programming concepts from basic syntax to advanced algorithms. Each solution is ready to run and demonstrates practical Python programming techniques.

---

<br>

<h2 align="center">✨ Author</h2>

<p align="center">
  <b>Saad Abdur Razzaq</b><br>
  <i>Machine Learning Engineer | Effixly AI</i>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/saadarazzaq" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:sabdurrazzaq124@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="https://saadarazzaq.dev" target="_blank">
    <img src="https://img.shields.io/badge/Website-000000?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
  <a href="https://github.com/saadabdurrazzaq" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
</p>

<br>

---

<div align="center">

### ⭐ Don't forget to star this repository if you find it helpful!

</div>
