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
          {% if post.featured_image %}
          <img src="{{ post.featured_image }}" alt="{{ post.title }}" class="post-image">
          {% endif %}
          <div class="post-content">
            <span class="post-category">{{ post.categories[0] }}</span>
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <p>{{ post.description | truncate: 120 }}</p>
            <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</section>