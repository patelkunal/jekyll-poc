---
layout: page
title: All Posts
permalink: /posts/
---

# All Blog Posts

{% if site.posts.size > 0 %}
  <div class="feed">
    {% for post in site.posts %}
      <section class="snippet snippet_{{ post.id | slugify: "ascii" }}">
        {% include snippet.html post=post %}
      </section>
    {% endfor %}
  </div>
{% else %}
  <p>No posts yet. Stay tuned!</p>
{% endif %}

---

[Back to Home]({{ site.baseurl }})
