---
layout: page
title: Talkslist
permalink: /talklist/
---

### TEST:

{% for post in site.talklist %}
<article>
        <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
        <time datetime="{{ post.date | date: "%Y-%m-%d" }}">
                {{ post.date | date_to_string }}
        </time>
        {{ post.content }}
</article>
{% endfor %}

