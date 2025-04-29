---
layout: default
title: Home
---

<header class="hero">
  <div class="hero-content">
    <h1>Increase your Artificial Intelligence IQ</h1>
    <p>The AI revolution is happening right now. Discover the latest tools, concepts, and applications to stay ahead.</p>
    <a href="#featured-posts" class="btn btn-primary">Start Learning</a>
  </div>
</header>

<section id="mission" class="section">
  <div class="container">
    <h2>Our Mission</h2>
    <p>At bitesize AIQ, we believe that artificial intelligence is the most transformative technology of our generation. Our mission is to help everyone increase their AI literacy through bite-sized, accessible content that demystifies complex concepts and showcases practical tools.</p>
    <p>Whether you're looking to enhance your productivity, boost your creativity, or simply understand how AI is changing our world, we're here to guide you through the AI revolution—one bite at a time.</p>
  </div>
</section>

<section id="categories" class="section bg-light">
  <div class="container">
    <h2>Explore AI Topics</h2>
    <div class="category-grid">
      <a href="/category/ai-tools/" class="category-card">
        <div class="category-icon">🛠️</div>
        <h3>AI Tools</h3>
        <p>Discover and master the most powerful AI tools for productivity, creativity, and more</p>
      </a>
      <a href="/category/ai-concepts/" class="category-card">
        <div class="category-icon">💡</div>
        <h3>AI Concepts</h3>
        <p>Understand the fundamental ideas behind artificial intelligence in simple terms</p>
      </a>
      <a href="/category/ai-applications/" class="category-card">
        <div class="category-icon">🚀</div>
        <h3>AI Applications</h3>
        <p>See how AI is transforming industries and creating new possibilities</p>
      </a>
    </div>
  </div>
</section>

<section id="featured-posts" class="section">
  <div class="container">
    <h2>Latest Articles</h2>
    <div class="post-grid">
      {% for post in site.posts limit:6 %}
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
    <div class="text-center">
      <a href="/all-articles" class="btn btn-secondary">View All Articles</a>
    </div>
  </div>
</section>
