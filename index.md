---
layout: default
title: Daily News
---

<p style="text-align:right;display:flex;align-items:center;justify-content:flex-end;gap:12px;flex-wrap:wrap;">
  <span id="pipelineStatus" style="font-size:0.85em;"></span>
  <button onclick="refreshToday()" id="refreshBtn"
     style="padding:6px 14px;border:1px solid #157878;border-radius:4px;background:#157878;color:#fff;cursor:pointer;font-size:0.9em;">
    ↻ Refresh (today)
  </button>
  <span id="refreshStatus" style="font-size:0.85em;color:#666;margin-left:0;"></span>
</p>

<script>
const WORKER_URL = "https://daily-news-refresh.pantha704.workers.dev";
const PIPELINE_ID = "daily-summary.yml";
const CACHE_KEY = "pipelineStatus";

function setCached(html, ttl) {
  localStorage.setItem(CACHE_KEY, JSON.stringify({html: html, expiry: Date.now() + ttl}));
}

function getCached() {
  try {
    var c = JSON.parse(localStorage.getItem(CACHE_KEY));
    if (c && c.expiry > Date.now()) return c.html;
  } catch(e) {}
  return null;
}

function renderStatus(html) {
  document.getElementById("pipelineStatus").innerHTML = html;
}

async function checkPipelineStatus() {
  renderStatus(getCached() || "");
  try {
    const r = await fetch("https://api.github.com/repos/pantha704/daily-news/actions/workflows/" + PIPELINE_ID + "/runs?per_page=1&status=in_progress");
    const data = await r.json();
    if (data.workflow_runs && data.workflow_runs.length > 0) {
      var h = '<span style="color:#e05d44;">●</span> running';
      renderStatus(h);
      setCached(h, 60000);
      return;
    }
    const r2 = await fetch("https://api.github.com/repos/pantha704/daily-news/actions/workflows/" + PIPELINE_ID + "/runs?per_page=1&status=completed");
    const d2 = await r2.json();
    if (d2.workflow_runs && d2.workflow_runs.length > 0) {
      const last = d2.workflow_runs[0];
      const t = new Date(last.updated_at);
      const s = t.toLocaleString(undefined, {month:"short",day:"numeric",hour:"2-digit",minute:"2-digit"});
      var h = '<span style="color:#2ea44f;">●</span> last run: ' + s;
      renderStatus(h);
      setCached(h, 300000);
    } else {
      var h = '<span style="color:#999;">○</span> idle';
      renderStatus(h);
      setCached(h, 300000);
    }
  } catch (e) {
    renderStatus(getCached() || "");
  }
}

async function refreshToday() {
  const btn = document.getElementById("refreshBtn");
  const status = document.getElementById("refreshStatus");
  btn.disabled = true;
  status.textContent = "triggering...";
  var h = '<span style="color:#e05d44;">●</span> running';
  renderStatus(h);
  setCached(h, 600000);
  try {
    const r = await fetch(WORKER_URL, { method: "POST" });
    status.textContent = r.ok ? "pipeline started (~10min)" : "failed";
  } catch (e) {
    status.textContent = "error: " + e.message;
  }
  btn.disabled = false;
}

checkPipelineStatus();
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

<script>
(function(){
  var btn = document.querySelector(".page-header .btn");
  if (btn) {
    var el = document.createElement("div");
    el.style.cssText = "text-align:center;margin-top:12px;font-size:.85em;";
    el.innerHTML = 'built upon <a href="https://github.com/Thysrael/Horizon" style="color:inherit;text-decoration:underline;">Horizon</a>';
    btn.parentNode.insertBefore(el, btn.nextSibling);
  }
})();
</script>
