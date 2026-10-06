---
layout: default
title: Blogs
permalink: /blogs/
---

<p class="kicker">Writing</p>
<h1 class="display">Notes, thoughts, and posts.</h1>

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in posts_by_year %}
<h2>{{ year.name }}</h2>
<ul class="post-list">
  {% for post in year.items %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="muted">{{ post.date | date: "%d %b %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% endfor %}

{% if site.posts.size == 0 %}
<p>No posts yet.</p>
{% endif %}

<p class="note">New post: add a Markdown file in <code>_posts/</code> named <code>YYYY-MM-DD-title.md</code>.</p>
