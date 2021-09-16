---
title: "Conditional Statements In Python"
permalink: /docs/python/conditional-statement-python/
excerpt: "This post discuss on conditional statements and it's control flow"
author_profile: false
sidebar:
  title: "Python"
  nav: python
toc: true
mathjax: true
read_time : true
toc_sticky: true
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

#### Introduction

Can we check for some conditions in python ? We have seen earlier that we have `<, > , <= , >=` as comparison operators. But the need of the time is not only to compare, but also to put some conditions and execute certain lines of code depending upon the output of the condition.

For example, consider the following,

You have to check if a given number **n** is an even number or an odd number. If n is even, you have to print, "n is an even number", else you have to print "n is an odd number".

It's clear from the above problem statement that the rest of our program execution depends on a simple check - "*n is divisible by 2 or not*"

These type of problems are handled swiftly by using the in-built conditional operators in python, **if**...........**else**.

##### Syntax

Let's have a look at the syntax,

```
if( <condition> ):
	<some code, when the condition is True>
	
else:
	<some code, when the condition is False>
```

The code goes as below,

```python
# program to check is an user input number n is even or odd

# taking input from the user

n = input("please enter a number")

# using conditional statements
if(n % 2 == 0):
    print(f"{n} is even\n")            # if (n%2 == 0) is True
else:
    print(f"{n} is odd\n")			   # if (n%2 == 0) is False
```

```
OUTPUT:

---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-6-d4d385c90321> in <module>
      6 
      7 # using conditional statements
----> 8 if(n % 2 == 0):
      9     print(f"{n} is even\n")            # if (n%2 == 0) is True
     10 else:

TypeError: not all arguments converted during string formatting
```

It gives an error !

The reason of giving an error is quite important for python and needs special attention. The **input()** function we have studied earlier takes input from the user and stores it as a **string** object, which means we have, `n="20"` instead of `n=20`. And the difference being the datatype. `"20"` is a string but `20` is an integer. We can't use modulus operator on `"20"` , hence the compiler gives an error at the conditional statement. This problem can be solved by introducing a **typecasting method** in python.

Have a look at the below code.

```python
# first-case
age1 = input("What's your age ? ")

# second-case
age2 = int(input("What's your age ? "))
```

In the first-case, the input() has prompted the user and the user entered some value **x**, here **age1** stores **x** as a string because the default return type of the input() function is string [Will discuss more about functions in few pages].  In the second-case we have applied something like **int()** as a cover to the **input()** function, this just converted the string *x* that we got from the user to an integer.  Hence age2 stores an integer.

This **int()** cover is also known as a technique called as typecasting.

Now writing the correct code for even & odd checking, we get,

```python
# program to check is an user input number n is even or odd

# taking input from the user
n = int(input("please enter a number"))

# using conditional statements
if(n % 2 == 0):
    print(f"{n} is even\n")            # if (n%2 == 0) is True
else:
    print(f"{n} is odd\n")			   # if (n%2 == 0) is False
```

```
please enter a number20
20 is even
```
##### if....elif...else
Now there me a simple question in your mind at this point of time, i.e. what to do when there are multiple conditions ? For example, suppose we have a question, check if n is divisible by only 2, only 3 or both by 2 & 3 ? In this case we have three cases to check, if n is divisible by 2 or n is divisible by 3 or n is divisible by both 2 & 3 ?

These types of problems can be solved by using **if**........**elif**......**else** statement in python.

Let's jump into code and have a look,

```python
# taking input from the user
n = int(input("Please enter a number\n"))

# using conditional statements
if(n % 2 == 0 and n % 3 == 0):
    print(f"{n} is divisible by both 2 & 3")
elif(n % 2 == 0 and n % 3 != 0):
	print(f"{n} is divisible by only 2")
elif(n % 3 == 0 and n % 2 != 0):
	print(f"{n} is divisible by only 3")
else:
    print("Condition fails")
```

```
Please enter a number
9
9 is divisible by only 3
```

As you can notice we have used something like **and** here, which is a **logical operator** and it returns true is both the conditional statements[(n % 2 == 0) & (n % 3 == 0)] are true. Also we have used **assignment operator** like ``==,!=`` etc. Let's study about these operators in the next section.


<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}


