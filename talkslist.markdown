---
layout: page
title: Talkslist
permalink: /talks/
collection: talks
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

