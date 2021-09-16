---
title: "Sets"
permalink: /docs/python/sets-python/
excerpt: "This post discuss about sets in python"
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

In mathematics a set is an unordered collection of items, where every set items are unique. Python supports a similar built-in data type known as `set` that can also be used to perform mathematical set operations like union, intersection, symmetric difference, etc.

##### creating a set in python 

A set is created by placing all the items (elements) inside curly braces `{}`, separated by comma, or by using the built-in `set()` function. Set can have different data types as it's elements except mutable elements like lists. Have a look at the below code to understand how to create a set and how an error occurs when we include any mutable element inside the set.

```python 
# creating an empty set
my_set = set()

# creating a non-empty set
my_set = {1,2,3,4,5}
print(my_set)

# creating a set having immutable data types
my_set = {2,"Hello",(90,45,67)}
print(my_set)

# trying to create a set having mutable data types
try:
    my_set = {3,4,"Torso",[1,2,3]}
except:
    print("An error occured")
```

```
OUTPUT :

{1, 2, 3, 4, 5}
{(90, 45, 67), 2, 'Hello'}
An error occured
```

One thing to notice, the set is unordered data type. Like in the second line of the output, we can see it's been printed in a different order than the assigned order.

##### changing elements of set

As we have seen above sets are unordered, hence the indexing has no meaning. We cannot access or change an element of a set using indexing or slicing. Set data type does not support it. Though sets are mutable, the slicing method doesn't work.

##### adding elements to the set

We can add a single element using the `add()` method, and multiple elements using the `update()` method.

```python
my_set = {1,2,3,4,5}

# adding a new element
my_set.add(56)
print(my_set)

# adding an element that already exists inside the set
my_set.add(3)
print(my_set)

# adding a tuple of elements
my_set.update((4,90,34))
print(my_set)

# adding both tuple and list elements
my_set.update([13,44],(23,45))
print(my_set)

# in all the cases above the duplicates are avoided
```

```
OUTPUT :

{1, 2, 3, 4, 5, 56}
{1, 2, 3, 4, 5, 56}
{1, 2, 3, 4, 5, 34, 56, 90}
{1, 2, 3, 4, 5, 34, 44, 13, 45, 23, 56, 90}
```

##### removing elements from a set

A particular item can be removed from a set using the methods `discard()` and `remove()`.

The only difference between the two is that the `discard()` function leaves a set unchanged if the element is not present in the set. On the other hand, the `remove()` function will raise an error in such a condition (if element is not present in the set).

```python
# declaring a set
my_set = {1,2,3,4,5}

# removing an existing element 
my_set.remove(3)
print(my_set)

# discarding an existing element
my_set.discard(2)
print(my_set)

# discarding a non-existing element
my_set.discard(10)
print(my_set)

# removing a non-existing element
try:
    my_set.remove(10)
except:
    print("An error occured")
```

```
OUTPUT :

{1, 2, 4, 5}
{1, 4, 5}
{1, 4, 5}
An error occured
```

##### python set operations

Sets can be used to carry out mathematical set operations like union, intersection, difference and symmetric difference. 

###### Set Union

<img src="https://i.postimg.cc/bwb4wRNQ/union.jpg" alt="union" style="zoom:80%;" />

Union of A and B is a set of all elements from both sets. Union is performed using `|` operator. Same can be accomplished using the `union()` method.

```python
A = {1, 2, 3, 4, 5}
B = {4, 5, 6, 7, 8}

# using | operator
print(A | B)
```

```
{1, 2, 3, 4, 5, 6, 7, 8}
```

###### Set Intersection

<img src="https://i.postimg.cc/15bLSdPm/intersection.jpg" alt="intersection" style="zoom:80%;" />

Intersection of A and B is a set of elements that are common in both the sets. Intersection is performed using `&` operator. Same can be accomplished using the `intersection()` method.

```python
A = {1, 2, 3, 4, 5}
B = {4, 5, 6, 7, 8}

# using & operator
print(A & B)
```

```
{4, 5}
```

###### Set Difference

<img src="https://i.postimg.cc/hPXHHBkZ/difference.jpg" alt="difference" style="zoom:80%;" />

Difference of the set B from set A(A - B) is a set of elements that are only in A but not in B. Similarly, B - A is a set of elements in B but not in A. Difference is performed using `-` operator. Same can be accomplished using the `difference()` method.

```python
A = {1, 2, 3, 4, 5}
B = {4, 5, 6, 7, 8}

# using - operator on A
print(A - B)
```

```
{1, 2, 3}
```

###### Set Symmetric Difference

<img src="https://i.postimg.cc/Bv0kL1XR/symmetric.jpg" alt="symmetric" style="zoom:80%;" />

Symmetric Difference of A and B is a set of elements in A and B but not in both (excluding the intersection). Symmetric difference is performed using `^` operator. Same can be accomplished using the method `symmetric_difference()`.

```python
A = {1, 2, 3, 4, 5}
B = {4, 5, 6, 7, 8}

# using ^ operator
print(A ^ B)
```

```
{1, 2, 3, 6, 7, 8}
```

##### built-in methods in set 

| Method   | Description                                                  |
| -------- | ------------------------------------------------------------ |
| sum()    | returns the sum of all elements in the set                   |
| sorted() | returns a sorted list of the elements in the set (doesn't change the set) |
| min()    | returns the smallest item of the set                         |
| max()    | returns the largest item of the set                          |
| len()    | returns the length of the set or the number of elements in the set |

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}