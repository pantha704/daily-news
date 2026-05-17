---
layout: default
title: Daily News
---

<p style="text-align:right;">
  <button onclick="refreshToday()" id="refreshBtn"
     style="padding:6px 14px;border:1px solid #ccc;border-radius:4px;background:#fff;cursor:pointer;font-size:0.9em;">
    ↻ Refresh Today
  </button>
  <span id="refreshStatus" style="font-size:0.85em;color:#666;margin-left:8px;"></span>
</p>

<script>
const WORKER_URL = "https://daily-news-refresh.pantha704.workers.dev";
async function refreshToday() {
  const btn = document.getElementById("refreshBtn");
  const status = document.getElementById("refreshStatus");
  btn.disabled = true;
  status.textContent = "triggering...";
  try {
    const r = await fetch(WORKER_URL, { method: "POST" });
    status.textContent = r.ok ? "pipeline started (~10min)" : "failed";
  } catch (e) {
    status.textContent = "error: " + e.message;
  }
  btn.disabled = false;
}
</script>

{% assign all_posts = site.posts | sort: "date" | reverse %}
{% assign total_items = 0 %}
{% assign day_count = 0 %}

{% if all_posts.size == 0 %}
  <p><em>No posts yet. The daily pipeline runs at 06:00 UTC.</em></p>
{% endif %}

<style>
.digest-card {
  border:1px solid #e0d8f0;border-radius:8px;padding:12px 18px;margin:12px 0;
  transition:box-shadow .15s;
}
.digest-card:hover { box-shadow:0 2px 8px rgba(0,0,0,.08); }
.digest-card .date { font-size:1.1em;font-weight:600;color:#333;text-decoration:none; }
.digest-card .date:hover { color:#157878; }
.digest-card .desc { color:#666;font-size:.9em;margin-top:4px; }
.digest-card .meta { font-size:.8em;color:#999;margin-top:4px; }
</style>

{% assign en_posts = all_posts | where: "lang", "en" %}
{% for post in en_posts limit:20 %}
  {% assign day_count = day_count | plus: 1 %}
  {% assign cur_date = post.date | date: "%Y-%m-%d" %}
  {% assign num = post.description | split: "," | last | split: " " | first | plus: 0 %}
  {% assign total_items = total_items | plus: num %}
  <div class="digest-card">
    <a href="{{ post.url | relative_url }}" class="date">{{ cur_date }}</a>
    {% if post.description %}
    <div class="desc">{{ post.description }}</div>
    {% endif %}
  </div>
{% endfor %}

<p style="color:#999;font-size:.85em;">{{ total_items }} articles across {{ day_count }} digest{% if day_count != 1 %}s{% endif %}</p>
