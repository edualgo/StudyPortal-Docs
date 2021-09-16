---
title: "Variables and Printing in Python"
permalink: /docs/python/variable-printing/
excerpt: "This section discuss on how to deal with variables and the printing operation"
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

A variable is nothing more than a name for something in python, which can be visualized as an empty bucket, where we can place any datatype.

For example,

```python
# assigning integer datatype
a = 10                            # a is the variable name
b = 20

# assigning float datatype
p = 6.787                         # p is the variable name
q = 9.867

# assigning boolean datatype
clause = False                    # clause is a variable name
harm = True

# assigning character datatype
front = 'c'                       # front is a variable name 
back = '\n'

# assigning string datatype
name = "eduAlgo"                  # name is a variable name 
work = "digital publication"
```

Not only the in-built data types like float,integer,Boolean Etc. are the only supported types, but also an user can define their own datatype which can be further assigned to a variable name. These type of used defined data types are known as **class** and instances of the class are known as **objects**. What makes python so strong, is the ability of Object Oriented Programming. Technically python is not an Object Oriented language, but it's a scripting language that supports Object Oriented Programming. We will learn about OOP in the upcoming chapters in great details.

Let's have some hands on programming problems, to learn simply.

#### Can we print out a variable at a certain position inside a string(or a text in python) ?

##### Thinking Procedure

- First of all we have to print, hence it's clear we are going to use **print()** function for the work.
- The question asks about some variables, definitely we have some variables defined earlier, now we have a simpler work, i.e. format the printout text in such a way that the variables appear in a certain position. But the question is how to format ?

##### Code it out

There can be numerous methods is python to achieve this task as python is quite flexible as well as it's growing at a large scale every year.

But, we are going to discuss three important methods, one of which is quite faster than the other two

1. **The % method**

   String objects have a built-in operation using the `%` operator, which you can use to format strings. This method can be used for both one variable and a multivariable conditions. For example,

   ```python
   # formatting string using %
   name = "eduAlgo"
   age = 21
   
   print("I am %s" % name)
   print("I am %s and I am %d years old" % (name,age))
   ```

   Here is the output,

   ```
   OUTPUT:
   
   I am eduAlgo
   I am eduAlgo and I am 21 years old
   ```

   As you can see %s and %d are the format specifiers for string and integer respectively. This method can be used with objects as well, see the code below,

   ```python
   # declaring a BioData class
   class BioData:
       def __init__(self,name,age):
           self.name = name
           self.age = age
     
   # declaring an instance of the BioData class
   person = BioData("eduAlgo",21)
   
   # printing using %s only
   print("My name is %s and I am %s years old" % (person.name,person.age))
   
   # printing using %s and %d
   print("My name is %s and I am %s years old" % (person.name,person.age))
   ```

   The output is,

   ```
   My name is eduAlgo and I am 21 years old
   My name is eduAlgo and I am 21 years old
   ```

   As you can see the format specifier thing doesn't matter in case of OOP.  Don't worry about the **class** and **object** thing at this point of time. It's just for an illustration and example purpose, we will discuss more about OOP in the upcoming chapters. Unfortunately, this kind of formatting isn’t great because it is verbose and leads to errors, like not displaying tuples or dictionaries correctly.

2. **The str.format() method**

   It's similar to the **%** format method with a few syntax changes, but the concept remains the same. We just have to plugin the proper value inside the empty curly braces, **{}** of our text by passing proper parameters in the **.format()** method.

   Have a look at the code,

   ```python
   # using .format() method to format our string
   name = "eduAlgo"
   age = 21
   
   print("I am {} and I am {} years old".format(name,age))
   print("I am {} years old".format(age))
   print("I am {}".format(name))
   ```

   ```
   OUTPUT:
   
   I am eduAlgo and I am 21 years old
   I am 21 years old
   I am eduAlgo
   ```

   It's quite simple but have the similar problem as that of % formatting. It leads to longer code writing and it requires the programmer to be cautious while passing the parameters to the format() function.

   But the aim of python is to make it easier, isn't it. Hence we have something better than the above two.

3. **The f-string method (faster and better)**

   According to the official python documentation,

   >  F-strings provide a way to embed expressions inside string literals, using a minimal syntax. It should be noted that an f-string is really an expression evaluated at run time, not a constant value. In Python source code, an f-string is a literal string, prefixed with `f`, which contains expressions inside braces. The expressions are replaced with their values.

   Let's code it out,

   ```python
   # using f-string for string formatting
   name = "eduAlgo"
   age = 21
   
   print(f"I am {name} and I am {age} years old")
   print(f"I am {name}")
   ```

   ```
   OUTPUT:
   
   I am eduAlgo and I am 21 years old
   I am eduAlgo
   ```

   It's quite effective and easier than the other two methods. For the rest of the book, we will be using the third method for our coding purpose.

#### Experiment your way out

##### Experiment No - 01

```python
# what will be the output ?

fruit1 = "Apple"
price1 = 20

fruit2 = "Banana"
price2 = 30

fruit3 = "Orange"
price3 = 40

# first program
print("I have %s, and the price is %d rupees a kilo" % (fruit1,price1))
print("I have %s, and the price is %d rupees a kilo" % (fruit2,price2))
print("I have %s, and the price is %d rupees a kilo" % (fruit3,price3))

# second program
class Fruits:
    def __init__(self,name,price):
        self.fruit = name
        self.price = price 
        
first_fruit = Fruits(fruit1,price1)
print("I have %s, and the price is %d rupees a kilo" %(first_fruit.fruit,first_fruit.price))

# Can you see some difference in both the programs ?
```

#### Exercise your way out

**Q -** Write your biodata in a text format as shown below, by using variables and string formatting,

> My name is <your_name> and I am <your_profession>. My father's name is <father's_name> and I am <you r_age> years old. My date of birth is <your_DOB>.

**Q** - Write a paragraph to summarize your previous semester marks, by using variables and string formatting,

> I am <your_name>
>
> My marks are as below,
>
> Math - <your_math_marks>
>
> Physics - <your_physics_marks>
>
> Social Studies - <your_socialstudy_marks>
>
> I have scored a total of <your_total_mark> which is an aggregate of <your_aggregate_percentage>

**Q -** Can you write a passage on your favorite food where each line is a new line and each line has some formatting ? Remember to use only one print() function [Have a look at the next section]

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}