---
title: "Tuples"
permalink: /docs/python/tuples-python/
excerpt: "This post discuss about the tuples data structure in python"
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

A t`tuple` in Python is similar to python `list` that we have previously discussed. The difference between the two is that we cannot change the elements of a tuple once it is assigned whereas we can change the elements of a list.  Tuple is normally enclosed by `( )`.

##### creating a tuple in python

A tuple is created by placing all the items (elements) inside parentheses `()`, separated by commas. It can have any number of items and they may be of different data types.

```python
# empty tuple
my_tuple = ()

# tuple of strings
my_tuple = ("Apple","Orange","Banana")

# tuple of integers
my_tuple = (1,4,5)

# tuple of mixed data types
my_tuple = (2,"Coconut",4,7.68)
```

There can be nested tuples as well,

```python
# nested tuple containing tuples as well as lists
my_tuple = (2,["Coconut","Apple","Orange"],4,7.68,(1,2,2))
```

One thing to notice here is that,`my_tuple` is also an object in python of the `tuple` type. Tuple can be created without using `( )`, which is known as **tuple packing**.

##### how to access elements from a tuple

`tuple` objects in python can be accessed through indexing, similar to that of `list`.

```python
# creating a tuple of items
my_tuple = ("Apple","Orange","Jackfruit")

# printing the tuple elements starting from 0
print(my_tuple[1])
print(my_tuple[-2])
print(my_tuple[2])

# trying to access the 3rd index
try:
    print(my_tuple[-4])
except:
    print("An error occured")
```

```
OUTPUT :

Orange
Orange
Jackfruit
An error occured
```

##### how to access a range of elements in a tuple ?

We can access a range of items in a tuple by using the slicing operator colon `:`, similar to that of `list`.

```python
# tuple slicing in Python
my_tuple = ('e','d','u','a','l','g','o')

# elements 3rd to 5th
print(my_tuple[2:5])

# elements beginning to 3rd
print(my_tuple[:-4])
```

```
OUTPUT :

('u', 'a', 'l')
('e', 'd', 'u')
```

##### changing elements of a tuple

Unlike lists, tuples are immutable. This means that elements of a tuple cannot be changed once they have been assigned. But, if the element is itself a mutable data type like list, its nested items can be changed. This is one of the important difference between the `tuple` and the `list` data type.

```python
# declaring a tuple in python
my_tuple = (1,2,3,5,6)

# changing one item of the tuple
try:
    my_tuple[3] = 10
    print(my_tuple)
except:
    print("Error occured")
```

```
OUTPUT :

Error occured
```

##### adding/inserting elements to a tuple

Unlike lists, we can't add/insert elements to a tuple. Tuples are immutable in nature, hence there are no such methods in python which can enable addition of new elements to the tuple. But there are few techniques that can be used to add elements to the tuple. One of which is **tuple concatenation**.

##### concatenating in a tuple

The `+` operator can be used for the concatenation of tuples, similar to lists.

```python
# creating the tuples
tuple1 = (1,2,3,4)
tuple2 =  ("Apple","coconut")

# adding the tuples
tuple3 = tuple1 + tuple2

# printing the added tuples
print(tuple3)
```

```
OUTPUT :

(1, 2, 3, 4, 'Apple', 'coconut')
```

##### deleting elements from the tuple

As tuples are immutable in nature, deleting an element is not possible, unlike lists. But the entire deletion of the tuple is possible by using the `del` keyword.

```python
# creating the tuples
tuple1 = (1,2,3,4)

del tuple1

try:
    print(tuple1)
except:
    print("An error occured")
```

```
OUTPUT :

An error occured
```

#### Exercise your way out

1. Write a Python program to add an item in a tuple.

2. Write a Python program to find the repeated items of a tuple.

3. Write a Python program to check whether an element exists within a tuple.

4. Write a Python program to reverse a tuple.

5. Write a Python program to unzip a list of tuples into individual lists.

6. Write a Python program to convert a tuple of string values to a tuple of integer values.

   ```
   Original tuple values:
   (('333', '33'), ('1416', '55'))
   New tuple values:
   ((333, 33), (1416, 55))
   ```

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}