---
title: "Getting a Git repository"
permalink: /docs/git-repository/
excerpt: "This article discuss about getting a git repository"
author_profile: false
sidebar:
  title: "Git"
  nav: git
toc: true
toc_sticky: true
read_time: true
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

You typically obtain a Git repository in one of two ways:

- You can take a local directory that is currently not under version control, and turn it into a Git
  repository, or
- You can clone an existing Git repository from elsewhere.

In either case, you end up with a Git repository on your local machine, ready for work.

#### Initializing a Repository in an Existing Directory

If you have a project directory that is currently not under version control and you want to start controlling it with Git, you first need to go to that project’s directory. If you’ve never done this, it looks a little different depending on which system you’re running:

```bash
$ cd /home/user/my_project
```


and type:

```bash
$ git init
```


This creates a new subdirectory named .git that contains all of your necessary repository files — a Git repository skeleton.

#### Cloning an Existing Repository

If you want to get a copy of an existing Git repository — for example, a project you’d like to contribute to — the command you need is `git clone`. By using this command, Git receives a full copy of nearly all data that the server has. Every version of every file for the history of the project is pulled down by default when you run git clone. In fact, if your server disk gets corrupted, you can often use nearly any of the clones on any client to set the server back to the state it was in when it was cloned.

You clone a repository with `git clone <url>`. 

For example, if you want to clone the python library of edualgo, you can do so like this:

```bash
git clone https://github.com/edualgo/eduAlgo.git
```

That creates a directory named eduAlgo, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new eduAlgo directory that was just created, you’ll see the project files in there, ready to be worked on or used.

If you want to clone the repository into a directory named something other than eduAlgo, you can specify the new directory name as an additional argument:

```bash
git clone https://github.com/edualgo/eduAlgo.git <YOUR_DIR_NAME>
```

That command does the same thing as the previous one, but the target directory is called YOUR_DIR_NAME.

Git has a number of different transfer protocols you can use. The previous example uses the https:// protocol, but you may also see git:// or user@server:path/to/repo.git, which uses the SSH transfer protocol. Getting Git on a Server will introduce all of the available options the server can set up to access your Git repository and the pros and cons of each.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}