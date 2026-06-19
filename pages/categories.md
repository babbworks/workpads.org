---
layout: default
title: Categories
permalink: /categories
---

<div class="page">
  <div class="container">
    <p class="structural">Browse</p>
    <h1 class="page-title">CATEGORIES</h1>

    <div style="margin-top:2rem;">
      {% for category in site.categories %}
      <div style="margin-bottom:2rem;">
        <h3 style="color:var(--accent);text-transform:uppercase;font-size:1.2rem;">{{ category[0] }}</h3>
        <ul class="post-list">
          {% for post in category[1] %}
          <li class="post-item">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span class="post-date">{{ post.date | date: "%d.%m.%Y" }}</span>
          </li>
          {% endfor %}
        </ul>
      </div>
      {% endfor %}
    </div>
  </div>
</div>
