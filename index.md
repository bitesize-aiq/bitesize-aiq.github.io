---
layout: default
title: Home
description: Welcome to my blog.
---

Welcome to **My Awesome Blog**! This site is powered by Jekyll on GitHub Pages.

Here are the latest posts:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      ({{ post.date | date: "%b %-d, %Y" }})
    </li>
  {% endfor %}
</ul>
