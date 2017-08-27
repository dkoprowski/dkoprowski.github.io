---
layout: archive
permalink: /categories/productivity/
title: Productivity
header:
  overlay_image: /assets/images/2016/cover-1.jpg
  overlay_color: "#333"
  overlay_filter: 0.5
---


<div id="archives">
{% for post in site.categories.productivity %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>