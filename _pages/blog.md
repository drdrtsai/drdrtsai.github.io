---
layout: page
permalink: /blog/
title: Blog
nav: true
nav_order: 5
---

<style>
  .blog-list { list-style: none; padding: 0; margin: 0; }
  .blog-list > li { margin-bottom: 1.6rem; }
  .blog-list .blog-title { font-weight: bold; font-size: 1.05rem; margin-bottom: 0.1rem; }
  .blog-list .blog-title a { color: var(--global-text-color); }
  .blog-list .blog-title a:hover { color: var(--global-theme-color); }
  .blog-list .blog-date { color: var(--global-text-color-light); font-size: 0.85rem; margin-bottom: 0.3rem; }
  .blog-list p { margin-bottom: 0.3rem; }
</style>

<ul class="blog-list">
  {% for post in site.posts %}
  <li>
    <div class="blog-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></div>
    <div class="blog-date">{{ post.date | date: "%B %-d, %Y" }}</div>
    <p>{{ post.summary }}</p>
  </li>
  {% endfor %}
</ul>
