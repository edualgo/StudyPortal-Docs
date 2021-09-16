---
title: "File Handling in Python"
permalink: /docs/python/file-handling-python/
excerpt: "This post discuss about file creation and handling"
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

**open ()** function in python is used to open a file in read or write mode. open ( ) will returns a file object basically. We use two arguments, that accepts file name and the mode, as shown below,

<table>
    <tr>
    	<td>
        	<b>Mode Arguement</b>
        </td>
        <td>
        	<b>Work</b>
        </td>
    </tr>
    <tr>
    	<td>
        	"r"
        </td>
        <td>
        	for reading
        </td>
    </tr>
    <tr>
    	<td>
        	"w"
        </td>
        <td>
        	for writing
        </td>
    </tr>
    <tr>
    	<td>
        	"a"
        </td>
        <td>
        	for appending
        </td>
    </tr>
    <tr>
    	<td>
        	"r+"
        </td>
        <td>
        	for both read and write
        </td>
    </tr>
</table>


##### Syntax

```python3
open(filename, mode)
```

#### Creating a file in python

To create a file, we are going to use the **open()** function along with the **write** mode operation. Let's execute the following code to have a look at how things are taking place.

Inside your folder create a **.py** file and place the following code inside it,

```python 
# opening a file, if it doen't exist then creating the file
file = open('edualgo.txt', 'w') 

# writing a string to the "edualgo.txt" file
file.write("eduAlgo is an opensource organization and we promote learning")

# closing the opened file
file.close()
```

**.txt** is an extension for the text files. We are creating a text file named as "edualgo.txt", by using the "w" mode as that file did not exist before. You may observe that a file of the same name "edualgo.txt" has been appeared in the same folder, which has contained the same string that has been passed as a parameter to the **file.write()** function.

#### Reading a file in python

To read a file, we are going to use the **read()** function along with the **read** mode operation. In the same folder create a new **.py** extension file and place the following block of code inside it.

```python
# opening file in a read mode
file = open("edualgo.txt", "r")  

# reading file and storing the content as an object
element = file.read()

# printing the content
print (element) 
```

```
OUTPUT Terminal:

(base) PS D:\Book-Py\Python_Programs> python .\program1.py
eduAlgo is an opensource organization and we promote learning
```

As you can see the **file.read()** operation has output the same string that we have passed in the previous file creating block of code. This way we can read a file and store it as an **object** in some variable and print the variable. Everything can be treated as an object in python and that's what makes python so strong and comfortable.

#### Adding new content to the file

Adding some new content to the files are relatively easy, we just need to change the mode of the file to **"a"** which means appending some more content.

Let's have a look at the code,

```python 
# opening a file in the append mode
file = open('edualgo.txt','a')

# writing a newline to the file
file.write("\nWe are currently teaching python") 

# closing the openened file
file.close() 
```

The above block of code will add a new line, that has been passed as a string in the **file.write()** function.

#### Experiment your way out

##### Experiment No 1

```python
# what is the output ?
with open("edualgo.txt") as file:   
    data = file.read()
    print(data)
```

##### Experiment No 2

```python
with open("edualgo.txt", "w") as f:  
    f.write("Hello Learners !") 

with open("edualgo.txt",'r') as f:
    print(f.read())
```

#### Exercise your way out

**Q -** Write a program using file handling to list out the table of **n**, to a file named "table.txt", where n being given input by the user.

**Q -** Write a program to read length and breadth of a rectangle from a file named "rectangle.txt", and write back the area of the rectangle. The initial content of the file "rectangle.txt" is given below,

```
# content of "rectangle.txt"

21
45
```

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}



