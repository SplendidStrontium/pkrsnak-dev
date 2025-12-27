---
layout: default
title: "Home"
permalink: /
---

<div class="homepage-intro">
  <p style="margin-top: 2em; margin-bottom: 2em;">I'm a student and aspiring astrophysicist based in New York. This site is a home for my academic work, research projects, and professional updates as I make my way toward a career in astrophysics research.</p>
</div>

<hr>

<div class="recent-posts">
  <h2>Recent Posts</h2>

{% for post in site.posts limit: 5 %}
<article class="post-card">
  <h3 class="post-card-title">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </h3>
  <p class="post-card-meta">
    {{ post.date | date: "%Y-%m-%d" }}
    {% if post.categories.size > 0 %}
      // {{ post.categories | join: ", " }}
    {% endif %}
  </p>
  <p class="post-card-excerpt">
    {{ post.excerpt | strip_html | truncatewords: 30 }}
  </p>
  <a href="{{ post.url }}" class="post-card-link">continue reading →</a>
</article>
{% endfor %}
</div>