---
layout: default
title: Archive
permalink: /archive/
---

<div class="page-content">
    <h1>Archive</h1>
    
    <p>Browse through our collection of past events, articles, and memorable moments from BAPS Bengaluru.</p>
    
    <h2>Posts by Year</h2>
    
    {% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
    
    {% for year in posts_by_year %}
    <h3>{{ year.name }}</h3>
    <div class="archive-posts">
        {% for post in year.items %}
        <div class="archive-post-item">
            <div class="archive-post-date">{{ post.date | date: "%B %d" }}</div>
            <div class="archive-post-content">
                <h4><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h4>
                {% if post.excerpt %}
                <p class="archive-post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
                {% endif %}
                {% if post.categories.size > 0 %}
                <div class="archive-post-categories">
                    {% for category in post.categories %}
                        <span class="tag">{{ category }}</span>
                    {% endfor %}
                </div>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>
    {% endfor %}
    
    {% if site.posts.size == 0 %}
    <div class="text-center">
        <p>No posts available yet. Check back soon for updates!</p>
    </div>
    {% endif %}
    
    <h2>Past Events</h2>
    
    <div class="events-list">
        <div class="event-item">
            <div class="event-date">June 15, 2025</div>
            <h3 class="event-title">Grand Opening Celebration</h3>
            <div class="event-description">
                The inaugural ceremony of BAPS Bengaluru center was celebrated with great enthusiasm. Hundreds of devotees participated in the blessing ceremony and cultural programs.
            </div>
        </div>
        
        <div class="event-item">
            <div class="event-date">May 20, 2025</div>
            <h3 class="event-title">Community Health Camp</h3>
            <div class="event-description">
                Free health checkups and medical consultations were provided to over 200 families from the local community, including eye checkups, diabetes screening, and general health assessments.
            </div>
        </div>
        
        <div class="event-item">
            <div class="event-date">April 25, 2025</div>
            <h3 class="event-title">Earth Day Environmental Drive</h3>
            <div class="event-description">
                Volunteers participated in tree plantation drives and awareness campaigns about environmental conservation, planting over 100 saplings in the local area.
            </div>
        </div>
        
        <div class="event-item">
            <div class="event-date">March 10, 2025</div>
            <h3 class="event-title">Holi Festival Celebration</h3>
            <div class="event-description">
                A vibrant celebration of the festival of colors with traditional songs, dances, and organic colors. Families enjoyed traditional sweets and participated in cultural activities.
            </div>
        </div>
    </div>
</div>

<style>
.archive-posts {
    margin-bottom: 2rem;
}

.archive-post-item {
    display: flex;
    background: white;
    border-radius: 8px;
    padding: 1rem;
    margin-bottom: 1rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    border-left: 4px solid #ff6b35;
}

.archive-post-date {
    min-width: 100px;
    color: #ff6b35;
    font-weight: bold;
    font-size: 0.9rem;
    margin-right: 1rem;
}

.archive-post-content {
    flex: 1;
}

.archive-post-content h4 {
    margin: 0 0 0.5rem 0;
    color: #2c3e50;
}

.archive-post-content h4 a {
    color: inherit;
    text-decoration: none;
}

.archive-post-content h4 a:hover {
    color: #ff6b35;
}

.archive-post-excerpt {
    color: #555;
    margin: 0.5rem 0;
    font-size: 0.95rem;
}

.archive-post-categories {
    margin-top: 0.5rem;
}

@media (max-width: 768px) {
    .archive-post-item {
        flex-direction: column;
    }
    
    .archive-post-date {
        margin-bottom: 0.5rem;
        margin-right: 0;
    }
}
</style>
