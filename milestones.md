---
title: "Project Milestones"
layout: page
---
The projects for this semester are all centered around the creation of software to support a dino-themed fast-food chain, _DinoDiner_.  We will be developing this program iteratively, and each week we will have a new set of features to add and turn in as a _milestone_.  These milestones are:

{% for milestone in site.milestones %}
[{{milestone.title}}]({{site.baseurl}}{{ milestone.url }})
{% endfor %}
