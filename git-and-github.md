---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: "Git and Github"
---
In this class, we will be working with multiple git repositories, much the way you would in professional practice. These repositories will all share a common history (i.e. they are clones).  We'll give two of them special names: _upstream_ and _origin_.  In addition, you may have multiple _local_ clones as well - typically one for each machine you develop on.

* __upstream__ is the repository I have created with the framework of our project in it.  I will be adding additional projects and files to this repository throughout the semester, so you will need to pull from it often.
* __origin__ is your clone of the upstream repository that is hosted on GitHub.  You will create this repository by _forking_ the upstream repository, and your local repositories will be _cloned_ from this one.
* __local__ you will have at least one local repository where you update your code to meet the assignments' requirements.  It is possible you may have multiple local repos - for example, one on the lab computer, and one on your desktop at home.

### Workflows
We often talk of _workflows_ in how we work, a pattern of steps to accomplish a goal.  The following workflows are sequences of git commands you will probably use in this course, and probably in later courses and industry as well.
* [Forking the upstream repository]({{ site.baseurl }}{% link git-workflows/fork.md %}) to create your origin repository.
* [Cloning your origin repository]({{site.baseurl}}{% link git-workflows/clone.md %}) to create a local repository.
* [Pulling changes from the upstream repository]({{site.baseurl}}{% link git-workflows/pull-upstream.md %}) into a local repository.
* [Committing changes]({{site.baseurl}}{% link git-workflows/committing-changes.md %}) on a local repository.
* [Pushing changes on a local repository]({{site.baseurl}}{% link git-workflows/pushing-changes.md %}) to your origin repository.
* [Pulling changes from your origin repository]({{site.baseurl}}{% link git-workflows/pull-origin.md %}) to a local repository.
* [Resolving merge conflicts]({{site.baseurl}}{% link git-workflows/merge-conflicts.md %}) after a merge or pull.
* [Creating a release]({{site.baseurl}}{% link git-workflows/create-release.md %}) on your origin repository to turn as your assignment.
