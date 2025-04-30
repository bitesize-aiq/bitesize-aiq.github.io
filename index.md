---
layout: default
title: Home
---

<section class="hero-section">
  <div class="container">
    <h1 class="hero-title">Increase your Artificial Intelligence IQ</h1>
    <p class="hero-description">The AI revolution is happening right now. Discover the latest tools, concepts, and applications to stay ahead.</p>
    <div class="hero-cta">
      <a href="#featured-posts" class="btn btn-primary">Start Learning</a>
      <a href="/about/" class="btn btn-secondary">About Us</a>
    </div>
  </div>
</section>

<section id="featured-posts" class="featured-posts">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Latest Articles</h2>
      <p class="section-description">Stay up to date with the newest developments in AI</p>
    </div>
    <div class="post-grid">
      {% for post in site.posts limit:6 %}
        <article class="post-card">
          <a href="{{ post.url | relative_url }}">
            <div class="post-card-image">
              {% if post.featured_image %}
              <img src="{{ post.featured_image | relative_url }}" alt="{{ post.title }}">
              {% else %}
              <img src="/assets/images/posts/ai-productivity.jpg" alt="{{ post.title }}">
              {% endif %}
              <div class="post-card-tags">
                {% if post.categories[0] %}
                <div class="post-card-category {{ post.categories[0] | slugify }}">{{ post.categories[0] | replace: '-', ' ' | replace: 'ai ', 'AI ' }}</div>
                {% endif %}
                {% if post.difficulty %}
                <div class="post-card-difficulty {{ post.difficulty | downcase }}">{{ post.difficulty }}</div>
                {% endif %}
              </div>
            </div>
            <div class="post-card-content">
              <h3 class="post-card-title">{{ post.title }}</h3>
              <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
              <div class="post-card-meta">
                <span class="post-card-author">{{ post.author | default: site.author.name }}</span>
                <span class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</span>
              </div>
            </div>
          </a>
        </article>
      {% endfor %}
    </div>
    <div style="text-align: center; margin-top: 4rem;">
      <a href="/all-articles/" class="btn btn-secondary">View All Articles</a>
    </div>
  </div>
</section>

<section class="categories-section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Explore by Category</h2>
      <p class="section-description">Find the AI topics that interest you most</p>
    </div>
    <div class="category-grid">
      <a href="/category/ai-tools/" class="category-card">
        <div class="category-icon"><i class="fas fa-tools"></i></div>
        <h3 class="category-title">AI Tools</h3>
        <p class="category-description">Discover and master the most powerful AI tools for productivity, creativity, and more</p>
        <span class="btn btn-primary">Explore Tools</span>
      </a>
      <a href="/category/ai-concepts/" class="category-card">
        <div class="category-icon"><i class="fas fa-lightbulb"></i></div>
        <h3 class="category-title">AI Concepts</h3>
        <p class="category-description">Understand the fundamental ideas behind artificial intelligence in simple terms</p>
        <span class="btn btn-primary">Learn Concepts</span>
      </a>
      <a href="/category/ai-applications/" class="category-card">
        <div class="category-icon"><i class="fas fa-rocket"></i></div>
        <h3 class="category-title">AI Applications</h3>
        <p class="category-description">See how AI is transforming industries and creating new possibilities</p>
        <span class="btn btn-primary">Discover Applications</span>
      </a>
    </div>
  </div>
</section>

<section class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Our Mission</h2>
      <p class="section-description">Helping everyone increase their artificial intelligence IQ, one bite at a time</p>
    </div>
    <div class="post-content" style="max-width: 800px; margin: 0 auto; text-align: center;">
      <p>At bitesize AIQ, we believe that artificial intelligence is the most transformative technology of our generation. Our mission is to help everyone increase their AI literacy through bite-sized, accessible content that demystifies complex concepts and showcases practical tools.</p>
      <p>Whether you're looking to enhance your productivity, boost your creativity, or simply understand how AI is changing our world, we're here to guide you through the AI revolution—one bite at a time.</p>
      <div style="margin-top: 3rem;">
        <a href="/about/" class="btn btn-secondary">Learn More About Us</a>
      </div>
    </div>
  </div>
