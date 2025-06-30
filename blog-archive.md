---
layout: default
title: Blog Archive
permalink: /blog/archive/
section: blog
---

{% include navigation.html %}

# Blog Archive

Here's a complete archive of all blog posts organized by date.

## Recent Posts

{% for post in site.posts limit:10 %}
- **{{ post.date | date: "%B %d, %Y" }}** - [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

## All Posts by Year

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in posts_by_year %}
### {{ year.name }}
{% for post in year.items %}
- {{ post.date | date: "%b %d" }} - [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}

---

[View All Posts]({{ site.baseurl }}/posts) | [Back to Home]({{ site.baseurl }})
