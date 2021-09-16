---
title: "Lists"
permalink: /docs/python/lists-python/
excerpt: "This post tells us about the list data structure in python"
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

Python, being versatile, provides us with many compound data types, one of which is **list**. As the name suggests, it's a combination of different objects enclosed inside a box. The box in python being `[ ]`, square brackets. List is used frequently in python, making python a great choice for modern developers.

##### creating a list in python

A list is created by placing all the items (elements) inside square brackets `[]`, separated by commas. It can have any number of items and they may be of different data types.

```python
# empty list
my_list = []

# list of strings
my_list = ["Apple","Orange","Banana"]

# list of integers
my_list = [1,4,5]

# list of mixed data types
my_list = [2,"Coconut",4,7.68]
```

The most important thing, a list in python can contain another list, i.e. nested list.

```python
# a nested list 
my_list = [4,["Apple","grapes"],[3.45,6.776556],"eduAlgo"]
```

One thing to notice here is that,`my_list` is also an object in python of the `list` type.

##### how to access elements from a list 

`list` objects in python can be accessed through indexing. Suppose we have `my_list` as given below,

```python
# creating a list of items
my_list = ["Apple","Orange","Jackfruit"]
```

As we can see, there are three elements in the `my_list` object. And the indexing starts from `0` . Run the below code to understand the indexing in a better way.

```python
# creating a list of items
my_list = ["Apple","Orange","Jackfruit"]

# printing the list elements starting from 0
print(my_list[0])
print(my_list[1])
print(my_list[2])

# trying to access the 3rd index
try:
    print(my_list[3])
except:
    print("An error occured")
```

```
OUTPUT :

Apple
Orange
Jackfruit
An error occured
```

As we have tried to access the 3rd index, the program generated an error as expected. So we get a conclusion, that if a list has $n$ elements, then the maximum index that can be used to access the element is $n-1$.

To check the length of any list we can use the following code by using the `len()` function ,

```python
print(len(my_list))
```

```
3
```

Python also allows negative indexing for its sequences. The index of -1 refers to the last item, -2 to the second last item and so on.

```python
# creating a list of items
my_list = ["Apple","Orange","Jackfruit"]

# printing the list elements starting from 0
print(my_list[-1])
print(my_list[-2])
print(my_list[-3])

# trying to access the 3rd index
try:
    print(my_list[-4])
except:
    print("An error occured")
```

```
OUTPUT :

Apple
Orange
Jackfruit
An error occured
```

##### how to access a range of elements in a list ?

We can access a range of items in a list by using the slicing operator `:`(colon). This method is also known as **slicing**.

```python
# List slicing in Python
my_list = ['e','d','u','a','l','g','o']

# elements 3rd to 5th
print(my_list[2:5])

# elements beginning to 3rd
print(my_list[:-4])
```

```
OUTPUT :

['u', 'a', 'l']
['e', 'd', 'u']
```

##### changing elements of a list

As the python lists are mutable, their content can be changed by using the assignment operator (`=`) .

```python
# declaring a list in python
my_list = [1,2,3,5,6]

# changing one item of the list
my_list[3] = 10
print(my_list)

# changing a list of items of the list
my_list[:3] = [23,24,25]
print(my_list)
```

```
OUTPUT :

[1, 2, 3, 10, 6]
[23, 24, 25, 10, 6]
```

##### adding elements to the list

To add one item to the list we can use the `append()` function that's applicable to the python lists. To add several items we can use `extend()` function for the list.

```python
# declaring a list in python
my_list = [1,2,3,5,6]

# adding one element to the python list
my_list.append(20)
print(my_list)

# extending the python list by adding three elements
my_list.extend([23,24,25])
print(my_list)
```

```
OUTPUT :

[1, 2, 3, 5, 6, 20]
[1, 2, 3, 5, 6, 20, 23, 24, 25]
```

##### concatenation in a list

We can use the `+` operator to combine two lists, which in term known as **list concatenation**.

```python
# creating the lists
list1 = [1,2,3,4]
list2 = [ "Apple","coconut"]

# adding the lists
list3 = list1 + list2

# printing the added list
print(list3)
```

```
OUTPUT :

[1, 2, 3, 4, 'Apple', 'coconut']
```

##### inserting element(s) in a list

Inserting into the list can be achieved by using the `insert()` function. `insert(position,element)`, it takes two arguments, first one being the position of the list where to insert the element. To insert multiple items use an empty slice of a list.

```python
my_list = [1,2,3,4,5]

# inserting a single element to the list
my_list.insert(2,10)
print(my_list)

# inserting a group of elements to the list
my_list[2:2] = [25,26,27]
print(my_list)
```

```
OUTPUT:

[1, 2, 10, 3, 4, 5]
[1, 2, 25, 26, 27, 10, 3, 4, 5]
```

##### deleting an element from the list

`del` keyword can be used both to delete an element from the list as well as delete the entire list.

```python
my_list = ["Apple","Orange","Coconut","Jackfruit","Banana"]

# deleting a single element from the list
del my_list[3]
print(my_list)

# deleting the entire list
del my_list

# trying to print the deleted list
try:
    print(my_list)
except:
    print("An error occured")
```

