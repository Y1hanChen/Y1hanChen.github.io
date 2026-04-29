---
layout: page
title: Blog
permalink: /blog/
---

<div class="blog-page">
  <p class="blog-intro">
    Thoughts on NLP, LLM safety, and research experiences.
  </p>

  <div class="posts-list">
    {% for post in site.posts %}
      <article class="post-preview">
        <h2 class="post-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <p class="post-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%B %-d, %Y" }}
          </time>
        </p>
        {% if post.excerpt %}
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
        {% endif %}
        <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
      </article>
    {% endfor %}
  </div>

  {% if site.posts.size == 0 %}
  <p class="no-posts">No posts yet. Check back soon!</p>
  {% endif %}
</div>
