---
title: "Inheritance"
permalink: /docs/python/inheritance-python/
excerpt: "This post discusses about inheritance in python"
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

Inheritance generally means transfer of characters from the parents to the children. Consider a situation where we have a `person` class which has data attributes like name,addresses,height,weight,gender etc. Now in the same program it's required to design another class named as `students` that has all the attributes of the `person` class like name,addresses,height,weight along with some more attributes specific to the `students` class like the college_name,branch,semester etc. In this case, we can see that the `students` class inherit all the properties of the person class and has some more data attributes present, which are not really necessary for the `person` class.

In such cases, the **inheritance** ability of python comes into play.

Inheritance is the capability of one class to derive or inherit the properties from another class. It provides **reusability** of a code. The same code needn't to be written again and again. Also, it allows us to add more features to a class without modifying it. It is **transitive** in nature, which means that if class B inherits from another class A, then all the subclasses of B would automatically inherit from class A.

Let's learn by coding it out,

```python
# the parent class
class person:
    def __init__(self,name,age,gender):
        self.name = name
        self.age = age
        self.gender = gender
        
    def print_details(self):
        print(f"Name : {self.name}")
        print(f"Age : {self.age}")
        print(f"Gender : {self.gender}")

# the child class      
class Student(person):
    def __init__(self,name,age,gender,college_name,semester):
        # When you add the __init__() function, the child class will no 
        # longer inherit the parent's __init__() function.
        
        # To keep the inheritance of the parent's __init__() function, 
        # add a call to the parent's __init__() function:
        person.__init__(self,name,age,gender)
        self.college_name = college_name
        self.semester = semester
    
    def print_student_details(self):
        # using the member function of the parent class
        person.print_details(self)
        print(f"College : {self.college_name}")
        print(f"Semester : {self.semester}")
        
# creating an object of the child class
student1 = Student("Abhijit",21,"Male","Central University,Bilaspur","3")

# printing the student details, using the function in the child class
student1.print_student_details()
```

```
OUTPUT:

Name : Abhijit
Age : 21
Gender : Male
College : GGV,Bilaspur
Semester : 3
```

As we can see we have a parent class of `person` and a child class of `student` , one important thing to notice is that, we are adding our own `__init__()` function in the child class, which is breaking it's inheritance from the base class, due to the reason that both the constructors are taking different number of parameters, it makes both the class as two different entity. Hence to link the parent class with the child class, we are calling `person.__init__()` .

#### Experiment your way out 

```python
# what will be the output ?

# the base class
class person:
    def __init__(self,name,age,gender):
        self.name = name
        self.age = age
        self.gender = gender
        
    def print_details(self):
        print(f"Name : {self.name}")
        print(f"Age : {self.age}")
        print(f"Gender : {self.gender}")

# the child class      
class Student(person):
    def __init__(self,name,age,gender,college_name,semester):
        super().__init__(name,age,gender)
        self.college_name = college_name
        self.semester = semester
    
    def print_student_details(self):
        person.print_details(self)
        print(f"College : {self.college_name}")
        print(f"Semester : {self.semester}")
        
# creating an object of the child class
student1 = Student("Abhijit",21,"Male","GGV,Bilaspur","3")

# printing the student details, using the function in the child class
student1.print_student_details()
```

### Types of Inheritance

Mainly there are five types of inheritance, that can be observed in a software design.

**Single Inheritance** 

When a child class inherits from one parent class it's called as Single Inheritance. The `person` and `Student` class that we have designed above are the example of Single Inheritance.

**Multiple Inheritance**

When a child class inherits from multiple parent classes, it is called multiple inheritance. 

```python
# the base classes
class first_base: 
    def __init__(self): 
        self.str1 = "First Base Class"
  
class second_base: 
    def __init__(self): 
        self.str2 = "Second Base Class"         
  
# multiple inheritance, derived from two base classes
class derived(first_base, second_base): 
    def __init__(self): 
        first_base.__init__(self) 
        second_base.__init__(self) 
```





<img src="https://static.javatpoint.com/tutorial/typescript/images/typescript-classes-types-of-inheritance.png" alt="TypeScript Inheritance - javatpoint" style="zoom:67%;" />







**Multilevel Inheritance**

When there is a child class as well as a grandchild class which is derived from the child class, we call it as multilevel inheritance.

```python
# the base class
class Base: 
    def __init__(self, a): 
        self.a = a
  
# inherited child class  
class Child(Base): 
    def __init__(self, a, b): 
        Base.__init__(self, a) 
        self.b = b 
  
# inherited grand child class
class GrandChild(Child): 
    def __init__(self, a, b, c): 
        Child.__init__(self, a, b) 
        self.c = c 
```

**Hierarchical inheritance** 

When more than one derived class are constructed from a single base class we call it as Hierarchical inheritance.

```python
# the base class
class Base: 
    def __init__(self, a): 
        self.a = a
  
# inherited child class  
class Child1(Base): 
    def __init__(self, a, b): 
        Base.__init__(self, a) 
        self.b = b 
  
# inherited child class
class Child2(Base): 
    def __init__(self, a, c): 
        Base.__init__(self, a) 
        self.c = c 
```

**Hybrid inheritance**:

If more than one form of inheritance is present then it's known as Hybrid inheritance.

```python
# the base class
class Base: 
    def __init__(self, a): 
        self.a = a
  
# inherited child class from the base class  
class Child1(Base): 
    def __init__(self, a, b): 
        Base.__init__(self, a) 
        self.b = b 

# inherited grand child class from the child class 
class GrandChild(Child1):
    def __init__(self,a,b,d):
        Child1.__init__(self,a,b)
        self.d = d
        
# ingerited child class from base class
class Child2(Base): 
    def __init__(self, a, c): 
        Base.__init__(self, a) 
        self.c = c 

# inherited from the grand child class of the base class       
class derived_grand(GrandChild):
    def __init__(self,a,b,c,e,f):
        GrandChild.__init__(self,a,b,c)
        self.e = e
        self.f = f
```


##### Exercise your way out

**Q -** Design a program to have a base class of `library`, having child classes of `book`,`magazine`,`news_paper` and grand child of `science_stream`,`business_stream` & `story`. Design some member functions to print their details. Remember to put the `ref_no` of the library books as private in all the inherited class.

**Q -** Design a program to have a base class of `company`, having child class of `developer_team`,`finance_team`,`sales_team` etc, with some person specific grandchildren like `employee`,`manager`,`project_lead` etc. Design some member functions to print their details and their work. `employee` has some child of `interns`,`trainee`,`part_time`,`full_time` too.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}