---
title: "OOP Introduction"
permalink: /docs/python/oop-introduction-python/
excerpt: "This post gives an introduction to the object oriented programming in python"
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

Till now, we have studied about the basic operations in python like printing, file handling, writing functions, performing some mathematics etc. Now it's the time to take a step forward and learn the core concepts of object oriented programming which is quite important for becoming a good software developer.

We have written some procedures and functions in our previous exercises that performed different operations with the data. This paradigm of programming is technically known as **Procedural programming**.

But, in object oriented programming, it's all about creating certain **objects** of some manually created, user defined building blocks known as **class**, that has both data members and member functions included. We will be discussing about the technical terms in detail, in the upcoming segments. To understand what OOP is, let's consider a real life example.

Consider we have a class of Cars under which Santro Xing, Alto and WaganR represents individual Objects. In this context each Car Object will have its own, Model,Year of Manufacture, Color, Top Speed, Engine Power etc.,which form Properties of the Car class and the associated actions i.e., object functions like Start, Move, Stop form the Methods of Car Class.

So,every programming or real life problem can be designed in such a way that can be solved using the OOP paradigm. Let's discuss each term one by one briefly to get the idea and the intuition behind.

##### Objects

Object is the basic unit of object-oriented programming, having their unique name. An object represents a particular instance of a class. There can be more than one instance of an object. Each instance of an object can hold its own relevant data.

An Object is a collection of data members and associated member functions also known as *methods*.

##### Class

Classes are data types based on which objects are created. Objects with similar properties and methods are grouped together to form a Class. Thus a Class represent a set of individual objects. Characteristics of an object are represented in a class as Properties. The actions that can be performed by objects becomes functions of the class and is referred to as *Methods*.

#### Creating classes and objects in Python

A class is like blueprint for an object, let's create one to check the syntax and the code.

```python
Syntax:

class ClassName:
    # Statement-1
    <Attributes>
    <member functions>
    # Statement-N
    
# syntax for creating an object
ObjectName = ClassName()
```

Let's break it to understand,

- Classes are created by keyword `class`.
- `ClassName` is the name of the class, that follows the same naming convention as that of variables.
- The variables that belongs to the class are known as attributes.
- Attributes can be publicly accessed by using the dot(.) operator.
- `ObjectName` is the name of the object that we want to create. This also follows the naming convention as that of variables.

We will be taking a sample real life problem of a Library, where there are different books on different shelfs. Each book has a name and topic associated with it. Every book has an author as well as a library ref. No mentioned.

Breaking the above mentioned context to fit OOP paradigm, we will get that *Library* is a class where the book is an *object*. Each object has different datatypes like - *name*, *topic*, *author's name* and *ref.No*.

Now, as the design is clear, let's write some code.

```python
# defining the class
class Library:
    name = "A beginner's guide to python programming"
    topic = "Python"
    author_name = "Abhijit Tripathy"
    ref_no = 1
    
# creating an object
book1 = Library()

print(f"In the library there is a book named {book1.name}, which is written by {book1.author_name} on the topic of {book1.topic}. It has a library reference number of {book1.ref_no}.")
```

```
OUTPUT:

In the library there is a book named A beginner's guide to python programming, which is written by Abhijit Tripathy on the topic of Python. It has a library reference number of 1.
```

Let's understand this block properly, take some more time to understand it as it's the most basic thing needed to solve a problem through any software.

- `Library` is the class name having four attributes namely *name*,*topic*,*author_name*,*ref_no*.
- When we created an object of the `Library` class namely `book1`, we have applied the class blueprint to the object which means the object has the same attributes now as that of the class which created it.  So as soon as the line `book1 = Library()` has been executed, one of the things that happened internally is that the object `book1` has been assigned the same attributes as that of the class `Library`. Along with that, another important thing has been taken place i.e. memory allocation. No memory is allocated when a class is created. Memory is allocated only when an object is created, i.e., when an instance of a class is created.
- The second point is quite evident from the *print()* function, which prints the attributes of `book1` by using f-string formatting.

#### How to declare methods/functions inside the class ?

In our `Library` class we can assign a method to each of our class instances that prints the details of the book, whenever called. To perform this, we just need to declare a function inside the class(just like the normal function declaration), along with a slightest change in the parameters passed.

We have to pass ``self`` as parameter along with other parameters while declaring it inside the class. 

```python
class ClassName:
    
    def function_name(self,*args):
        <logic>
```

Have a look at the code below,

```python
# defining the class
class Library:
    name = "A beginner's guide to python programming"
    topic = "Python"
    author_name = "Abhijit Tripathy"
    ref_no = 1
    
    # defining the member function
    def print_details(self):
        print(f"Name : {self.name}")
        print(f"Topic : {self.topic}")
        print(f"Author : {self.author_name}")
        print(f"Ref. NO : {self.ref_no}")
    
# creating an object
book1 = Library()

book1.print_details()
```

```
OUTPUT :

Name : A beginner's guide to python programming
Topic : Python
Author : Abhijit Tripathy
Ref. NO : 1
```

Let's get deeper to the `self` keyword and it's use.

- `self` is an extra first parameter in method definition. We do not give a value for this parameter, but when the function is called, python provides it for us.
- If we have a method which takes no arguments, then we still have to have one argument. [For example, the `print_details()`method in the above code].

Basically,when we call a method of this object as `ObjectName.MethodName(arg1, arg2)`, this is automatically converted into `ClassName.MethodName(ObjectName, arg1, arg2)` in python.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}
