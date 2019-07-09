---
layout: default
title: Installing Git
parent: Getting Started
permalink: /getting-started/installing-git/
nav_order: 2
---
### Download Git from [here](https://git-scm.com)

All the default settings are fine to use.

### What is Git?

Git is a source control management system. To put in simple terms, it helps keep track of source code. Git is mainly used for working on projects with one or more people.

### Why use Git?

Git makes collaboration easier especially when using **remote** (online) repositories like Github. Every time someone works on a specific thing in a project they'll add all the changed files and **commit** (explain their changes and sign) them. Then they'll send their commits to the remote so that other people working on the project can get the changes.

### What's Github?

Github is where people host their repositories so other people can view/collaborate/download projects.

### Git basics:

When you're making changes to files after you're done you should be adding your changes to your repository. 
Which can be done by using this command:

{% highlight bash %}
git add [file/directory]
{% endhighlight %}

So let's say I edited the file readme.txt and it's in the project directory under the root (base) directory. I would type in this command.

{% highlight bash %}
git add readme.txt
{% endhighlight %}

What if it's in a directory like text-files that's under the root?

{% highlight bash %}
git add text-files/readme.txt
{% endhighlight %}

What if I changed a handful of files that all pertain to a specific task

{% highlight bash %}
git add .
{% endhighlight %}

What does "." mean? . is just a shortcut for the directory you're in. Let's say you're currently in the directory ```/Documents/Projects/Robotics/NewProject/``` then "." would be that path. (For reference ".." means the previous directory from the current so using the same directory from before ".." would be "/Documents/Projects/Robotics")

### Resources:

- [Github Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
