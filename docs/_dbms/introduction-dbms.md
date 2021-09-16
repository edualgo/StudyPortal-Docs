---
title: "The Data Hierarchy"
permalink: /docs/database-hierarchy/
excerpt: "This article discuss about the hierarchy of data in DBMS"
author_profile: false
sidebar:
  title: "DBMS"
  nav: dbms
toc: true
toc_sticky: true
read_time: true
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

#### What is Data

Data can be defined as a representation of facts, concepts, or instructions in a formalized manner, which should be suitable for communication, interpretation, or processing by human or electronic machine.

#### Hierarchy of Data

Data are the principal resources of an organization. Data stored in computer systems form a hierarchy extending from a single bit to a database, the major record-keeping entity of a firm. Each higher rung of this hierarchy is organized from the components below it.

Data are logically organized into:

1. Bits (characters)

2. Fields

3. Records

4. Files

5. Databases

***Bit*** (Character) - a bit is the smallest unit of data representation (value of a bit may be a 0 or 1). Eight bits make a byte which can represent a character or a special symbol in a character code.

***Field*** - a field consists of a grouping of characters. A data field represents an attribute (a characteristic or quality) of some entity (object, person, place, or event)(columns in your spreadsheet can represent a single field)

***Record*** - a record represents a collection of attributes that describe a real-world entity. A record consists of fields, with each field describing an attribute of the entity(rows in your spreadsheet can represent a single record)

***File*** - a group of related records. Files are frequently classified by the application for which they are primarily used (employee file). A ***primary key*** in a file is the field (or fields) whose value identifies a record among others in a data file.

***Database*** - is an integrated collection of logically related records or files. A database consolidates records previously stored in separate files into a common pool of data records that provides data for many applications. The data is managed by systems software called database management systems (DBMS). The data stored in a database is independent of the application programs using it and of the types of secondary storage devices on which it is stored.

### What is a Database Management System

A computer software that the storage, retrieval, and updating of data in a computer system, mainly addition of data, editing data items, deleting data items, sorting the data items etc.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}