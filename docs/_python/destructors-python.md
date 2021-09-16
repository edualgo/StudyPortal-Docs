---
title: "Destructors"
permalink: /docs/python/destructor-python/
excerpt: "This post discusses about constructors in python"
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

Destructors are called when an object gets destroyed. In Python, destructors are not needed as much needed because Python has a garbage collector that handles memory management automatically.
The`__del__()` method is a known as a destructor method in Python. It is called when all references to the object have been deleted i.e when an object is garbage collected.

```python
def __del__(self):
  # body of destructor
```

Let's use the keyword **del** and delete our book objects manually.

```python
# defining the class
class Library:
    name = ""
    topic = ""
    author_name = ""
    ref_no = 0
    
    # defining a constructor
    def __init__(self,name,topic,author_name,ref_no):
        self.name = name
        self.topic = topic
        self.author_name = author_name
        self.ref_no = ref_no
    
    # defining the member function
    def print_details(self):
        print(f"Name : {self.name}")
        print(f"Topic : {self.topic}")
        print(f"Author : {self.author_name}")
        print(f"Ref. NO : {self.ref_no}",end="\n\n")
        
    def __del__(self):
        print(f"{self.ref_no} Destroyed")
    
# creating an object
book1 = Library("A beginner's guide to Python","Python","Abhijit Tripathy",1)
book2 = Library("Learning Python In a Practical Way","Python","Abhijit Tripathy",2)
book3 = Library("A beginner's guide to Machine Learning","Machine Learning","Abhijit Tripathy",3)

# printing the book details using the member function
book1.print_details()
del book1
book2.print_details()
del book2
book3.print_details()
del book3
```

```
OUTPUT:

Name : A beginner's guide to Python
Topic : Python
Author : Abhijit Tripathy
Ref. NO : 1

1 Destroyed
Name : Learning Python In a Practical Way
Topic : Python
Author : Abhijit Tripathy
Ref. NO : 2

2 Destroyed
Name : A beginner's guide to Machine Learning
Topic : Machine Learning
Author : Abhijit Tripathy
Ref. NO : 3

3 Destroyed
```

##### Exercise your way out

**Q -** Design a program for the `car` class, where the attributes being, name, model, color, price, mileage etc.

**Q -** Imagine there is a 5 floor building in your town and each floor has different company offices. Design a program to imitate the same 

**Q -** Design a program using OOP for some college mark list.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}
