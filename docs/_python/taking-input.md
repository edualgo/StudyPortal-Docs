---
title: "Taking Input From The User"
permalink: /docs/python/taking-input-python/
excerpt: "This section discuss on how to take input from the user in python"
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

### Introduction

Is it even possible to take some input from the user in python ? Let's get introduced to the **input()** function.

Write this code in one of your python files and run it from the terminal,

```python
# age is a variable used to store the input from the user
age = input("What's your age\n")

# printing out the age in the terminal
print(f"Your age is {age}")
```

```
OUTPUT:

What's your age
20
Your age is 20
```

You might have witnessed that the cursor at the terminal stopped and waited for your input after printing the line "What's your age", this is because of the **input()** function which is an inbuilt function, that takes a string as parameter, which is nothing but the question you want to ask the user. If you don't want to ask the question but still want to take the input, your code might look like, `age = input()`, this will not ask any question as a string, but will take an input from the user and place it in the variable `age` which is an empty bucket to hold objects in python, as discussed earlier.

So, we are more powerful now with our bio-data exercise, we can do something like the following and make our code user specific. It's the best thing about python, you don't need to write a ton of code, neither there exists a heavy syntax.

```python
# taking your name as input from the terminal
name = input("What's your name ?\n")

# taking your father's name as input from the terminal
father_name = input("What's your father's name ?\n")

# taking your age input from the terminal
age = input("What's your age ?\n")

# taking your profession input from the terminal
profession = input("What do you do?\n")

# printing out the formatted text
print(f"Hello ! I am {name} and my father's name is {father_name}. I am {profession} and I am {age} years old.")
```

```
What's your name ?
Abhijit
What's your father's name ?
Sasank Sekhar
What's your age ?
21
What do you do?
an entrepreneur
Hello ! I am Abhijit and my father's name is Sasank Sekhar. I am an entrepreneur and I am 21 years old.
```

#### Exercise your way out

**Q-** Write a python program to take your friend's previous semester marks as input and print it to the terminal.

**Q-**  Write a program to take length and breadth of a rectangle as input and print the corresponding area and perimeter as output.

**Q -** Write a program that takes an integer n as input and prints the sum of all positive integers between 0 to n (both inclusive)

**Q -** Write a program that takes two integer m and n from the user and prints the maximum of them.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}