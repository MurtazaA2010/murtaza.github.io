---
layout: default
title: Achievements
permalink: /achievements/
---

# Achievements

{% for group in site.data.achievements %}
<h2 id="{{ group.year }}">{{ group.year }}</h2>
{% if group.items.size == 0 %}
<p class="muted">Nothing listed for this year yet.</p>
{% else %}
{% for item in group.items %}
<div class="achievement">
  <p><strong>{{ item.title }}</strong><br>{{ item.result }}</p>
</div>
{% endfor %}
{% endif %}
{% endfor %}
