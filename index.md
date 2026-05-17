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
{% assign day_count = 0 %}

{% if all_posts.size == 0 %}
  <p><em>No posts yet. The daily pipeline runs at 06:00 UTC.</em></p>
{% endif %}

{% assign en_posts = all_posts | where: "lang", "en" %}
{% for post in en_posts limit:20 %}
  {% assign day_count = day_count | plus: 1 %}
  {% assign cur_date = post.date | date: "%Y-%m-%d" %}
  {% assign num = post.description | split: "," | last | split: " " | first | plus: 0 %}
  {% assign total_items = total_items | plus: num %}
  <p style="margin:0.5rem 0;">
    <a href="{{ post.url | relative_url }}" style="font-size:1.1em;">
      {{ cur_date }}
    </a>
    {% if post.description %}
    <br><small>{{ post.description }}</small>
    {% endif %}
  </p>
{% endfor %}

<p><em>{{ total_items }} articles across {{ day_count }} digest{% if day_count != 1 %}s{% endif %}</em></p>
