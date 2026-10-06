---
layout: default
title: Achievements
permalink: /achievements/
---

<p class="kicker">Selected work</p>
<h1 class="display">A collection of awards and achievements.</h1>

{% for group in site.data.achievements %}
<section class="year-block" id="{{ group.year }}">
  <h2>{{ group.year }}</h2>
  {% if group.items.size == 0 %}
  <p class="muted">Nothing listed for this year yet.</p>
  {% else %}
  <ul class="award-list">
    {% for item in group.items %}
    <li>
      <span class="award-name">{{ item.title }}</span>
      <span class="award-result">{{ item.result }}</span>
    </li>
    {% endfor %}
  </ul>
  {% endif %}
</section>
{% endfor %}
