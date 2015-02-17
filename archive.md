---
title: Archive
layout: page
permalink: /archive/
---

<div class="archives"></h1>
  {% assign last_year = 0 %}
  {% for post in site.posts %}
    {% capture current_year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% if last_year != current_year %}
      <h2 class='archive-year'>{{ post.date | date: '%Y' }}</h2>
    {% endif %}
    <h3 class="archives-entry"><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h3>
    {% assign last_year = current_year %}
  {% endfor %}
</div>