</section>

<section class="aiq-score-section">
  <div class="aiq-score-container">
    <h2 class="aiq-score-title">Track Your AIQ Score</h2>
    <p class="aiq-score-subtitle">
      As you learn and complete quizzes, watch your AIQ score grow across six essential AI
      literacy categories
    </p>
    
    <div class="aiq-score-content">
      <div class="aiq-score-visualization">
        <div class="aiq-hexagon">
          <div class="aiq-hexagon-inner">
            <div class="aiq-hexagon-category">Automation</div>
            <div class="aiq-hexagon-score">80</div>
          </div>
        </div>
        
        <div class="aiq-hexagon">
          <div class="aiq-hexagon-inner">
            <div class="aiq-hexagon-category">Understanding</div>
            <div class="aiq-hexagon-score">75</div>
          </div>
        </div>
        
        <div class="aiq-hexagon">
          <div class="aiq-hexagon-inner">
            <div class="aiq-hexagon-category">Processing</div>
            <div class="aiq-hexagon-score">65</div>
          </div>
        </div>
        
        <div class="aiq-hexagon">
          <div class="aiq-hexagon-inner">
            <div class="aiq-hexagon-category">Critical</div>
            <div class="aiq-hexagon-score">60</div>
          </div>
        </div>
        
        <div class="aiq-hexagon aiq-hexagon-total">
          <div class="aiq-hexagon-inner">
            <div class="aiq-hexagon-category">Total</div>
            <div class="aiq-hexagon-score">720</div>
          </div>
        </div>
        
        <div class="aiq-hexagon">
          <div class="aiq-hexagon-inner">
            <div class="aiq-hexagon-category">Application</div>
            <div class="aiq-hexagon-score">70</div>
          </div>
        </div>
      </div>
      
      <div class="aiq-score-breakdown">
        <h3>Your AIQ Breakdown</h3>
        
        <div class="aiq-score-item">
          <div class="aiq-score-label">Automation</div>
          <div class="aiq-score-value">80/100</div>
        </div>
        <div class="aiq-score-bar">
          <div class="aiq-score-progress aiq-score-automation" style="width: 80%"></div>
        </div>
        
        <div class="aiq-score-item">
          <div class="aiq-score-label">Processing Speed</div>
          <div class="aiq-score-value">65/100</div>
        </div>
        <div class="aiq-score-bar">
          <div class="aiq-score-progress aiq-score-processing" style="width: 65%"></div>
        </div>
        
        <div class="aiq-score-item">
          <div class="aiq-score-label">Understanding</div>
          <div class="aiq-score-value">75/100</div>
        </div>
        <div class="aiq-score-bar">
          <div class="aiq-score-progress aiq-score-understanding" style="width: 75%"></div>
        </div>
        
        <div class="aiq-score-item">
          <div class="aiq-score-label">Critical Thinking</div>
          <div class="aiq-score-value">60/100</div>
        </div>
        <div class="aiq-score-bar">
          <div class="aiq-score-progress aiq-score-critical" style="width: 60%"></div>
        </div>
        
        <div class="aiq-score-item">
          <div class="aiq-score-label">Innovation</div>
          <div class="aiq-score-value">50/100</div>
        </div>
        <div class="aiq-score-bar">
          <div class="aiq-score-progress aiq-score-innovation" style="width: 50%"></div>
        </div>
        
        <div class="aiq-score-item">
          <div class="aiq-score-label">Application</div>
          <div class="aiq-score-value">70/100</div>
        </div>
        <div class="aiq-score-bar">
          <div class="aiq-score-progress aiq-score-application" style="width: 70%"></div>
        </div>
        
        <div class="aiq-score-note">
          Complete more lessons and tests to increase your AIQ score. The higher your score in each category, the more advanced AI concepts you'll unlock.
        </div>
      </div>
    </div>
  </div>
</section>
