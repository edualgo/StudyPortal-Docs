---
title: "Important String Methods"
permalink: /docs/python/strings-python/
excerpt: "This post discuss about a few important string methods in python"
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

A string is a sequence of characters. In Python, a string is a sequence of Unicode characters. Unicode was introduced to include every character in all languages and bring uniformity in encoding. Strings can be created by enclosing characters inside a single quote or double-quotes. Triple quotes are used to represent multiline strings and docstrings.

##### accessing characters from a string

Just like lists and tuples we can access characters of a string by indexing and range of characters by slicing.

```python
name = "Abhijit Tripathy"

# accessing single character
print(name[6])
```

```python
# accessing range of characters
print(name[2:6])

# trying to access something out of the index
try:
    print(name[25])
except:
    print("An error occured")
```

```
OUTPUT :

t
hiji
An error occured
```

##### changing or deleting string

Like tuples and unlike lists strings are immutable. This means that elements of a string cannot be changed once they have been assigned. Deleting a string can be carried out by using the ``del`` keyword similar to that of the tuple.

##### Methods in string

| Method Name  | Work of the method                                         |
| ------------ | ---------------------------------------------------------- |
| endswith()   | Check if the string ends with some special character       |
| capitalize() | Convert the first character to capital letter              |
| find()       | Returns the index of the first occurrence of the substring |
| index()      | Returns the index of the substring                         |
| join()       | Used for string concatenation                              |
| upper()      | Returns upper case string                                  |
| lower()      | Returns lower case string                                  |


<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}