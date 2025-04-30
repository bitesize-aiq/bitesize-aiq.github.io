---
layout: default
title: All Articles
---

<section class="section">
  <div class="container">
    <h1 class="page-title">All Articles</h1>
    
    <div class="post-grid">
      {% for post in site.posts %}
        <div class="post-card">
          <a href="{{ post.url }}">
            {% if post.featured_image %}
            <div class="post-card-image">
              <img src="{{ post.featured_image }}" alt="{{ post.title }}">
              <div class="post-card-tags">
                {% if post.categories[0] %}
                <div class="post-card-category {{ post.categories[0] | slugify }}">{{ post.categories[0] | replace: '-', ' ' | replace: 'ai ', 'AI ' }}</div>
                {% endif %}
                {% if post.difficulty %}
                <div class="post-card-difficulty {{ post.difficulty | downcase }}">{{ post.difficulty }}</div>
                {% endif %}
              </div>
            </div>
            {% endif %}
            <div class="post-card-content">
              <h3 class="post-card-title">{{ post.title }}</h3>
              <p class="post-card-excerpt">{{ post.description | truncate: 120 }}</p>
              <div class="post-card-meta">
                <span class="post-card-author">{{ post.author | default: site.author.name }}</span>
                <span class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</span>
              </div>
            </div>
          </a>
        </div>
      {% endfor %}
    </div>
  </div>
</section>