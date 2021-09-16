---
title: "Version Control System"
permalink: /docs/git/version-control-system/
excerpt: "This post discuss about the version control system"
author_profile: false
sidebar:
  title: "Git"
  nav: git
toc: true
read_time : true
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

> Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. 

For example let’s assume that you are building an android application and at the initial level you have added only 4 features. The next version of your app(version 2) may contain more than 4 feature, let’s say 8 features and it became successful. Now in version 3,  let’s assume that you added 5 unique features which were never been added in your previous versions and they backfired. Now you have two choices, to implement a version 4 and code out the entire version 2 again or else you can restore back to version 2 by using some version control system.

Using a VCS also generally means that if you screw things up or lose files, you can easily recover. In addition, you get all this for very little overhead.

#### Simple Version Control Method

In order to understand version control properly, in the above example, you can actually copy the code content of version 1 to another directory, version 2 to another and version 3 to another. If you screw things up (which is ofcourse possible) then you can actually look up to those directories to copy the content and restore the version.

This manual method has a very serious problem.

It is easy to forget which directory you’re in and accidentally write to the wrong file or copy over files you don’t mean to.

To overcome these, let’s try to think about a possible solution. What about designing a *database* to keep all the versions and access them when required. This actually solves the above problem upto a large extent. No need to remember the directory and the version number. If you are screwed up, just look into the database and you are done.

That *database* is actually the basic building block of a version control system.

#### Local and Centralized Version Control System

Locally, a database can be set up to track the versions of a file. But this becomes limited to one user. Centralized version control system has a central database and many developers are connected to it at the same time as well as can change the file content. In the centralized version control system, every developer can actually keep a check on what others are changing. thus making the development process super managed. But it has a severe failure. If by any chance the central database is lost (due to memory corruption and other reasons) then the entire data on file versions are lost.

We need to keep copies of the database, in order to avoid such failure. Thus it gave birth to the modern version control systems like git, bitbucket, mercurial etc.

#### Distributed Version Control System

Clients don’t just check out the latest snapshot of the files; rather, they fully mirror the repository, including its full history. Thus, if any server dies, and these systems were collaborating via that server, any of the client repositories can be copied back up to the server to restore it. Every clone is really a full backup of all the data. 

Furthermore, many of these systems deal pretty well with having several remote repositories they
can work with, so you can collaborate with different groups of people in different ways
simultaneously within the same project. This allows you to set up several types of workflows that
aren’t possible in centralized systems, such as hierarchical models.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}