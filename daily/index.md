---
layout: default
title: Daily News
---

{% assign all_posts = site.posts | sort: "date" | reverse %}

{% if all_posts.size == 0 %}
  <p><em>No posts yet. The daily pipeline runs at 06:00 UTC.</em></p>
{% endif %}

{% for post in all_posts limit:10 %}
  <article style="margin-bottom:2rem;padding-bottom:1.5rem;border-bottom:1px solid #e0d8f0;">
    <h2 style="margin-bottom:0.25rem;">
      <a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }} — {{ post.lang | upcase }}</a>
    </h2>
    <p style="color:#666;margin-top:0;">{{ post.description }}</p>
    <ul style="list-style:none;padding:0;">
      {% assign items = post.content | split: "1. " | shift %}
      {% for item in items limit:5 %}
        {% assign title = item | split: "]" | first | remove: "[" %}
        {% if title != "" %}
          <li style="margin:0.25rem 0;">• {{ title }}</li>
        {% endif %}
      {% endfor %}
    </ul>
  </article>
{% endfor %}
