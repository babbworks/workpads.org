---
layout: default
title: Updates
permalink: /updates
---

<div class="page">
  <div class="container">
    <p class="structural">Workpads</p>
    <h1 class="page-title">UPDATES</h1>

    {% if site.posts.size > 0 %}
    <ul class="post-list" style="margin-top:2rem;">
      {% for post in site.posts %}
      <li class="post-item" style="flex-direction:column;gap:0.5rem;">
        <a href="{{ post.url | relative_url }}" style="font-size:1.2rem;">{{ post.title }}</a>
        {% if post.excerpt %}
        <p style="color:var(--text-muted);font-size:0.95rem;margin:0;">{{ post.excerpt | strip_html | truncatewords: 35 }}</p>
        {% endif %}
        <div class="post-meta-row">
          <span class="post-date">{{ post.date | date: "%d.%m.%Y" }}</span>
          {% for cat in post.categories %}
          <a class="cat-tag" href="/categories/{{ cat | slugify }}">{{ cat }}</a>
          {% endfor %}
        </div>
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <p style="color:var(--text-muted);margin-top:2rem;">No updates yet.</p>
    {% endif %}

    <p style="margin-top:2rem;font-size:0.85rem;display:flex;gap:1.5rem;flex-wrap:wrap;">
      <a href="/categories">Browse by category →</a>
      <a href="{{ '/feed.xml' | relative_url }}">Subscribe via RSS →</a>
    </p>
  </div>
</div>
