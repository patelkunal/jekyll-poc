---
layout: default
title: Posts
permalink: /posts/
section: blog
---

---
layout: default
title: All Posts
permalink: /posts/
section: blog
---

<div class="page-content">
    <h1>All Posts</h1>
    <p>Browse through all our posts and updates from BAPS Bengaluru.</p>
</div>

<section class="posts-section">
    {% if site.posts.size > 0 %}
    <div class="posts-grid">
        {% for post in site.posts %}
        <article class="post-card">
            {% if post.image %}
            <div class="post-card-image">
                <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
            </div>
            {% else %}
            <div class="post-card-image">
                <img src="{{ '/assets/img/default-post.jpg' | relative_url }}" alt="{{ post.title }}">
            </div>
            {% endif %}
            
            <div class="post-card-content">
                <h3 class="post-card-title">
                    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
                </h3>
                
                <div class="post-card-meta">
                    {{ post.date | date: "%B %d, %Y" }}
                    {% if post.categories.size > 0 %} • {{ post.categories | first }}{% endif %}
                </div>
                
                <div class="post-card-excerpt">
                    {% if post.excerpt %}
                        {{ post.excerpt | strip_html | truncatewords: 30 }}
                    {% else %}
                        {{ post.content | strip_html | truncatewords: 30 }}
                    {% endif %}
                </div>
                
                <a href="{{ post.url | relative_url }}" class="post-card-link">Read More</a>
            </div>
        </article>
        {% endfor %}
    </div>
    
    {% else %}
    <div class="text-center">
        <p>No posts available yet. Check back soon for updates!</p>
    </div>
    {% endif %}
</section>
