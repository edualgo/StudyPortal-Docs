---
title: "Escape Sequence in Python"
permalink: /docs/python/escape-sequence/
excerpt: "This section discuss on escape sequences and their usages"
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
<img src="https://i.postimg.cc/nVm8Qk3S/Capture-ldcmvif.png" alt="Escape Sequence Table" style="zoom:100%;" />

This \ (backslash) character encodes difficult-to-type characters into a string. There are various **”escape
sequences”** available for different characters you might want to use.

Let's try it out,

```python
# use of the '\n' aka the newline escape character
print("Ring the bell \nEnter the home")

# use of the '\t' aks the tab space escape character
print("We teach python \t we teach Machine Learning too")

# use of the '\b' aka the backspace escape characters
print("We promote opensource\b")
```

```
OUTPUT:

Ring the bell 
Enter the home
We teach python 	 we teach Machine Learning too
We promote opensourc
```

### Exercise your way out

**Q -** Write your biodata, with every line in a new line with the help of "\n".

**Q -** Make a table-like structure as shown below, using escape sequences and print() function.

```
Commodity name 		 Price(in Rs.)
Oil 			 	 40
Salt 			 	 10
Spices 			 	 100
Sugar 			 	 60
Vegetables 		 	 90
```


<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}