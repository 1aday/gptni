---
title: Books
description: Collection of books I've read and recommend
date: 2024-01-01
hide:
  - navigation
  - toc
template: books.html
---

<div class="grid">
{% for page in pages | selectattr("meta.type", "equalto", "book") | sort(attribute="meta.date") | reverse %}
  <div class="book-card">
    <a href="{{ page.url }}">
      {% if page.meta.cover %}
        <img class="book-cover" src="{{ page.meta.cover }}" alt="{{ page.meta.title }}">
      {% endif %}
      <div class="book-info">
        <h3>{{ page.meta.title }}</h3>
        {% if page.meta.author %}
          <p class="author">by {{ page.meta.author }}</p>
        {% endif %}
        {% if page.meta.description %}
          <p class="description">{{ page.meta.description }}</p>
        {% endif %}
      </div>
    </a>
  </div>
{% endfor %}
</div>