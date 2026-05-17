---
layout: default
title: Daily News
---

<p style="text-align:right;">
  <a href="https://github.com/pantha704/daily-news/actions/workflows/daily-summary.yml"
     style="display:inline-block;padding:6px 14px;border:1px solid #ccc;border-radius:4px;text-decoration:none;font-size:0.9em;">
    ↻ Refresh Today
  </a>
</p>

{% assign all_posts = site.posts | sort: "date" | reverse %}
{% assign total_items = 0 %}

{% if all_posts.size == 0 %}
  <p><em>No posts yet. The daily pipeline runs at 06:00 UTC.</em></p>
{% endif %}

{% for post in all_posts limit:20 %}
  {% assign desc = post.description | split: "," | last | split: " " | first %}
  {% assign num = desc | plus: 0 %}
  {% if num > 0 %}
    {% assign total_items = total_items | plus: num %}
  {% endif %}
  <p style="margin:0.5rem 0;">
    <a href="{{ post.url | relative_url }}" style="font-size:1.1em;">
      {{ post.date | date: "%Y-%m-%d" }} — {{ post.lang | upcase }}
    </a>
    {% if post.description %}
    <br><small>{{ post.description }}</small>
    {% endif %}
  </p>
{% endfor %}

<p><em>{{ total_items }} articles across {{ all_posts.size }} digest{% if all_posts.size != 1 %}s{% endif %}</em></p>