```
OUTPUT :

['Apple', 'Orange', 'Coconut', 'Banana']
An error occured
```

We can use the `remove` method to remove a given item or the `pop` method to remove item from a given position.

```python
my_list = ["Apple","Orange","Coconut","Jackfruit","Banana"]

# removing a given element from the list
my_list.remove("Apple")
print(my_list)

# poping an element from the given list from a certain postion
print(my_list.pop(1))
print(my_list)

# poping out the last element of the list
print(my_list.pop())
print(my_list)
```

```
OUTPUT :

['Orange', 'Coconut', 'Jackfruit', 'Banana']
Coconut
['Orange', 'Jackfruit', 'Banana']
Banana
['Orange', 'Jackfruit']
```

One thing to notice here, `pop()` with a null parameter, pops out the last element from the list. This property of python list helps in the **Stack** data-structure. [Discussing about data-structures like **Stack**, **Queue**, **Graph** etc are out of the scope of this book]

### List Methods in Python

| Method Name | Actions by the Method                              |
| ----------- | -------------------------------------------------- |
| append()    | Add an element to the end of the list              |
| extend()    | Add all element of the list to another list        |
| insert()    | Insert an item at the defined index                |
| remove()    | Removes an item at the defined index               |
| pop()       | Removes and returns an element at the given index  |
| clear()     | Removes all items from the list                    |
| index()     | Returns the index of the first matched item        |
| count()     | Returns the number of items in the passed argument |
| sort()      | Sort a list in an ascending order                  |
| reverse()   | Reverse the item order in the list                 |
| copy()      | Returns a shallow copy of the list                 |

#### List Comprehension

What if, there is a question to create a list of n integers where the list contains \\(i^2\\) for \\(1<= i <= n\\)

We can write something like,

```python
# creating an empty list
square_list = []

# taking input from the user
n = int(input())

# generating square of numbers and appending back to the list
for i in range(1,n+1):
    square_list.append(i ** 2)
 
# print the list
print(square_list)
```

```
OUTPUT :

7
[1, 4, 9, 16, 25, 36, 49]
```

List comprehension is a concise way to create a new list. A list comprehension consists of an expression followed by a **for statement** inside square brackets.

The above program can be achieved easily in very less lines of code,

```python
# taking input from the user
n = int(input())

# creating a list of square numbers using list comprehension
square_list = [i ** 2 for i in range(1,n+1)]

# printing the square list
print(square_list)
```

```
OUTPUT :

7
[1, 4, 9, 16, 25, 36, 49]
```

#### Using membership operators

We can test if an item exists in a list or not, using the keyword `in`. Also by using a `for` loop we can iterate through each item in a list.

```python
# creating a list
fruits = ["Apple","Orange","Coconut","Jackfruit"]

# using membership operator "in"
for fruit in fruits:
    print(f"{fruit} is a good fruit")
```

```
OUTPUT :

Apple is a good fruit
Orange is a good fruit
Coconut is a good fruit
Jackfruit is a good fruit
```

#### Exercise your way out 

**1.** Write a Python program to sum all the items in a list.

**2.** Write a Python program to multiplies all the items in a list.

**3.** Write a Python program to get the largest number from a list. 

**4.** Write a Python program to get the smallest number from a list. 

**5.** Write a Python program to count the number of strings where the string length is 2 or more and the first and last character are same from a given list of strings. 

```
Sample List : ['abc', 'xyz', 'aba', '1221']
Expected Result : 2
```

**6.** Write a Python program to remove duplicates from a list.

**7.** Write a Python program to check a list is empty or not.

**8.** Write a Python program to clone or copy a list

**9.** Write a Python program to find the list of words that are longer than n from a given list of words.

**10.** Write a Python function that takes two lists and returns True if they have at least one common member. 

**11.** Write a Python program to print a specified list after removing the 0th, 4th and 5th elements. 

```
Sample List : ['Red', 'Green', 'White', 'Black', 'Pink', 'Yellow']
Expected Output : ['Green', 'White', 'Black']
```

**12.** Write a Python program to print the numbers of a specified list after removing even numbers from it. 

**13.** Given the names and grades for each student in a class of \\(N\\) students, store them in a nested list and print the name(s) of any student(s) having the second lowest grade.

*Note:* If there are multiple students with the second lowest grade, order their names alphabetically and print each name on a new line.

*Example*

```
records = [["Abhijit",90],["Himanshu",98],["Amogh",97],["Himanshi",100],["Smriti",97]]
```

The ordered list of scores is [90,97,98,100], so the second lowest score is 97 . There are two students with that score: ["Amogh","Smriti"]. Ordered alphabetically, the names are printed as:

```
Amogh
Smriti
```

**14.** Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given scores. Store them in a list and find the score of the runner-up.

**15.** Create a list of 20 `student` class objects having `name` and `total_mark` as the data members and print the list in the sorted order of their marks, in a tabular format. 

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}