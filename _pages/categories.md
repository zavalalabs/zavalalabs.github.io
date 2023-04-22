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
    ## {{ category_name }} ({{ post_count }})
      {% for post in posts %}
        ### [{{ post.title }}]({{ post.url }})
      {% endfor %}
    </ul>
  {% endif %}
{% endfor %}
