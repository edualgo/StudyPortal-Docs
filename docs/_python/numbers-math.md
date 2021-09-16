---
title: "Numbers and Math in Python"
permalink: /docs/python/number-math-python/
excerpt: "This section discuss on how to deal with numbers and math in python"
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

### Numbers and Math
This exercise has lots of math symbols. Here are the names:

<table>
    <tr>
        <td>
            <b>The symbol</b>
        </td>
        <td>
            <b>The Name</b>
        </td>
        <td>
        	<b>The Work</b>
        </td>
    </tr>
    <tr>
        <td>
            +
        </td>
        <td>
            plus
        </td>
        <td>
        	Addition
        </td>
    </tr>
    <tr>
        <td>
            -
        </td>
        <td>
            minus
        </td>
        <td>
        	Subtraction
        </td>
    </tr>
    <tr>
        <td>
            *
        </td>
        <td>
            asterisk
        </td>
        <td>
        	Multiplication
        </td>
    </tr>
    <tr>
        <td>
            %
        </td>
        <td>
            percent
        </td>
        <td>
        	Division
        </td>
    </tr>
    <tr>
        <td>
            <
        </td>
        <td>
            less-than
        </td>
        <td>
        	compare
        </td>
    </tr>
    <tr>
        <td>
            >
        </td>
        <td>
            greater-than
        </td>
        <td>
        	compare
        </td>
    </tr>
    <tr>
        <td>
            <=
        </td>
        <td>
           less-than equal-to
        </td>
        <td>
        	compare
        </td>
    </tr>
    <tr>
        <td>
            >=
        </td>
        <td>
            greater-than equal-to
        </td>
        <td>
        	compare
        </td>
    </tr>
</table>


Let's write a piece of code and check the outputs,

```python
# normal maths
print("Apples", 3+4+2/3)   # fist-case
print("Banana", 10*6+2-3)  # second-case

# comparison
print(3 + 9 < 9 - 8)       # third-case

# modulus action
print(15 % 4)              # fourth-case
```

So, run the code now and try to understand the output

```
OUTPUT :

Apples 7.666666666666667
Banana 59
False
3
```

##### observations

- In the first case & second case, the print() function has one string and one mathematical expression separated by comma, where the mathematical expression is solved by the normal **BODMAS** rule.
- In the third case, we had a comparison and it returns Boolean datatype. Which means binary (0 & 1) . **True** is treated as  1 and **False** is treated as 0.
- In the fourth case we are dealing with the **%** operator which simply means modulus but not percent here. In simpler words a % b means, the reminder obtained when a is divided by b. For example here 15 is divided by 4 and the reminder obtained is 3.

#### Exercise your way out

**Q** - You are given a list of marks(out of 100) for a student. Your aim is to print the corresponding percentage of the student.

​     	Mathematics - 50

​		 Physics - 85

​		 Social Science - 60

​	Also print the total aggregate percentage.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}