---
layout: default
title: Daily News
---

{% assign all_posts = site.posts | sort: "date" | reverse %}

{% if all_posts.size == 0 %}
  <p><em>No posts yet. The daily pipeline runs at 06:00 UTC.</em></p>
{% endif %}

{% for post in all_posts limit:20 %}
  <p style="margin:0.5rem 0;">
    <a href="{{ post.url | relative_url }}" style="font-size:1.1em;">
      {{ post.date | date: "%Y-%m-%d" }} — {{ post.lang | upcase }}
    </a>
    {% if post.description %}
    <br><small>{{ post.description }}</small>
    {% endif %}
  </p>
{% endfor %}
