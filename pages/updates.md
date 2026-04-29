---
layout: default
title: Updates
permalink: /updates
---

<div class="wrapper">
  <div class="updates-page">
    <div class="page-header">
      <p class="page-eyebrow">Workpads Standard</p>
      <h1>Updates</h1>
    </div>

    {% if site.posts.size > 0 %}
    <ul class="updates-list">
      {% for post in site.posts %}
      <li>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 35 }}</p>
        {% endif %}
        <div class="post-meta-row">
          <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
          {% for cat in post.categories %}
          <a class="cat-tag" href="/categories/{{ cat | slugify }}">{{ cat }}</a>
          {% endfor %}
        </div>
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <p style="color:var(--text-muted);margin-top:var(--spacing)">No updates yet.</p>
    {% endif %}

    <p style="margin-top:var(--spacing);font-size:0.85rem;display:flex;gap:20px;flex-wrap:wrap">
      <a href="/categories">Browse by category →</a>
      <a href="{{ "/feed.xml" | relative_url }}">Subscribe via RSS →</a>
    </p>
  </div>
</div>
