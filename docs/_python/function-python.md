---
title: "Functions"
permalink: /docs/python/function-python/
excerpt: "This post discuss about functions in python"
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

#### Introduction
**Functions** is an important topic in every programming language as it gives the power of reusability to the programmer. Remember the "area" finding exercise above, each time you had to write a statement like `area = length*breadth`. As a programmer, it's quite frustrating to write the same logic every time.

But as programmers are smart, they have devised a way to get rid of this repetitive logic writing. They have come up with an idea to create a box, which has one (or many) input tunnels and one (or many) output tunnels. The only thing we have to do is to supply the parameters to the input channels and the output is ready every-time we need it. We just need to write the logic once.

For an illustration, let's consider the method of preparing curry.

We have to wash the vegetables, cut the vegetables, put them in a container having some water, mix the required spices, follow an entire cooking methodology of proper heat and proper stirring and finally after some 30-40 minutes of work the curry will be prepared. Now imagine you have to make the curry daily, it will take a 30-40 minutes of time daily to follow the procedure (or the logic you may say). That is quite repetitive.

But what if we have a **box**, where we just need to put the vegetables, spices and some water only & the rest will be taken care of by some system ? Cooking will be quite easier !

This **box** in programming, is known as **functions**. These are the basic pillars of software designing. Technically known as **black-boxes**, the programmer who is using a function, needs to know only about the input and the output but not the logic inside. The logic is written just once, may be by some other programmers.

In this segment of the book, we are going to discuss about both the logic writing as well as function designing. So let's get started.

#### Creating a function

A function is a block of code which only runs when it is called. We can pass data, known as parameters, into a function and the function returns data as a result.

In python, we define a function using a special keyword `def` .

```python
# the function syntax

def <function_name>(parameters):
    <logic>
```

For example, lets write an **area()** function which takes two parameters,**length** and **breadth**, it returns the area of the rectangle. The function naming and the parameter naming follows the same rule as that of variable naming.

```python
# function to return the rectangle area

def area(length,breadth):
    return length*breadth
```

Let's break the above block of code,

- `def` is the keyword for function, as explained earlier, whenever the compiler gets a `def` it understands that this is a function definition.
- `area` here is the function name and this name can be anything like `rectangle_area` or `area_of_rectangle` etc. The same naming convention as that of variable naming is used for function naming.
- `length` & `breadth` are the name of the parameters and these name can also be anything like `l` & `b` etc according to the variable naming convention. It matters on the arguments we are passing as length and breadth but not really on their values.
- `return` statement returns something from the function, which is some data in most of the cases.

So basically in one line, the **area()** function, takes two arguments as parameters namely **length** and **breadth** and returns the area as the function return data.

#### Calling a function

To call a function, we use the function name with the parenthesis and the required arguments are passed as parameters.

Foe example,

```python
# function to return the rectangle area
def area(length,breadth):
    return length*breadth

answer = area(10,3)
print(answer)
```

```
OUTPUT:

30
```

We have called the function as `area(10,3)` and stored the returned data in the variable `answer`. `10` and `3` are known as arguments passed to the length and breadth parameter of the function respectively. The order of argument matters here because you have to send the arguments in the order of the parameters in the function.  If the order is changes, the return data will also be changed.

#### Keyword Arguments 

Arguments can also be sent with the *key* = *value* syntax. This way the order of the arguments does not matter.

For example, have a look at the code below,

```python
def fruit_named(fruit1,fruit2,fruit3):
    print(f"{fruit2} is a good fruit")
    
fruit_named(fruit1 = "Apple", fruit2 = "Orange", fruit3 = "Grapes")
fruit_named(fruit2 = "Mango", fruit1 = "Coconut", fruit3 = "Jackfruit")
```

```
OUTPUT:

Orange is a good fruit
Mango is a good fruit
```

#### Arbitrary Arguments

If there is no certainty on how many arguments that will be passed into the function, we add a `*` before the parameter name in the function definition, like `*args`.

The function can receive as many arguments as you wish. The internal working mechanism of `*args` follows something named as *tuple* , which is an in-built python data structure.

```python
def my_function(*fruits):
  print(f"{fruits[1]} is a good fruit")

my_function("Apple", "Mango", "Coconut")

# in tuples, it starts from zero,
# fruits[0] = "Apple"
# fruits[1] = "Mango"
# fruits[2] = "Coconut"
```

```
OUTPUT:

Mango is a good fruit
```

#### Arbitrary Keyword Arguments

If there is no certainty on how many keyword arguments that will be passed into your function, add two asterisk: `**` before the parameter name in the function definition.

The function can now receive as many keyword argument as wished. The internal working mechanism of `**kwarg` follows something known as *dictionary* in python, which is an in-built python data structure.

```python
def fruit_function(**fruits):
    print(fruits["fruit2"] + " is a good fruit")

fruit_function(fruit1 = "Apples", fruit2 = "Mango", fruit3 = "Orange")
```

```
Mango is a good fruit
```

#### Default parameter passing

In case of a need, we can even pass a default parameter to a python function,when a function is passed as having no parameters in it, the default parameter will be used.

```python 
def name_function(name="eduAlgo"):
    print(f"{name} is an organization")
    
name_function("Google")
name_function("Netflix")
name_function()								# blank parameter
name_function("XYZ")
```

#### Exercise your way out

**Q -** Write a function to print \\(i^2\\) provided, \\(0< i <= 100\\) 

**Q -** Write a function, that takes \\(n\\) as an input from the user and prints out the table of \\(n\\) in another file, the file name being passed as a parameter to the function.

**Q -** Write a function, which can have as many parameters as the user wish i.e. \\(n_1,n_2,n_3......\\)  and returns their multiplication table one by one.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}