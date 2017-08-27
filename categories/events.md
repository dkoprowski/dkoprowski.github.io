---
layout: archive
permalink: /categories/events/
title: Events
---


<div id="archives">
{% for post in site.categories.events %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>