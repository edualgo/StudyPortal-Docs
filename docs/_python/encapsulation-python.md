---
title: "Encapsulation"
permalink: /docs/python/encapsulation-python/
excerpt: "This post discusses about encapsulation in python"
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

Till now, we have used the default **public** access modifier in our class, which enabled us to access any data member and member function from outside of the class. But in some cases we need to hide some data and restrict the access to some member functions.

Imagine a real life situation of an University, there are different departments namely Physics, Chemistry, Mathematics, Journalism, Literature etc. Suppose you are a student of the Mathematics department and you want to access the student's data from the Chemistry department for one of your statistical models. Now you have no ways to access the data from the chemistry department as it's restricted, or in technical terms, it's **encapsulated**. To access the data in such situation, you will need to contact someone from the Chemistry department administration and request them.

In a similar way, inside a software, there are few blocks of code whose access is **private** and they can't be modified by any method outside of the class. Using OOP in Python, we can restrict access to methods and variables. This prevents data from direct modification which is called **encapsulation**.

#### Private Access Modifier

The class members declared private should neither be accessed outside the class. There is no existence of **Private** instance variables that cannot be accessed except inside a class in python. However, to define a private member prefix the member name with double underscore “__”.

Have a look at the following code,

```python
# defining the class
class Library:
    
    # defining a constructor
    def __init__(self,name,topic,author_name,ref_no):
        self.name = name
        self.topic = topic
        self.author_name = author_name
        self.__ref_no = ref_no						# private attribute
    
    # defining the member function
    def print_details(self):
        print(f"Name : {self.name}")
        print(f"Topic : {self.topic}")
        print(f"Author : {self.author_name}")
        print(f"Ref. NO : {self.__ref_no}",end="\n\n")
        
    # defining a destructor 
    def __del__(self):
        print(f"{self.ref_no} Destroyed")
    
# creating an object
book1 = Library("A beginner's guide to Python","Python","Abhijit Tripathy",1)

# printing the book details using the member function
book1.print_details()

# trying to print the ref_no by directly accessing
print(book1.__ref_no)
```

```
OUTPUT:

Name : A beginner's guide to Python
Topic : Python
Author : Abhijit Tripathy
Ref. NO : 1

---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-46-8c10ac780031> in <module>
     26 
     27 # trying to print the ref_no by directly accessing
---> 28 print(book1.__ref_no)

AttributeError: 'Library' object has no attribute '__ref_no'
```

It generates an `AttributeError` when we tried to access the data member outside of the class, but the program output correctly when we have used the member function defined inside the class to print the book details. The member function of the `Library` class is defined inside the class, hence is able to access the private member ``__ref_no`.

#### Exercise your way out

**Q -** Design a program, where there is a class named `students` that holds the details of students like the name,roll_no,marks obtained etc and you have to print the percentage obtained by the student, providing the mark attribute and the function for converting marks to percentage are private. Create 5 student objects and test your design on each one of them. The program should contain proper constructor and destructor too.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}