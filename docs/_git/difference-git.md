---
title: "Difference in Git"
permalink: /docs/git-difference/
excerpt: "This article discuss about finding the difference of status between files in a git repository"
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

Git diff is a command-line utility. When it is executed, it runs a diff function on Git data sources. These data sources can be files, branches, commits, and more. It is used to show changes between commits, commit, and working tree, etc. It compares the different versions of data sources. The version control system stands for working with a modified version of files. So, the diff command is a useful tool for working with Git.

Let's understand different scenarios where we can utilize the git diff command.

Let’s say you edit and stage the README file again and then edit the CONTRIBUTING.md file without staging it. If you run your git status command, you once again see something like this:

```bash
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
    Changes to be committed:
    	(use "git reset HEAD <file>..." to unstage)
    	
            modified: README
    
    Changes not staged for commit:
        (use "git add <file>..." to update what will be committed)
        (use "git checkout -- <file>..." to discard changes in working directory)
        	
    		modified: CONTRIBUTING.md
```

To see what you’ve changed but not yet staged, type git diff with no other arguments:

```bash
$ git diff
diff --git a/CONTRIBUTING.md b/CONTRIBUTING.md
index 8ebb991..643e24f 100644
--- a/CONTRIBUTING.md
+++ b/CONTRIBUTING.md
@@ -65,7 +65,8 @@ branch directly, things can get messy.
Please include a nice description of your changes when you submit your PR;
if we have to read the whole diff to figure out why you're contributing
in the first place, you're less likely to get feedback and have your change
-merged in.
+merged in. Also, split your changes into comprehensive chunks if your patch is
+longer than a dozen lines.
If you are starting to work on a particular area, feel free to submit a PR
that highlights your work in progress (and note in the PR title that it's
```

That command compares what is in your working directory with what is in your staging area. The result tells you the changes you’ve made that you haven’t yet staged.

If you want to see what you’ve staged that will go into your next commit, you can use `git diff --staged`. This command compares your staged changes to your last commit:

```bash
$ git diff --staged
diff --git a/README b/README
new file mode 100644
index 0000000..03902a1
--- /dev/null
+++ b/README
@@ -0,0 +1 @@
+My Project
```

It’s important to note that git diff by itself doesn’t show all changes made since your last commit — only changes that are still unstaged. If you’ve staged all of your changes, git diff will give you no output.

<i class="fas fa-lightbulb fa-2x"></i> **We are here to help** ! Be sure to check our website and don't hesitate to ask any questions on our community platform. We provide personal mentoring and teaching too, in order to upgrade your skills. Vist [www.edualgoacademy.com](https://www.edualgoacademy.com) to get started.
{: .notice--info}

<i class="fas fa-bug fa-2x"></i> **Spotted a bug ?** Great job, you found a bug. Please report it to us in our [mail](mailto:founder@edualgoacademy.com) and we'll fix it as soon as possible.
{: .notice--danger}