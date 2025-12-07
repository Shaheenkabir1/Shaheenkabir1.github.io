---
layout: default
title: Journal
permalink: /journal/
---
# Daily Journal

{% for post in site.categories.journal %}
### {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})

{{ post.excerpt }}

---
{% endfor %}
