---
layout: page
title: Categories
permalink: /categories/
---

{% assign categories = site.categories | sort %}
{% for category in categories %}
  {% assign category_name = category | first %}
  {% assign posts = category | last %}
  {% assign post_count = posts | size %}
  {% if post_count > 0 %}
    <h2 id="{{ category_name | slugify }}">{{ category_name }} ({{ post_count }})</h2>
    <ul>
      {% for post in posts %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  {% endif %}
{% endfor %}