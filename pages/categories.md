---
layout: default
title: Categories
permalink: /categories
---

<div class="wrapper">
  <div class="page-wrapper">
    <div class="page-header">
      <p class="page-eyebrow">Workpads Standard</p>
      <h1>Categories</h1>
    </div>

    {% assign cats = site.categories | sort %}
    {% if cats.size > 0 %}
    <ul class="category-index">
      {% for category in cats %}
        {% assign cat_name = category[0] %}
        {% assign cat_posts = category[1] %}
        <li class="category-index-item">
          <a href="/categories/{{ cat_name | slugify }}" class="cat-index-link">
            <span class="cat-index-name">{{ cat_name }}</span>
            <span class="cat-index-count">{{ cat_posts.size }} post{% if cat_posts.size != 1 %}s{% endif %}</span>
          </a>
          <ul class="cat-post-list">
            {% for post in cat_posts limit:3 %}
            <li>
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
              <span class="label-mono">{{ post.date | date: "%Y-%m-%d" }}</span>
            </li>
            {% endfor %}
            {% if cat_posts.size > 3 %}
            <li class="cat-more">
              <a href="/categories/{{ cat_name | slugify }}">+{{ cat_posts.size | minus: 3 }} more →</a>
            </li>
            {% endif %}
          </ul>
        </li>
      {% endfor %}
    </ul>
    {% else %}
    <p style="color:var(--text-muted)">No categories yet.</p>
    {% endif %}
  </div>
</div>
