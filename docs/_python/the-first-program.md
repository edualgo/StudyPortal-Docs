---
title: "Writing the computer first program in Python"
permalink: /docs/python/the-first-program/
excerpt: "This post discuss on how to write the first code in python"
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

After setting up the editor the next step is to learn how to use the editor and write the first program. So let's start.

### Write a program to print your name using python

##### Thinking Procedure

- As this is the first program, there should be a python executable file having a **.py** extension in which we have to write the piece of code. So the first step is to *Making a .py file*.
- The program asks us to print something, means we have to use a tool/technique which can be helpful in printing.

##### Moving further

The tool/technique which we are going to use for printing is known as **print()** function in python which is an inbuilt function.

Let's look into a piece of code,

```python
# program to print the name --> comment statement 

print("My name is eduAlgo")
```

As it can be clearly seen in the above piece of code, it contains mainly three components,

- A line starting with **#** which is an indicator that the line is a **comment** statement. A **comment** statement in programming is a statement which is not executed when the compiler finds a delimiter. In python the delimiter is **#**, also known as the **octothorpe**.

  Here it is `# program to print the name`

- A **print()** function which is a basic in-built function of python that helps in printing something that's passed into the **(....)** of the function. Technically this "something" is known as an object which we will be discussing in the later part of the book when we will study about OOP.

- Finally here comes something in the format of **"......."** , where we have passed a text saying `My name is eduAlgo`. In python this is known as a *string*.

  *Strings* are combination of characters that helps in using text type objects in programming. We will study an extensive topic on sting in our upcoming chapters.

Let's now run the program, but here comes another study drill. As we are using VS Code and we have to write a python program. 

Here are the steps,

1. Create a new folder named **Python_Programs**.
2. Open your VS Code from this folder.
3. Create a file inside the folder by VS Code using the file creation option, let's name the file as **print_name.py**.
4. Now inside the editor our work is to write the code and save it by **ctrl+s**.
5. Open up the terminal by using **ctrl+`**.
6. Navigate to the target folder of yours by using the command `cd <your_folder_name>` in the terminal window. For example - `cd Python_Programs`
7. Now execute the python program by using the command `python print_name.py` and you are done.

Congratulations on completing your first program !

##### Exercise your way out

**Q -** Create a folder named "My_Bio_Data" and create a file named "bio_data.py" inside it. Now your task is to print your bio data using **print()** function.

The bio data must contain the following,

- Your name
- Father's name 
- Mother's name
- Date of birth 
- College/School/Company Name

**Q -** Write an essay on "Your favorite food" using python and print it to the terminal.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}