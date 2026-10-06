---
layout: default
title: Blogs
permalink: /blogs/
---

# Blogs

To publish a new post, add a Markdown file in `_posts/` named `YYYY-MM-DD-title.md`.

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in posts_by_year %}
## {{ year.name }}
<ul class="post-list">
  {% for post in year.items %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="muted"> — {{ post.date | date: "%d %b %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% endfor %}

{% if site.posts.size == 0 %}
<p>No posts yet.</p>
{% endif %}
