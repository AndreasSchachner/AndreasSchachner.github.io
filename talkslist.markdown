---
layout: page
title: Talkslist
permalink: /talks/
collection: talks
---

### TEST:

{% for post in site.posts %}
<article>
        <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
        <time datetime="{{ post.date | date: "%Y-%m-%d" }}">
                {{ post.date | date_to_string }}
        </time>
        {{ post.content }}
</article>
{% endfor %}

