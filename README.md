# Python Programming Exercises (150 Questions)

A comprehensive collection of 150 Python programming exercises with complete solutions, covering basic to advanced concepts.

<img width="750" height="1000" alt="image" src="https://github.com/user-attachments/assets/83a8c8e2-522c-4024-bb92-39b3d3e85f33" />


## Table of Contents 📑

- [Basic Exercises (1-50)](#basic-exercises-1-50)
- [Intermediate Exercises (51-100)](#intermediate-exercises-51-100)
- [Mathematical Exercises (101-130)](#mathematical-exercises-101-130)
- [Advanced Exercises (131-150)](#advanced-exercises-131-150)
- [How to Use](#how-to-use)

---

## Basic Exercises (1-50) 🔰

### 1. Divisible by 7 but not 5
**Problem**: Find numbers between 2000-3200 divisible by 7 but not multiples of 5.
```python
l = []
for i in range(2000, 3201):
    if (i % 7 == 0) and (i % 5 != 0):
        l.append(str(i))
print(','.join(l))
```

### 2. Factorial Calculation
**Problem**: Compute factorial of a given number.
```python
def fact(x):
    if x == 0:
        return 1
    return x * fact(x - 1)

x = int(input())
print(fact(x))
```

### 3. Square Dictionary
**Problem**: Generate dictionary with numbers as keys and their squares as values.
```python
n = int(input())
d = dict()
for i in range(1, n + 1):
    d[i] = i * i
print(d)
```

### 4. List and Tuple Conversion
**Problem**: Convert comma-separated numbers to list and tuple.
```python
values = input()
l = values.split(",")
t = tuple(l)
print(l)
print(t)
```

### 5. String Manipulation Class
**Problem**: Class with methods to get and print uppercase string.
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
**Problem**: Compute Q = √[(2*C*D)/H] with C=50, H=30.
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
**Problem**: Create 2D array where element[i][j] = i*j.
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

### 8. Word Sorting
**Problem**: Sort comma-separated words alphabetically.
```python
items = [x for x in input().split(',')]
items.sort()
print(','.join(items))
```

### 9. Line Capitalization
**Problem**: Capitalize all characters in input lines.
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
**Problem**: Remove duplicate words and sort alphanumerically.
```python
s = input()
words = [word for word in s.split(" ")]
print(" ".join(sorted(list(set(words)))))
```

### 11. Binary Divisible by 5
**Problem**: Check 4-digit binary numbers divisible by 5.
```python
value = []
items = [x for x in input().split(',')]
for p in items:
    intp = int(p, 2)
    if not intp % 5:
        value.append(p)
print(','.join(value))
```

### 12. Even Digit Numbers
**Problem**: Find numbers between 1000-3000 with all even digits.
```python
values = []
for i in range(1000, 3001):
    s = str(i)
    if all(int(digit) % 2 == 0 for digit in s):
        values.append(s)
print(",".join(values))
```

### 13. Count Letters and Digits
**Problem**: Count letters and digits in a sentence.
```python
s = input()
d = {"DIGITS": 0, "LETTERS": 0}
for c in s:
    if c.isdigit():
        d["DIGITS"] += 1
    elif c.isalpha():
        d["LETTERS"] += 1
print("LETTERS", d["LETTERS"])
print("DIGITS", d["DIGITS"])
```

### 14. Count Upper/Lower Case
**Problem**: Count uppercase and lowercase letters.
```python
s = input()
d = {"UPPER CASE": 0, "LOWER CASE": 0}
for c in s:
    if c.isupper():
        d["UPPER CASE"] += 1
    elif c.islower():
        d["LOWER CASE"] += 1
print("UPPER CASE", d["UPPER CASE"])
print("LOWER CASE", d["LOWER CASE"])
```

### 15. Pattern Sum
**Problem**: Compute a + aa + aaa + aaaa for given digit.
```python
a = input()
n1 = int(a)
n2 = int(a * 2)
n3 = int(a * 3)
n4 = int(a * 4)
print(n1 + n2 + n3 + n4)
```

### 16. Square Odd Numbers
**Problem**: Square each odd number in a list.
```python
values = input()
numbers = [x for x in values.split(",") if int(x) % 2 != 0]
print(",".join(numbers))
```

### 17. Bank Transaction Log
**Problem**: Compute net amount from transaction log.
```python
netAmount = 0
while True:
    s = input()
    if not s:
        break
    values = s.split(" ")
    operation = values[0]
    amount = int(values[1])
    if operation == "D":
        netAmount += amount
    elif operation == "W":
        netAmount -= amount
print(netAmount)
```

### 18. Password Validation
**Problem**: Validate passwords with specific criteria.
```python
import re
value = []
items = [x for x in input().split(',')]
for p in items:
    if len(p) < 6 or len(p) > 12:
        continue
    if not re.search("[a-z]", p):
        continue
    elif not re.search("[0-9]", p):
        continue
    elif not re.search("[A-Z]", p):
        continue
    elif not re.search("[$#@]", p):
        continue
    value.append(p)
print(",".join(value))
```

### 19. Sort Tuples
**Problem**: Sort (name, age, height) tuples by multiple keys.
```python
from operator import itemgetter
l = []
while True:
    s = input()
    if not s:
        break
    l.append(tuple(s.split(",")))
print(sorted(l, key=itemgetter(0, 1, 2)))
```

### 20. Divisible by 7 Generator
**Problem**: Generator for numbers divisible by 7 in range.
```python
def putNumbers(n):
    i = 0
    while i < n:
        j = i
        i = i + 1
        if j % 7 == 0:
            yield j

for i in putNumbers(100):
    print(i)
```

### 21. Robot Movement
**Problem**: Calculate robot's distance from origin.
```python
import math
pos = [0, 0]
while True:
    s = input()
    if not s:
        break
    movement = s.split(" ")
    direction = movement[0]
    steps = int(movement[1])
    if direction == "UP":
        pos[0] += steps
    elif direction == "DOWN":
        pos[0] -= steps
    elif direction == "LEFT":
        pos[1] -= steps
    elif direction == "RIGHT":
        pos[1] += steps
print(int(round(math.sqrt(pos[1] ** 2 + pos[0] ** 2))))
```

### 22. Word Frequency
**Problem**: Count and sort word frequencies.
```python
freq = {}
line = input()
for word in line.split():
    freq[word] = freq.get(word, 0) + 1
words = sorted(freq.keys())
for w in words:
    print("%s:%d" % (w, freq[w]))
```

### 23. Square Function
**Problem**: Function to calculate square of number.
```python
def square(num):
    return num ** 2

print(square(2))
print(square(3))
```

### 24. Built-in Documentation
**Problem**: Print documentation of built-in functions.
```python
print(abs.__doc__)
print(int.__doc__)
print(input.__doc__)
```

### 25. Class and Instance Parameters
**Problem**: Class with class parameter and instance parameter.
```python
class Person:
    name = "Person"
    
    def __init__(self, name=None):
        self.name = name

jeffrey = Person("Jeffrey")
print("%s name is %s" % (Person.name, jeffrey.name))
nico = Person()
nico.name = "Nico"
print("%s name is %s" % (Person.name, nico.name))
```

### 26. Sum Function
**Problem**: Sum of two numbers.
```python
def SumFunction(number1, number2):
    return number1 + number2

print(SumFunction(1, 2))
```

### 27. Integer to String
**Problem**: Convert integer to string.
```python
def printValue(n):
    print(str(n))

printValue(3)
```

### 28. String to Integer Sum
**Problem**: Convert strings to integers and sum.
```python
def printValue(s1, s2):
    print(int(s1) + int(s2))

printValue("3", "4")
```

### 29. String Concatenation
**Problem**: Concatenate two strings.
```python
def printValue(s1, s2):
    print(s1 + s2)

printValue("3", "4")
```

### 30. String Length Comparison
**Problem**: Print string with maximum length.
```python
def printValue(s1, s2):
    len1 = len(s1)
    len2 = len(s2)
    if len1 > len2:
        print(s1)
    elif len2 > len1:
        print(s2)
    else:
        print(s1)
        print(s2)

printValue("one", "three")
```

### 31. Even/Odd Check
**Problem**: Check if number is even or odd.
```python
def checkValue(n):
    if n % 2 == 0:
        print("It is an even number")
    else:
        print("It is an odd number")

checkValue(7)
```

### 32. Small Square Dictionary
**Problem**: Dictionary with keys 1-3 and squared values.
```python
def printDict():
    d = dict()
    d[1] = 1
    d[2] = 2 ** 2
    d[3] = 3 ** 2
    print(d)

printDict()
```

### 33. Square Dictionary 1-20
**Problem**: Dictionary with keys 1-20 and squared values.
```python
def printDict():
    d = dict()
    for i in range(1, 21):
        d[i] = i ** 2
    print(d)

printDict()
```

### 34. Print Dictionary Values
**Problem**: Print only values from dictionary.
```python
def printDict():
    d = dict()
    for i in range(1, 21):
        d[i] = i ** 2
    for v in d.values():
        print(v)

printDict()
```

### 35. Square List
**Problem**: List of squares from 1-20.
```python
def printList():
    li = list()
    for i in range(1, 21):
        li.append(i ** 2)
    print(li)

printList()
```

### 36. First 5 Squares
**Problem**: First 5 elements of square list.
```python
def printList():
    li = list()
    for i in range(1, 21):
        li.append(i ** 2)
    print(li[:5])

printList()
```

### 37. Last 5 Squares
**Problem**: Last 5 elements of square list.
```python
def printList():
    li = list()
    for i in range(1, 21):
        li.append(i ** 2)
    print(li[-5:])

printList()
```

### 38. All Except First 5
**Problem**: All elements except first 5.
```python
def printList():
    li = list()
    for i in range(1, 21):
        li.append(i ** 2)
    print(li[5:])

printList()
```

### 39. Square Tuple
**Problem**: Tuple of squares from 1-20.
```python
def printTuple():
    li = list()
    for i in range(1, 21):
        li.append(i ** 2)
    print(tuple(li))

printTuple()
```

### 40. Tuple Slicing
**Problem**: Split tuple into first and second half.
```python
tp = (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
tp1 = tp[:5]
tp2 = tp[5:]
print(tp1)
print(tp2)
```

### 41. Even Numbers from Tuple
**Problem**: Extract even numbers from tuple.
```python
tp = (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
li = list()
for i in tp:
    if i % 2 == 0:
        li.append(i)
tp2 = tuple(li)
print(tp2)
```

### 42. String Validation
**Problem**: Check if string is "yes" in any case.
```python
s = input()
if s.lower() == "yes":
    print("Yes")
else:
    print("No")
```

### 43. Filter Even Numbers
**Problem**: Filter even numbers using filter function.
```python
li = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
evenNumbers = list(filter(lambda x: x % 2 == 0, li))
print(evenNumbers)
```

### 44. Map Squares
**Problem**: Square elements using map function.
```python
li = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squaredNumbers = list(map(lambda x: x ** 2, li))
print(squaredNumbers)
```

### 45. Filter and Map Combined
**Problem**: Square of even numbers using filter and map.
```python
li = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
evenNumbers = list(map(lambda x: x ** 2, filter(lambda x: x % 2 == 0, li)))
print(evenNumbers)
```

### 46. Filter Even Numbers 1-20
**Problem**: Even numbers between 1-20 using filter.
```python
evenNumbers = list(filter(lambda x: x % 2 == 0, range(1, 21)))
print(evenNumbers)
```

### 47. Map Squares 1-20
**Problem**: Squares of numbers 1-20 using map.
```python
squaredNumbers = list(map(lambda x: x ** 2, range(1, 21)))
print(squaredNumbers)
```

### 48. Static Method
**Problem**: American class with static method.
```python
class American(object):
    @staticmethod
    def printNationality():
        print("America")

anAmerican = American()
anAmerican.printNationality()
American.printNationality()
```

### 49. Class Inheritance
**Problem**: American and NewYorker classes.
```python
class American(object):
    pass

class NewYorker(American):
    pass

anAmerican = American()
aNewYorker = NewYorker()
print(anAmerican)
print(aNewYorker)
```

### 50. Circle Class
**Problem**: Circle class with area calculation.
```python
class Circle(object):
    def __init__(self, r):
        self.radius = r
    
    def area(self):
        return self.radius ** 2 * 3.14

aCircle = Circle(2)
print(aCircle.area())
```

---

## Intermediate Exercises (51-100) 🔸

### 51. Rectangle Class
**Problem**: Rectangle class with area calculation.
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

### 52. Shape Inheritance
**Problem**: Shape and Square classes with method overriding.
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

### 53. Raise Exception
**Problem**: Raise RuntimeError exception.
```python
raise RuntimeError('something wrong')
```

### 54. Exception Handling
**Problem**: Try/except for division by zero.
```python
def throws():
    return 5 / 0

try:
    throws()
except ZeroDivisionError:
    print("division by zero!")
except Exception as err:
    print('Caught an exception')
finally:
    print('In finally block for cleanup')
```

### 55. Custom Exception
**Problem**: Custom exception class.
```python
class MyError(Exception):
    def __init__(self, msg):
        self.msg = msg

error = MyError("something wrong")
```

### 56. Extract Username from Email
**Problem**: Extract username from email address.
```python
import re
emailAddress = input()
pat2 = "(\w+)@((\w+\.)+(com))"
r2 = re.match(pat2, emailAddress)
print(r2.group(1))
```

### 57. Extract Company from Email
**Problem**: Extract company name from email.
```python
import re
emailAddress = input()
pat2 = "(\w+)@(\w+)\.(com)"
r2 = re.match(pat2, emailAddress)
print(r2.group(2))
```

### 58. Extract Digits from String
**Problem**: Find and print digits from string.
```python
import re
s = input()
print(re.findall("\d+", s))
```

### 59. Unicode String
**Problem**: Print unicode string.
```python
unicodeString = "hello world!"
print(unicodeString)
```

### 60. Series Sum
**Problem**: Compute 1/2 + 2/3 + ... + n/(n+1)
```python
n = int(input())
sum = 0.0
for i in range(1, n + 1):
    sum += float(float(i) / (i + 1))
print(sum)
```

### 61. Recursive Function
**Problem**: f(n) = f(n-1) + 100
```python
def f(n):
    if n == 0:
        return 0
    else:
        return f(n - 1) + 100

n = int(input())
print(f(n))
```

### 62. Fibonacci Recursive
**Problem**: Fibonacci sequence using recursion.
```python
def f(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return f(n - 1) + f(n - 2)

n = int(input())
print(f(n))
```

### 63. Fibonacci with List Comprehension
**Problem**: Fibonacci sequence with list comprehension.
```python
def f(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return f(n - 1) + f(n - 2)

n = int(input())
values = [str(f(x)) for x in range(0, n + 1)]
print(",".join(values))
```

### 64. Even Number Generator
**Problem**: Generator for even numbers.
```python
def EvenGenerator(n):
    i = 0
    while i <= n:
        if i % 2 == 0:
            yield i
        i += 1

n = int(input())
values = []
for i in EvenGenerator(n):
    values.append(str(i))
print(",".join(values))
```

### 65. Divisible by 5 and 7 Generator
**Problem**: Generator for numbers divisible by 5 and 7.
```python
def NumGenerator(n):
    for i in range(n + 1):
        if i % 5 == 0 and i % 7 == 0:
            yield i

n = int(input())
values = []
for i in NumGenerator(n):
    values.append(str(i))
print(",".join(values))
```

### 66. Assert Statements
**Problem**: Verify all numbers in list are even.
```python
li = [2, 4, 6, 8]
for i in li:
    assert i % 2 == 0
```

### 67. Expression Evaluation
**Problem**: Evaluate mathematical expressions.
```python
expression = input()
print(eval(expression))
```

### 68. Binary Search
**Problem**: Implement binary search algorithm.
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

### 69. Random Float 10-100
**Problem**: Generate random float between 10-100.
```python
import random
print(random.random() * 100)
```

### 70. Random Float 5-95
**Problem**: Generate random float between 5-95.
```python
import random
print(random.random() * 100 - 5)
```

### 71. Random Even Number
**Problem**: Random even number between 0-10.
```python
import random
print(random.choice([i for i in range(11) if i % 2 == 0]))
```

### 72. Random Divisible by 5 and 7
**Problem**: Random number divisible by 5 and 7.
```python
import random
print(random.choice([i for i in range(201) if i % 5 == 0 and i % 7 == 0]))
```

### 73. 5 Random Numbers
**Problem**: 5 random numbers between 100-200.
```python
import random
print(random.sample(range(100, 201), 5))
```

### 74. 5 Random Even Numbers
**Problem**: 5 random even numbers between 100-200.
```python
import random
print(random.sample([i for i in range(100, 201) if i % 2 == 0], 5))
```

### 75. Random Divisible Numbers
**Problem**: 5 random numbers divisible by 5 and 7.
```python
import random
print(random.sample([i for i in range(1, 1001) if i % 5 == 0 and i % 7 == 0], 5))
```

### 76. Random Integer
**Problem**: Random integer between 7-15.
```python
import random
print(random.randrange(7, 16))
```

### 77. String Compression
**Problem**: Compress and decompress string.
```python
import zlib
s = b'hello world!hello world!hello world!hello world!'
t = zlib.compress(s)
print(t)
print(zlib.decompress(t))
```

### 78. Execution Time
**Problem**: Measure execution time.
```python
from timeit import Timer
t = Timer("for i in range(100):1+1")
print(t.timeit())
```

### 79. List Shuffling
**Problem**: Shuffle list elements.
```python
from random import shuffle
li = [3, 6, 7, 8]
shuffle(li)
print(li)
```

### 80. Sentence Generation
**Problem**: Generate all subject-verb-object combinations.
```python
subjects = ["I", "You"]
verbs = ["Play", "Love"]
objects = ["Hockey", "Football"]
for i in range(len(subjects)):
    for j in range(len(verbs)):
        for k in range(len(objects)):
            sentence = "%s %s %s." % (subjects[i], verbs[j], objects[k])
            print(sentence)
```

### 81. Remove Even Numbers
**Problem**: Remove even numbers from list.
```python
li = [5, 6, 77, 45, 22, 12, 24]
li = [x for x in li if x % 2 != 0]
print(li)
```

### 82. Remove Divisible by 5 and 7
**Problem**: Remove numbers divisible by 5 and 7.
```python
li = [12, 24, 35, 70, 88, 120, 155]
li = [x for x in li if x % 5 != 0 and x % 7 != 0]
print(li)
```

### 83. Remove Specific Indexes
**Problem**: Remove 0th, 2nd, 4th, 6th elements.
```python
li = [12, 24, 35, 70, 88, 120, 155]
li = [x for (i, x) in enumerate(li) if i % 2 != 0]
print(li)
```

### 84. 3D Array
**Problem**: Create 3*5*8 3D array with zeros.
```python
array = [[[0 for col in range(8)] for col in range(5)] for row in range(3)]
print(array)
```

### 85. Remove Multiple Indexes
**Problem**: Remove 0th, 4th, 5th elements.
```python
li = [12, 24, 35, 70, 88, 120, 155]
li = [x for (i, x) in enumerate(li) if i not in (0, 4, 5)]
print(li)
```

### 86. Remove Specific Value
**Problem**: Remove all occurrences of 24.
```python
li = [12, 24, 35, 24, 88, 120, 155]
li = [x for x in li if x != 24]
print(li)
```

### 87. List Intersection
**Problem**: Intersection of two lists.
```python
set1 = set([1, 3, 6, 78, 35, 55])
set2 = set([12, 24, 35, 24, 88, 120, 155])
set1 &= set2
li = list(set1)
print(li)
```

### 88. Remove Duplicates Preserve Order
**Problem**: Remove duplicates while preserving order.
```python
def removeDuplicate(li):
    newli = []
    seen = set()
    for item in li:
        if item not in seen:
            seen.add(item)
            newli.append(item)
    return newli

li = [12, 24, 35, 24, 88, 120, 155, 88, 120, 155]
print(removeDuplicate(li))
```

### 89. Gender Classes
**Problem**: Person, Male, Female classes.
```python
class Person(object):
    def getGender(self):
        return "Unknown"

class Male(Person):
    def getGender(self):
        return "Male"

class Female(Person):
    def getGender(self):
        return "Female"

aMale = Male()
aFemale = Female()
print(aMale.getGender())
print(aFemale.getGender())
```

### 90. Character Frequency
**Problem**: Count frequency of each character.
```python
dic = {}
s = input()
for s in s:
    dic[s] = dic.get(s, 0) + 1
print('\n'.join(['%s,%s' % (k, v) for k, v in dic.items()]))
```

### 91. String Reversal
**Problem**: Reverse a string.
```python
s = input()
s = s[::-1]
print(s)
```

### 92. Even Index Characters
**Problem**: Print characters at even indexes.
```python
s = input()
s = s[::2]
print(s)
```

### 93. List Permutations
**Problem**: Generate all permutations of list.
```python
import itertools
print(list(itertools.permutations([1, 2, 3])))
```

### 94. Chinese Puzzle
**Problem**: Solve chickens and rabbits problem.
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

### 95. Sum of List
**Problem**: Find sum of all elements in list.
```python
def sum_list(lst):
    return sum(lst)

print(sum_list([1, 2, 3, 4, 5]))
```

### 96. Largest Number
**Problem**: Find largest number in list.
```python
def find_max(lst):
    return max(lst)

print(find_max([1, 2, 3, 4, 5]))
```

### 97. Smallest Number
**Problem**: Find smallest number in list.
```python
def find_min(lst):
    return min(lst)

print(find_min([1, 2, 3, 4, 5]))
```

### 98. Count Vowels
**Problem**: Count vowels in string.
```python
def count_vowels(s):
    vowels = 'aeiouAEIOU'
    count = 0
    for char in s:
        if char in vowels:
            count += 1
    return count

print(count_vowels("Hello World"))
```

### 99. Palindrome Check
**Problem**: Check if string is palindrome.
```python
def is_palindrome(s):
    return s == s[::-1]

print(is_palindrome("madam"))
```

### 100. Remove Punctuation
**Problem**: Remove punctuation from string.
```python
import string

def remove_punctuation(s):
    return s.translate(str.maketrans('', '', string.punctuation))

print(remove_punctuation("Hello, World!"))
```

---

## Mathematical Exercises (101-130) 🧮

### 101. Common Elements
**Problem**: Find common elements between two lists.
```python
def common_elements(list1, list2):
    return list(set(list1) & set(list2))

print(common_elements([1, 2, 3, 4], [3, 4, 5, 6]))
```

### 102. Merge Dictionaries
**Problem**: Merge two dictionaries.
```python
def merge_dicts(dict1, dict2):
    return {**dict1, **dict2}

print(merge_dicts({'a': 1}, {'b': 2}))
```

### 103. Key Existence
**Problem**: Check if key exists in dictionary.
```python
def key_exists(d, key):
    return key in d

print(key_exists({'a': 1}, 'a'))
```

### 104. Element Frequency
**Problem**: Count frequency of list elements.
```python
from collections import Counter

def frequency(lst):
    return dict(Counter(lst))

print(frequency([1, 1, 2, 3, 3, 3]))
```

### 105. Flatten Nested List
**Problem**: Flatten a nested list.
```python
def flatten(lst):
    result = []
    for item in lst:
        if isinstance(item, list):
            result.extend(flatten(item))
        else:
            result.append(item)
    return result

print(flatten([1, [2, 3], [4, [5, 6]]]))
```

### 106. Second Largest
**Problem**: Find second largest number in list.
```python
def second_largest(lst):
    return sorted(set(lst))[-2]

print(second_largest([1, 2, 3, 4, 5]))
```

### 107. Longest Word Length
**Problem**: Find length of longest word.
```python
def longest_word_length(s):
    return max(len(word) for word in s.split())

print(longest_word_length("The quick brown fox"))
```

### 108. Most Frequent Element
**Problem**: Find most frequent element in list.
```python
from collections import Counter

def most_frequent(lst):
    return Counter(lst).most_common(1)[0][0]

print(most_frequent([1, 1, 2, 3, 3, 3]))
```

### 109. Prime Numbers
**Problem**: Find all prime numbers up to n.
```python
def primes_up_to(n):
    sieve = [True] * (n + 1)
    for i in range(2, int(n ** 0.5) + 1):
        if sieve[i]:
            for j in range(i * i, n + 1, i):
                sieve[j] = False
    return [i for i in range(2, n + 1) if sieve[i]]

print(primes_up_to(20))
```

### 110. GCD Calculation
**Problem**: Calculate Greatest Common Divisor.
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

print(gcd(48, 18))
```

### 111. LCM Calculation
**Problem**: Calculate Least Common Multiple.
```python
def lcm(a, b):
    return abs(a * b) // gcd(a, b)

print(lcm(12, 18))
```

### 112. Perfect Square Check
**Problem**: Check if number is perfect square.
```python
def is_perfect_square(n):
    return int(n ** 0.5) ** 2 == n

print(is_perfect_square(16))
```

### 113. Factors
**Problem**: Find all factors of number.
```python
def factors(n):
    return [i for i in range(1, n + 1) if n % i == 0]

print(factors(12))
```

### 114. Digit Sum
**Problem**: Calculate sum of digits.
```python
def sum_digits(n):
    return sum(int(d) for d in str(n))

print(sum_digits(123))
```

### 115. Number Reversal
**Problem**: Reverse a number.
```python
def reverse_number(n):
    return int(str(n)[::-1])

print(reverse_number(123))
```

### 116. Armstrong Number
**Problem**: Check if number is Armstrong number.
```python
def is_armstrong(n):
    digits = [int(d) for d in str(n)]
    return sum(d ** 3 for d in digits) == n

print(is_armstrong(153))
```

### 117. Recursive Factorial
**Problem**: Factorial using recursion.
```python
def factorial(n):
    return 1 if n == 0 else n * factorial(n - 1)

print(factorial(5))
```

### 118. Fibonacci Series
**Problem**: Generate Fibonacci series.
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

### 119. Natural Number Sum
**Problem**: Sum of first n natural numbers.
```python
def sum_natural(n):
    return n * (n + 1) // 2

print(sum_natural(10))
```

### 120. Square Sum
**Problem**: Sum of squares of first n natural numbers.
```python
def sum_squares(n):
    return n * (n + 1) * (2 * n + 1) // 6

print(sum_squares(5))
```

### 121. Circle Area
**Problem**: Area of circle given radius.
```python
import math

def circle_area(r):
    return math.pi * r ** 2

print(circle_area(5))
```

### 122. Circle Circumference
**Problem**: Circumference of circle given radius.
```python
import math

def circle_circumference(r):
    return 2 * math.pi * r

print(circle_circumference(5))
```

### 123. Celsius to Fahrenheit
**Problem**: Convert Celsius to Fahrenheit.
```python
def celsius_to_fahrenheit(c):
    return (c * 9 / 5) + 32

print(celsius_to_fahrenheit(100))
```

### 124. Fahrenheit to Celsius
**Problem**: Convert Fahrenheit to Celsius.
```python
def fahrenheit_to_celsius(f):
    return (f - 32) * 5 / 9

print(fahrenheit_to_celsius(212))
```

### 125. Quadratic Roots
**Problem**: Find roots of quadratic equation.
```python
import math

def quadratic_roots(a, b, c):
    discriminant = b ** 2 - 4 * a * c
    if discriminant < 0:
        return "No real roots"
    root1 = (-b + math.sqrt(discriminant)) / (2 * a)
    root2 = (-b - math.sqrt(discriminant)) / (2 * a)
    return root1, root2

print(quadratic_roots(1, -3, 2))
```

### 126. 2D Distance
**Problem**: Distance between two points in 2D.
```python
import math

def distance(x1, y1, x2, y2):
    return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)

print(distance(0, 0, 3, 4))
```

### 127. 3D Distance
**Problem**: Distance between two points in 3D.
```python
import math

def distance_3d(x1, y1, z1, x2, y2, z2):
    return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2 + (z2 - z1) ** 2)

print(distance_3d(0, 0, 0, 1, 1, 1))
```

### 128. Midpoint
**Problem**: Midpoint between two points.
```python
def midpoint(x1, y1, x2, y2):
    return (x1 + x2) / 2, (y1 + y2) / 2

print(midpoint(0, 0, 4, 4))
```

### 129. Slope Calculation
**Problem**: Slope of line given two points.
```python
def slope(x1, y1, x2, y2):
    return (y2 - y1) / (x2 - x1)

print(slope(0, 0, 2, 4))
```

### 130. Triangle Area
**Problem**: Area of triangle given base and height.
```python
def triangle_area(base, height):
    return 0.5 * base * height

print(triangle_area(10, 5))
```

---

## Advanced Exercises (131-150) 🔷

### 131. Triangle Area (Heron's)
**Problem**: Area of triangle given three sides.
```python
import math

def triangle_area_heron(a, b, c):
    s = (a + b + c) / 2
    return math.sqrt(s * (s - a) * (s - b) * (s - c))

print(triangle_area_heron(3, 4, 5))
```

### 132. Rectangle Perimeter
**Problem**: Perimeter of rectangle.
```python
def rectangle_perimeter(length, width):
    return 2 * (length + width)

print(rectangle_perimeter(10, 5))
```

### 133. Rectangle Area
**Problem**: Area of rectangle.
```python
def rectangle_area(length, width):
    return length * width

print(rectangle_area(10, 5))
```

### 134. Cube Volume
**Problem**: Volume of cube.
```python
def cube_volume(side):
    return side ** 3

print(cube_volume(5))
```

### 135. Cube Surface Area
**Problem**: Surface area of cube.
```python
def cube_surface_area(side):
    return 6 * side ** 2

print(cube_surface_area(5))
```

### 136. Cylinder Volume
**Problem**: Volume of cylinder.
```python
import math

def cylinder_volume(radius, height):
    return math.pi * radius ** 2 * height

print(cylinder_volume(3, 5))
```

### 137. Cylinder Surface Area
**Problem**: Surface area of cylinder.
```python
import math

def cylinder_surface_area(radius, height):
    return 2 * math.pi * radius * (height + radius)

print(cylinder_surface_area(3, 5))
```

### 138. Sphere Volume
**Problem**: Volume of sphere.
```python
import math

def sphere_volume(radius):
    return (4 / 3) * math.pi * radius ** 3

print(sphere_volume(5))
```

### 139. Sphere Surface Area
**Problem**: Surface area of sphere.
```python
import math

def sphere_surface_area(radius):
    return 4 * math.pi * radius ** 2

print(sphere_surface_area(5))
```

### 140. Compound Interest
**Problem**: Calculate compound interest.
```python
def compound_interest(principal, rate, time, frequency):
    return principal * (1 + rate / frequency) ** (frequency * time)

print(compound_interest(1000, 0.05, 10, 1))
```

### 141. Simple Interest
**Problem**: Calculate simple interest.
```python
def simple_interest(principal, rate, time):
    return principal * rate * time

print(simple_interest(1000, 0.05, 10))
```

### 142. Decimal to Binary
**Problem**: Convert decimal to binary.
```python
def decimal_to_binary(n):
    return bin(n)[2:]

print(decimal_to_binary(10))
```

### 143. Binary to Decimal
**Problem**: Convert binary to decimal.
```python
def binary_to_decimal(b):
    return int(b, 2)

print(binary_to_decimal('1010'))
```

### 144. Decimal to Hexadecimal
**Problem**: Convert decimal to hexadecimal.
```python
def decimal_to_hex(n):
    return hex(n)[2:]

print(decimal_to_hex(255))
```

### 145. Hexadecimal to Decimal
**Problem**: Convert hexadecimal to decimal.
```python
def hex_to_decimal(h):
    return int(h, 16)

print(hex_to_decimal('ff'))
```

### 146. Decimal to Octal
**Problem**: Convert decimal to octal.
```python
def decimal_to_octal(n):
    return oct(n)[2:]

print(decimal_to_octal(64))
```

### 147. Octal to Decimal
**Problem**: Convert octal to decimal.
```python
def octal_to_decimal(o):
    return int(o, 8)

print(octal_to_decimal('100'))
```

### 148. Character to ASCII
**Problem**: Find ASCII value of character.
```python
def char_to_ascii(c):
    return ord(c)

print(char_to_ascii('A'))
```

### 149. ASCII to Character
**Problem**: Find character from ASCII value.
```python
def ascii_to_char(n):
    return chr(n)

print(ascii_to_char(65))
```

### 150. Random Password Generator
**Problem**: Generate random password.
```python
import random
import string

def generate_password(length):
    chars = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choice(chars) for _ in range(length))

print(generate_password(12))
```

---

## How to Use 📖

### For Beginners:
1. Start with exercises 1-50 to build fundamental Python skills
2. Practice each exercise by typing the code yourself
3. Modify the solutions to understand how they work

### For Intermediate Learners:
1. Focus on exercises 51-100 to strengthen problem-solving skills
2. Try to solve problems before looking at solutions
3. Experiment with different approaches

### For Advanced Practice:
1. Work on exercises 101-150 for algorithm development
2. Optimize the solutions for better performance
3. Create your own variations of the problems

---

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
