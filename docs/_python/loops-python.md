---
title: "Loops In Python"
permalink: /docs/python/loops-python/
excerpt: "This post discuss about loops"
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
Sometimes the programs are going to be repetitive in nature. For example, suppose there is a problem statement to print 1 to 10(1,2,3,.....,9,10) . By looking into the problem in a deeper way we can see, to print 10 numbers we need 10 print() functions, which is not a scalable and perfect way to write code. The repetition being printing the number, but there is a small change, the number to be printed increases by 1 with each print() statement.

This becomes a necessity to use something which allows repetition in python as well as takes care of the changes.

In python(and every other programming language), such technicality is called as **looping** and normally python has two primitive loop commands, **for** and **while** loop.

A loop statement allows us to execute a statement or group of statements multiple times. 

Let's check the syntax of both the while and for loop and use them to print from 1 to 10.

```python
# syntax - while loop

while expression:
    statement(s)
    

# syntax - for loop

for iterator_var in sequence:
    statements(s)
```

`iterator_var` is the variable used for **iteration/traversing**. Normally the for loop is used in traversing.

Let's print 1 to 10 using these loops,

```python
# declaring an iteration variable
iter_var = 1

# using the loop method
while(iter_var <= 10):
    
    # the statement which repeats
    print(iter_var,end=" ")
    
    # the change
    iter_var += 1
```

```python
# using the for loop method
for iter_var in range(1,11):
    print(iter_var,end=" ")
```

```
OUTPUT:

1 2 3 4 5 6 7 8 9 10 
1 2 3 4 5 6 7 8 9 10 
```

Breaking apart the loops,

- `iter_var = 1` this denotes the declaration of an iteration variable and initially it's set to be 1.
- `while()` is the loop and `iter_var <= 10` is the condition, here the condition is to print from 1 to 10 which ,means we have to traverse from 1 to 10 and print the value of each `iter_var`.
- `print(iter_var,end=" ")` is the statement which repeats itself with each iteration.
- `iter_var+=1` is the change that we have explained above, with each iteration the number is increased by 1.

Similarly in for loop, we have used something known as **range()** in python, which is also an in-built function and takes two parameters (a,b), where a is inclusive and b is exclusive, that simply means the traverse will take place from a to b-1.

### Nested Loops

Can we place one loop inside another ?

Let's check that with a piece of code,

```python 
for iter_var in range(0,2):
    for iter_ma in range(0,2):
        print(iter_var + iter_ma,end = " ")
    print()
```

```
OUTPUT:

0 1 
1 2
```

#### Understanding what happened

To understand nested loops always break the loops in the following way,

```python
for iter_var in range(0,2):
    <statement>
```

This is the outer-loop, when the outer loop executes, the `<statement>` part of the loop also executes. 

The `<statement>` execution can take place only when the inner loop executes, this means the execution of the entire outer-loop is directly dependent on the results obtained from the inner loops. One of the ways to solve a nested loop is to start executing from the inner loop. 

Here due to the inner loop the value of `iter_ma` changes from 0 to 1, with each execution of the outer loop. It means for every `iter_var` in the outer loop there exists two `iter_ma`, which is a better visualization of the problem here.

#### Loop control statements

Loop control statements change execution from its normal sequence. When execution leaves a scope, all automatic objects that were created in that scope are destroyed.

Python supports the following control statements. 

- **break statement**

  It terminates the current loop and resumes execution at the next statement. The **break** statement can be used in both *while* and *for* loops. If you are using nested loops, the break statement stops the execution of the innermost loop and start executing the next line of code after the block.

  For example,

  ```python
  for i in range(0,10):
      if(i==7):
          break
      else:
          print(i,end=" ")
  ```

  ```
  0 1 2 3 4 5 6 
  ```

- **continue statement**

  The **continue** statement rejects all the remaining statements in the current iteration of the loop and moves the control back to the top of the loop.

  The **continue** statement can be used in both *while* and *for* loops.

  ```python
  for i in range(0,10):
      if(i==7):
          continue
      else:
          print(i,end=" ")
  ```

  ```
  0 1 2 3 4 5 6 8 9 
  ```

- **pass statement**

  It is used when a statement is required syntactically but you do not want any command or code to execute.

  The **pass** statement is a *null* operation; nothing happens when it executes. The **pass** is also useful in places where your code will eventually go, but has not been written yet.

  ```python
  for i in range(0,10):
      if(i==7):
          pass
      else:
          print(i,end=" ")
  ```

  ```
  0 1 2 3 4 5 6 8 9 
  ```

#### Exercise your way out

**Q -** For each \\(i <= n\\), print \\(i^2\\), where \\(n\\) is the taken from user.

**Q -** Write a program to print the following matrix to the terminal,

```
0 1 2
1 2 3
2 3 4
```

**Q -** Write a program to print A to Z, five characters per line. 

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}









