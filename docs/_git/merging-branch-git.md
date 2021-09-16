---
title: "Merging Branch in Git"
permalink: /docs/merging-branch-git/
excerpt: "This article discuss about merging branch in a git repository"
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

Let’s create a new branch from the master branch and add one commit to it.

```bash
$ git checkout -b hotfix
Switched to a new branch 'hotfix'
$ vim index.html
$ git commit -a -m 'Fix broken email address'
[hotfix 1fb7853] Fix broken email address
1 file changed, 2 insertions(+)
```

<img src="https://i.postimg.cc/MHhwwT03/Git-Slides-mod-14.jpg" size="80%">

You can run your tests, make sure the hotfix is what you want, and finally merge the hotfix branch back into your master branch to deploy to production. You do this with the `git merge` command:

```bash
$ git checkout master
$ git merge hotfix
Updating f42c576..3a0874c
Fast-forward
    index.html | 2 ++
    1 file changed, 2 insertions(+)
```

You’ll notice the phrase “fast-forward” in that merge. Because the commit 6 pointed to by the branch hotfix you merged in was directly ahead of the commit 4 you’re on, Git simply moves the pointer forward. To phrase that another way, when you try to merge one commit with a commit that can be reached by following the first commit’s history, Git simplifies things by moving the pointer forward because there is no divergent work to merge together — this is called a “fastforward.”

Your change is now in the snapshot of the commit pointed to by the master branch, and you can deploy the fix.
<img src="https://i.postimg.cc/cJDZLZQW/Git-Slides-std-23.jpg" size="80%">

After your super-important fix is deployed, you’re ready to switch back to the work you were doing before you were interrupted. However, first you’ll delete the hotfix branch, because you no longer need it — the master branch points at the same place. You can delete it with the -d option to git branch:

```bash
$ git branch -d hotfix
Deleted branch hotfix (3a0874c)
```

Now you can switch back to your work-in-progress branch on testing and continue working on it.

```bash
$ git checkout testing
Switched to branch "testing"
$ vim index.html
$ git commit -a -m 'Finish the new footer'
    [iss53 ad82d7a] Finish the new footer 
    1 file changed, 1 insertion(+)
```

#### Merging The Testing Branch

It’s worth noting here that the work you did in your hotfix branch is not contained in the files in your testing branch. If you need to pull it in, you can merge your master branch into your testing branch by running git merge master, or you can wait to integrate those changes until you decide to pull the testing branch back into master later.

Suppose you’ve decided that yourtesting work is complete and ready to be merged into your master branch. In order to do that, you’ll merge your testing branch into master, much like you merged your hotfix branch earlier. All you have to do is check out the branch you wish to mergeinto and then run the git merge command:

```bash
$ git checkout master
Switched to branch 'master'
$ git merge testing
Merge made by the 'recursive' strategy.
index.html | 1 +
1 file changed, 1 insertion(+)
```

This looks a bit different than the hotfix merge you did earlier. In this case, your development history has diverged from some older point. Because the commit on the branch you’re on isn’t a direct ancestor of the branch you’re merging in, Git has to do some work. In this case, Git does a simple three-way merge, using the two snapshots pointed to by the branch tips and the common ancestor of the two.

Instead of just moving the branch pointer forward, Git creates a new snapshot that results from this three-way merge and automatically creates a new commit that points to it. This is referred to as a merge commit, and is special in that it has more than one parent.

<img src="https://i.postimg.cc/YS0Z8FWc/Git-Slides-status-32.jpg">

Now that your work is merged in, you have no further need for the testing branch. You can close the issue in your issue-tracking system, and delete the branch:

```bash
$ git branch -d testing
```

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}