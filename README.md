# Quick-Notes-Python

Notes about Python

## Comments

```python
print "Hello"

# one line comment

print "World"

"""
multiple
lines
comment
"""
```

## Data Structures

### String


### List

```python
list_fruits = [ "Apples", "Bananas", "Oranges" ]
```

List slice:

```python
to_five = print to_five[::2]

print to_five[3:]
# prints ['D', 'E'] 

print to_five[:2]
# prints ['A', 'B']

print to_five[::2]
# print ['A', 'C', 'E']

print to_five[::-1]
# print ['E', 'D', 'C', 'B', 'A']
```

List comprehension:

```python
evens_to_ten = [i for i in range(11) if i % 2 == 0]

even_squares = [x * x for x in range(1, 11) if (x % 2) == 0]
```

### Tuples

```python
tuple_os = ( "Linux", "MacOS X", "Windows" )
```

## Conditional Statements

Operators:
```
< <= > >= == !=
```

```
and or
```

```python
if (length < 10):
    print("small")
elif (length >= 10 and length < 20):
    print("medium")
else:
    print("big")
```

## Loops

### 'For' Loops

```python
for fruit in list_fruits:
    print(fruit)
  
for os in tuple_os:
    print(os)
```

Nested 'For' Loops

```python
str_episode = "Episode %dx%02d"
for season in range(1, 4):
    for episode in range(1, 7):
        print(str_episode%(season, episode))
```
>>>
```
Episode 1x01
Episode 1x02
Episode 1x03
Episode 1x04
Episode 1x05
Episode 1x06
Episode 2x01
Episode 2x02
Episode 2x03
Episode 2x04
Episode 2x05
Episode 2x06
Episode 3x01
Episode 3x02
Episode 3x03
Episode 3x04
Episode 3x05
Episode 3x06
```
#### range

```python
for i in range(0, 11, 2):
    print(i)
```
>>>
```
0
2
4
6
8
10
```

### 'While' Loops

```python
count = 0
while count < 10:
    count = count + 1
    print("%02d"%count)
```
>>>
```
01
02
03
04
05
06
07
08
09
10
```

```python
count = 0
while count < 10:
    count = count + 1
    if (count < 5):
        continue
    print("%02d"%count)
```
>>>
```
05
06
07
08
09
10
```

```python
count = 0
while count < 10:
    count = count + 1
    if (count > 5):
        break
    print("%02d"%count)
```
>>>
```
01
02
03
04
05
```

## Try / Except

```python
try:
    if my_undefined_var > 3:
        print("something to say")
except:
    print("Something went wrong")
```
>>>
```
Something went wrong
```

## Functions

```python
def hello(name):
    print("Hello " + name)
  
hello("world")
```
>>>
```
Hello world
```

```python
def add(num1, num2):
    return (num1 + num2)

sum = add(10, 32)
print sum
```
>>>
```
42
```

Anonymous Functions: (lambda)
```python
my_list = range(16)
print filter(lambda x: x % 3 == 0, my_list)

squares = [x ** 2 for x in range(1, 11)]
print filter(lambda x: x >= 30 and x <= 70, squares)
# [36, 49, 64]
```

## Builtin Functions

```
abs
min
max

bool

dir
help

eval
exec

type
str / float / int
```

dir
```
import math # Imports the math module
everything = dir(math) # Sets everything to a list of things from math
print everything # Prints 'em all!
```

type
```
integer = 42
pi = 3.14
msg = 'hello'

print type(integer)
print type(pi)
print type(msg)
```

## Object Oriented Programming

```python
class Triangle(object):
  number_of_sides = 3
  def __init__(self, angle1, angle2, angle3):
    self.angle1 = angle1
    self.angle2 = angle2
    self.angle3 = angle3
    
  def check_angles(self):
    if self.angle1 + self.angle2 + self.angle3 == 180:
      return True
    else:
      return False
    
my_triangle = Triangle(90, 30, 60)
print my_triangle.number_of_sides
print my_triangle.check_angles()

class Equilateral(Triangle):
  angle = 60
  def __init__(self):
    self.angle1 = self.angle
    self.angle2 = self.angle
    self.angle3 = self.angle
```
