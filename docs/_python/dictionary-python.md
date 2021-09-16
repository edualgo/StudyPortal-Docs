---
title: "Dictionary"
permalink: /docs/python/dictionary-python/
excerpt: "This post discuss about the dictionary data structure in python"
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

Python dictionary is an unordered collection of items. Each item of a dictionary has a `key/value` pair. Whenever the key is known to us, dictionary can retrieve the value in an optimized way.

##### creating a python dictionary

Creating a dictionary is as simple as placing items inside curly braces `{}` separated by commas. An item has a `key` and a corresponding `value` that is expressed as a pair (**key: value**). While the values can be of any data type and can repeat, keys must be of immutable type and must be unique.

```python
# creating an empty dictionary
my_dict = {}

# creating a dictionary
my_dict = {1:"Apple",2:"Banana"}
print(my_dict)

# creating a dictionary of different data types
my_dict = {"first":"edualgo",1:"book",(1,2,3):"nothing"}
print(my_dict)
```

```
OUTPUT :

{1: 'Apple', 2: 'Banana'}
{'first': 'edualgo', 1: 'book', (1, 2, 3): 'nothing'}
```

##### accessing elements from the dictionary

While indexing is used with other data types to access values, a dictionary uses `keys`. Keys can be used either inside square brackets `[]` or with the `get()` method.

If we use the square brackets `[]`, `KeyError` is raised in case a key is not found in the dictionary. On the other hand, the `get()` method returns `None` if the key is not found.

```python
# creating a dictionary of different data types
my_dict = {"first":"edualgo",1:"book",(1,2,3):"nothing"}

# accessing through key
print(my_dict["first"])
print(my_dict[1])
print(my_dict[(1,2,3)])

# accessing through key by using get method
print(my_dict.get(1))
print(my_dict.get(3))

# trying to access a non-existing key 
try:
    print(my_dict[3])
except:
    print("An error occured")
```

```
OUTPUT :

edualgo
book
nothing
book
None
An error occured
```

##### changing and adding dictionary elements

Dictionaries are mutable. We can add new items or change the value of existing items using an assignment operator.

If the key is already present, then the existing value gets updated. In case the key is not present, a new (**key: value**) pair is added to the dictionary.

```python
# creating a dictionary of different data types
my_dict = {"first":"edualgo",1:"book",(1,2,3):"nothing"}

my_dict["first"] = "banana"
print(my_dict)

my_dict["second"] = "coconut"
print(my_dict)
```

```
OUTPUT :

{'first': 'banana', 1: 'book', (1, 2, 3): 'nothing'}
{'first': 'banana', 1: 'book', (1, 2, 3): 'nothing', 'second': 'coconut'}
```

##### removing elements from the dictionary 

We can remove a particular item in a dictionary by using the `pop()` method. This method removes an item with the provided `key` and returns the `value`.

```python
# creating a dictionary of different data types
my_dict = {"first":"edualgo",1:"book",(1,2,3):"nothing"}

my_dict.pop("first")
print(my_dict)
```

```
OUTPUT :

{1: 'book', (1, 2, 3): 'nothing'}
```

#### Dictionary Comprehension

Dictionary comprehension is an elegant and concise way to create a new dictionary.

Dictionary comprehension consists of an expression pair (**key: value**) followed by a `for` statement inside curly braces `{}`.

```python
# creating a dictionary
cubes = {i: i**3 for i in range(10)}

# printing the dictionary out 
print(cubes)
```

```
OUTPUT :

{0: 0, 1: 1, 2: 8, 3: 27, 4: 64, 5: 125, 6: 216, 7: 343, 8: 512, 9: 729}
```

It's just similar to that of **list comprehension**.

#### Exercise your way out

1. Write a Python script to sort (ascending and descending) a dictionary by value.

2. Write a Python script to concatenate following dictionaries to create a new one.

   ```
   Sample Dictionary :
   dic1={1:10, 2:20}
   dic2={3:30, 4:40}
   dic3={5:50,6:60}
   Expected Result : {1: 10, 2: 20, 3: 30, 4: 40, 5: 50, 6: 60}
   ```

3. Write a Python script to check whether a given key already exists in a dictionary. 

4. Write a Python program to iterate over dictionaries using for loops.

5. Write a Python script to print a dictionary where the keys are numbers between 1 and 15 (both included) and the values are square of keys.

   ```
   Sample Dictionary
   {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81, 10: 100, 11: 121, 12: 144, 13: 169, 14: 196, 15: 225}
   ```

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}