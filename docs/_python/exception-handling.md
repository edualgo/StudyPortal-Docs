---
title: "Exception Handling"
permalink: /docs/python/exception-handling-python/
excerpt: "This post discusses about exception handling in python"
author_profile: false
sidebar:
  title: "Python"
  nav: python
toc: true
read_time : true
toc_sticky: true
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

Whenever there is an error in the program, python raises a `traceback` and generates an error statement. In python, it's quite easy to test a code using `try` keyword and generate an error statement using `except` keyword. When an error occurs, or exception as we call it, Python will normally stop and generate an error message.

These exceptions can be handled using the `try` statement:

```python
class Student:
    def __init__(self,maths,phy):
        self.maths = maths
        self.phy = phy
    
    def __str__(self):
        return f"The math marks is {self.maths}, and the physics marks is {self.phy}" 
        
monty = Student(75,80)
parker = Student(32,78)

# using exception handling
try:
    print(monty + parker)
except:
    print("An error occures")
```

```
OUPUT:

An error occures
```

It generates an error because of the `+` operator being used to add two user defined objects. Instead of getting a `traceback` our error has been handled by the `except` statement.

Even we can design `except` block of code for special kind of errors, like here the error generated is a `TypeError` as seen earlier.

```python
class Student:
    def __init__(self,maths,phy):
        self.maths = maths
        self.phy = phy
    
    def __str__(self):
        return f"The math marks is {self.maths}, and the physics marks is {self.phy}" 
        
monty = Student(75,80)
parker = Student(32,78)

try:
    print(monty + parker)
except TypeError:
    print("A TypeError occured")
except:
    print("An error occures")
```

```
OUTPUT:

A TypeError occured
```

##### else keyword in error handling 

We can use the `else` keyword to define a block of code to be executed if no errors were raised.

```python
class Student:
    def __init__(self,maths,phy):
        self.maths = maths
        self.phy = phy
    
    def __str__(self):
        return f"The math marks is {self.maths}, and the physics marks is {self.phy}" 
    
    def __add__(self,other):
        maths = self.maths + other.maths
        phy = self.phy + other.phy
        return Student(maths,phy)
        
monty = Student(75,80)
parker = Student(32,78)

# handling exceptions
try:
    print(monty + parker)
except:
    print("An error occures")
else:
    print("There are no errors")
```

```
OUTPUT :

The math marks is 107, and the physics marks is 158
There are no errors
```

##### finally keyword in exception handling

The `finally` block will be executed regardless if the try block raises an error or not.

```python
class Student:
    def __init__(self,maths,phy):
        self.maths = maths
        self.phy = phy
    
    def __str__(self):
        return f"The math marks is {self.maths}, and the physics marks is {self.phy}" 
        
monty = Student(75,80)
parker = Student(32,78)

# exception handling
try:
    print(monty + parker)
except:
    print("An error occures")
finally:
    print(monty)
    print(parker)
```

```
OUTPUT :

An error occures
The math marks is 75, and the physics marks is 80
The math marks is 32, and the physics marks is 78
```

##### raise an exception from any condition

You can choose to throw an exception if a condition occurs. To throw (or raise) an exception, use the `raise` keyword.

```python
x = 10

if x%3 != 0:
    raise Exception("Sorry not divisible by 3")
```

```
OUTPUT:

---------------------------------------------------------------------------
Exception                                 Traceback (most recent call last)
<ipython-input-18-e6bb540e6824> in <module>
      2 
      3 if x%3 != 0:
----> 4     raise Exception("Sorry not divisible by 3")

Exception: Sorry not divisible by 3
```

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}

