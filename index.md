---
layout: default
title: Welcome to BAPS Bengaluru
---

<div class="homepage-layout">
    <!-- Main Content Area -->
    <div class="main-content-area">
        <div class="page-content">
            <div class="text-center mb-2">
                <h1>Welcome to BAPS Bengaluru</h1>
                <p style="font-size: 1.2rem; color: #555;">Spiritual growth, community service, and cultural enrichment</p>
            </div>
            
            <div style="text-align: center; margin: 2rem 0;">
                <p>Welcome to the Bochasanwasi Akshar Purushottam Swaminarayan Sanstha (BAPS) Bengaluru center. We are a spiritual and charitable organization dedicated to serving the community through various religious, cultural, and humanitarian activities.</p>
            </div>
        </div>

        <!-- Recent Posts Section - Vertical Layout -->
        <section class="recent-posts-vertical">
            <h2 style="text-align: left; margin-bottom: 2rem; color: #2c3e50;">Latest Updates</h2>
            
            {% assign recent_posts = site.posts | limit: 5 %}
            
            {% if recent_posts.size > 0 %}
            <div class="posts-vertical-list">
                {% for post in recent_posts %}
                <article class="post-card-horizontal">
                    <div class="post-card-content-horizontal">
                        <div class="post-meta-horizontal">
                            <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
                            {% if post.categories.size > 0 %}<span class="post-category">{{ post.categories | first }}</span>{% endif %}
                        </div>
                        
                        <h3 class="post-title-horizontal">
                            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
                        </h3>
                        
                        <div class="post-excerpt-horizontal">
                            {% if post.excerpt %}
                                {{ post.excerpt | strip_html | truncatewords: 40 }}
                            {% else %}
                                {{ post.content | strip_html | truncatewords: 40 }}
                            {% endif %}
                        </div>
                        
                        <a href="{{ post.url | relative_url }}" class="read-more-link">Read Full Article →</a>
                    </div>
                    
                    {% if post.image %}
                    <div class="post-image-horizontal">
                        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
                    </div>
                    {% endif %}
                </article>
                {% endfor %}
            </div>
            
            <div class="text-center mt-2">
                <a href="{{ '/posts/' | relative_url }}" class="btn">View All Posts</a>
            </div>
            
            {% else %}
            <div class="text-center">
                <p>No posts available yet. Check back soon for updates!</p>
            </div>
            {% endif %}
        </section>
    </div>

    <!-- Right Sidebar -->
    <div class="sidebar">
        <!-- Upcoming Events Widget -->
        <div class="sidebar-widget">
            <h3 class="widget-title">Upcoming Events</h3>
            <div class="widget-content">
                <div class="event-item-small">
                    <div class="event-date-small">July 15</div>
                    <div class="event-info-small">
                        <h4>Weekly Satsang Assembly</h4>
                        <p>Join us for spiritual discourse and community fellowship</p>
                    </div>
                </div>
                
                <div class="event-item-small">
                    <div class="event-date-small">July 20</div>
                    <div class="event-info-small">
                        <h4>Youth Activities Workshop</h4>
                        <p>Character development and leadership skills</p>
                    </div>
                </div>
                
                <div class="event-item-small">
                    <div class="event-date-small">Aug 5</div>
                    <div class="event-info-small">
                        <h4>Janmashtami Celebration</h4>
                        <p>Festival celebrating the birth of Lord Krishna</p>
                    </div>
                </div>
                
                <a href="{{ '/upcoming-events/' | relative_url }}" class="widget-link">View All Events →</a>
            </div>
        </div>

        <!-- Announcements Widget -->
        <div class="sidebar-widget">
            <h3 class="widget-title">Announcements</h3>
            <div class="widget-content">
                <div class="announcement-item">
                    <h4>New Website Launch</h4>
                    <p>We're excited to announce the launch of our new website with improved features and better accessibility.</p>
                    <span class="announcement-date">July 1, 2025</span>
                </div>
                
                <div class="announcement-item">
                    <h4>Volunteer Registration Open</h4>
                    <p>Registration is now open for upcoming community service projects. Join us in serving the community.</p>
                    <span class="announcement-date">June 28, 2025</span>
                </div>
                
                <div class="announcement-item">
                    <h4>Summer Program Schedule</h4>
                    <p>Updated schedule for summer programs and activities. Check timings for all age groups.</p>
                    <span class="announcement-date">June 25, 2025</span>
                </div>
                
                <a href="{{ '/archive/' | relative_url }}" class="widget-link">View All Announcements →</a>
            </div>
        </div>
    </div>
</div>
