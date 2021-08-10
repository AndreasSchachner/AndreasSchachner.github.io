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

<ul class="posts">
  <span>Articles</span>
  {% for post in site.talklist %}
    {% unless post.next %}
    <div class="line"><span>{{ post.date | date: '%Y' }}</span></div>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <div class="line"><span>{{ post.date | date: '%Y' }}</span></div>
      {% endif %}
    {% endunless %}

    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

