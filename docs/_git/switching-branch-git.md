---
title: "Switching Branch in Git"
permalink: /docs/switching-branch-git/
excerpt: "This article discuss about switching branch in a git repository"
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

To switch to an existing branch, you run the git checkout command. Let’s switch to the new testing branch:

```bash
$ git checkout testing
```

This moves HEAD to point to the testing branch.

<img src="https://i.postimg.cc/DytHyH9D/Git-Slides-mod-3.jpg" size="80%">

What is the significance of that? Well, let’s do another commit:

```bash
$ vim test.rb
$ git commit -a -m 'made a change'
```

<img src="https://i.postimg.cc/L5gDc68s/Git-Slides-mod-4.jpg" size="80%">

This is interesting, because now your testing branch has moved forward, but your master branch still points to the commit you were on when you ran git checkout to switch branches. Let’s switch back to the master branch:

```bash
$ git checkout master
```

<img src="https://i.postimg.cc/nLd6ZrpK/Git-Slides-mod-5.jpg" size="80%">

That command did two things. It moved the HEAD pointer back to point to the master branch, and it reverted the files in your working directory back to the snapshot that master points to. This also means the changes you make from this point forward will diverge from an older version of the project. It essentially rewinds the work you’ve done in your testing branch so you can go in a
different direction.

>  It’s important to note that when you switch branches in Git, files in your working directory will change. If you switch to an older branch, your working directory will be reverted to look like it did the last time you committed on that branch. If Git cannot do it cleanly, it will not let you switch at all.

Let’s make a few changes and commit again:

```bash
$ vim test.rb
$ git commit -a -m 'made other changes'
```

You created and switched to a branch, did some work on it, and then switched back to your main branch and did other work. Both of those changes are isolated in separate branches: you can switch back and forth between the branches and merge them together when you’re ready. And you did all that with simple branch, checkout, and commit commands.

<img src="https://i.postimg.cc/sDpqxw3g/Git-Slides-mod-1.jpg" size="80%">


<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}