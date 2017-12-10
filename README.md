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

## Builtin Functions

```
abs
bool

dir
help

eval
exec

str / float / int
```

## Object Oriented Programming

```python
class Person:
    def __init__(self, firstname, lastname):
        self.firstname = firstname
        self.lastname = lastname
        
    def firstname(self):
        return self.firstname

p1 = Person("John", "Doe")
print(p1.firstname)
```
>>>
```
John
```

```python
class User(Person):
    def __init__(self, login):
        print("User Class")
        self.login = login
        
    def full_info(self):
        print(self.firstname + " " + self.lastname + " (" + self.login + ")")

u = User("John", "Doe", "jdoe")
print(u.firstname)
u.full_info()
```
