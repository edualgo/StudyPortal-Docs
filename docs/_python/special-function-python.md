---
title: "Python Special Functions"
permalink: /docs/python/special-functions-python/
excerpt: "This post discuss on how to write the first code in python"
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

Class functions that begin with double underscore `__` are called special functions in Python.

These functions are not the typical functions that we define for a class. The `__init__()` function we defined above is one of them. It gets called every time we create a new object of that class.

There are numerous other special functions in Python available in the official python documentations. Using special functions, we can make our class compatible with built-in functions. Let's have a look at some blocks of code to understand the need.

```python
# declaring a student class
class Student:
    def __init__(self,maths,phy):
        self.maths = maths
        self.phy = phy
        
# declaring two students
monty = Student(75,80)

# printing the object
print(monty)
```

```
OUTPUT:

<__main__.Student object at 0x000001F06623CA20>
```

As we can see when we tried to print out an object, it printed out the memory location that the object has been assigned in the computer memory. This is because the in-built print() function is not designed to print custom objects.

But as python is powerful, we can make the print() function compatible by using a `__str__()` method in our class that controls how the object gets printed.

```python
# defining a student class
class Student:
    def __init__(self,maths,phy):
        self.maths = maths
        self.phy = phy
    
    # the special method in python 
    def __str__(self):
        return f"The math marks is {self.maths}, and the physics marks is {self.phy}"
        
# declaring two students
monty = Student(75,80)

# printing the object
print(monty)
```

```
The math marks is 75, and the physics marks is 80
```

It printed correctly. There are numerous special functions in python available to be used from python documentation.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}