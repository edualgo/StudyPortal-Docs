---
title: "Creating Branch in Git"
permalink: /docs/create-branch-git/
excerpt: "This article discuss about creating a new branch in a git repository"
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

What happens when you create a new branch? Well, doing so creates a new pointer for you to move around. Let’s say you want to create a new branch called testing. You do this with the `git branch` command:

```bash
$ git branch testing
```

This creates a new pointer to the same commit you’re currently on.
<img src="https://i.postimg.cc/Z52nwbyR/Git-Slides-2.jpg" size="80%">

How does Git know what branch you’re currently on? It keeps a special pointer called HEAD.In Git, this is a pointer to the local branch you’re currently on. In this case, you’re still on master. The git branch command only created a new branch — it didn’t switch to that.

<img src="https://i.postimg.cc/CKCW2762/Git-Slides-mod-2.jpg" size="80%">

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}