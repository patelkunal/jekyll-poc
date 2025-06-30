---
layout: default
title: Posts
permalink: /posts/
section: blog
---

{% include navigation.html %}

# Blog Posts

{% if site.posts.size > 0 %}
  <ul>
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {% if post.excerpt %}
          <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No posts yet. Stay tuned!</p>
{% endif %}

---

[Back to Home]({{ site.baseurl }})
