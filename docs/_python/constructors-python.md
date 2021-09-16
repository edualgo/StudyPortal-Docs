---
title: "Constructors"
permalink: /docs/python/constructor-python/
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

Till now we have performed all the basic operations related to classes and objects like declaring member functions, accessing data members and member functions etc.

But, one thing if you have noticed is that, our `Library` class is not flexible, i.e. it contains only the data member for one book that we have declared. How to make it possible for the classes to hold data members and member functions for different book objects ?

In python and other programming languages, such limitations are covered up by something called as **constructors**.

Constructors are generally used for instantiating an object. The task of constructors is to initialize(assign values) to the data members of the class when an object of class is created. In Python the `__init__()` method is called the constructor and is always called when an object is created.

```python
# syntax of the constructor
def __init__(self):
    # constructor body
```

Declaring constructor is just like declaring member functions in python, with one difference that the function name is fixed as `__init__()`. Let's write the `Library` class code again by passing some parameters to the constructor.

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
    
# creating an object
book1 = Library("A beginner's guide to Python","Python","Abhijit Tripathy",1)
book2 = Library("Learning Python In a Practical Way","Python","Abhijit Tripathy",2)
book3 = Library("A beginner's guide to Machine Learning","Machine Learning","Abhijit Tripathy",3)

# printing the book details using the member function
book1.print_details()
book2.print_details()
book3.print_details()
```

```
OUTPUT :

Name : A beginner's guide to Python
Topic : Python
Author : Abhijit Tripathy
Ref. NO : 1

Name : Learning Python In a Practical Way
Topic : Python
Author : Abhijit Tripathy
Ref. NO : 2

Name : A beginner's guide to Machine Learning
Topic : Machine Learning
Author : Abhijit Tripathy
Ref. NO : 3

```

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}