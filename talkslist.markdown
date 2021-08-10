---
layout: archive
title: Talkslist
permalink: /talks/
collection: talks
sort_by: number
---

### TEST:

{% for post in site.talks %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    <li id="y{{currentdate}}">{{ currentdate }}</li>
    {% assign date = currentdate %} 
  {% endif %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}

