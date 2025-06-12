---
layout: default
title: Contact Us
description: We'd love to hear your questions about AI tools and technologies
permalink: /contact/
---

<div class="page-header">
  <div class="container">
    <h1 class="page-title">{{ page.title }}</h1>
    <p class="page-subtitle">{{ page.description }}</p>
  </div>
</div>

<section class="section">
  <div class="container">
    <div class="post-content">
      <div class="contact-info">
        <h2>Get In Touch</h2>
        <p>Have questions about specific AI tools? Looking for recommendations? Want to suggest a topic we should cover? We're here to help boost your AIQ!</p>

        <div class="contact-methods">
          
          <div class="contact-method">
            <div class="contact-header">
              <div class="contact-icon">
                <i class="fas fa-envelope" aria-hidden="true"></i>
              </div>
              <h3>Email Us</h3>
            </div>
            <p><a href="mailto:bitesize.aiq@gmail.com">bitesize.aiq@gmail.com</a></p>
          </div>

          <div class="contact-method">
            <div class="contact-header">
              <div class="contact-icon">
                <i class="fas fa-share-alt" aria-hidden="true"></i>
              </div>
              <h3>Follow Us</h3>
            </div>
            <div>
              <div class="social-links contact-social">
                <a href="https://twitter.com/{{ site.twitter_username }}" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="https://linkedin.com/{{ site.linkedin_username }}" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
                <a href="#" aria-label="Discord"><i class="fab fa-discord"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="contact-form-container">
        <h2>Ask Us About AI</h2>
        <form class="contact-form" action="https://formspree.io/f/mpwrpgjq" method="POST">
          <div class="form-field">
            <label for="name" class="form-label">Name</label>
            <input type="text" id="name" name="name" class="form-input" required>
          </div>

          <div class="form-field">
            <label for="email" class="form-label">Email</label>
            <input type="email" id="email" name="_replyto" class="form-input" required>
          </div>

          <div class="form-field">
            <label for="subject" class="form-label">Subject</label>
            <input type="text" id="subject" name="subject" class="form-input" required>
          </div>

          <div class="form-field">
            <label for="ai-interest" class="form-label">What AI topics are you most interested in?</label>
            <select id="ai-interest" name="ai-interest" class="form-input">
              <option value="productivity">AI for Productivity</option>
              <option value="creativity">AI for Creativity</option>
              <option value="business">AI for Business</option>
              <option value="education">AI for Education</option>
              <option value="personal">AI for Personal Use</option>
              <option value="other">Other (Please specify in message)</option>
            </select>
          </div>

          <div class="form-field">
            <label for="message" class="form-label">Message</label>
            <textarea id="message" name="message" class="form-input" rows="6" required></textarea>
          </div>

          <div class="form-field">
            <button type="submit" class="btn btn-primary">Send Message</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>
