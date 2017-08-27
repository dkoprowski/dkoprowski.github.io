---
layout: archive
permalink: /categories/productivity/
title: Productivity
---


<div id="archives">
{% for post in site.categories.productivity %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>