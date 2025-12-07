---
layout: default
title: Home
---
# Welcome

Hi — I write about biology, coding, and research.  
Browse my [Articles](/blog/) or check my [Projects](/projects/).

Latest posts:
<ul>
  {% for post in site.posts limit:5 %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
