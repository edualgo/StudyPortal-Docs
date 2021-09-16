---
title: "Import and Scopes"
permalink: /docs/python/importing-python/
excerpt: "This post discuss on about importing libraries and defining variable scopes in python"
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

When our program grows bigger, it is a good idea to break it into different modules.

A module is a file containing Python definitions and statements. Python modules have a filename and end with the extension `.py`. Definitions/methods inside a module can be imported to another module or the interactive interpreter in Python. We use the `import` keyword to do this.

For example, we can import the `math` module, which is in-built by typing the following line:

```python
import math
print(math.pi)
```

```
3.141592653589793
```

```python
import sys
print(sys.path)
```

```
['C:\\Users\\Abhijit Tripathy', 'C:\\Users\\Abhijit Tripathy\\AppData\\Roaming\\nltk_data', 'C:\\Users\\Abhijit Tripathy\\tic tac toe game', 'C:\\Users\\Abhijit Tripathy', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\python37.zip', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\DLLs', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\lib', 'C:\\Users\\Abhijit Tripathy\\Anaconda3', '', 'C:\\Users\\Abhijit Tripathy\\AppData\\Roaming\\Python\\Python37\\site-packages', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\lib\\site-packages', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\lib\\site-packages\\win32', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\lib\\site-packages\\win32\\lib', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\lib\\site-packages\\Pythonwin', 'C:\\Users\\Abhijit Tripathy\\Anaconda3\\lib\\site-packages\\IPython\\extensions', 'C:\\Users\\Abhijit Tripathy\\.ipython']
```

##### Python variable scope

A scope is the portion of a program from where a variable can be accessed directly without any prefix.

At any given moment, there are at least three nested scopes.

1. Scope of the current function which has local names
2. Scope of the module which has global names
3. Outermost scope which has built-in names

When a reference is made inside a function, the name is searched in the local namespace, then in the global namespace and finally in the built-in namespace. If there is a function inside another function, a new scope is nested inside the local scope.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}