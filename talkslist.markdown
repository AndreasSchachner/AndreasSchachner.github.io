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

{%  for post in site.talklist %}
  <div class='big mod modBlogPost no_bg'>
    <div class='content'>
    {% unless post.next %}
    <div class="line"><span>{{ post.date | date: '%Y' }}</span></div>
    {% else %}
    
      <p class='info'>
       <!-- /
        <span>
          <a href="#">4 commetns</a>
        </span>-->
      </p>
      <h1><a href="{{ post.url }}">{{ post.title }} </a></h1>
      <span>{{post.date | date: "%B %d, %Y" }}</span>
      <span>
        at
        {% for cat in post.place %}
          <a href="#">{{cat}}</a>
          {% unless forloop.last %}
              ,
          {% endunless %}
        {% endfor %}
      </span>
      {% if post.preview %}
        <div class='row'>
          <div class='small-6 medium-4 large-4 columns'>
            <img alt="" src="{{site.url}}{{site.baseurl}}/{{post.preview}}" />
          </div>
          <div class='small-6 medium-8 large-8 columns'>
            <p>{{post.excerpt}}</p>
          </div>
        </div>
      {% else %}
        <p>{{post.excerpt}}</p>
      {% endif %}
      
      <div class='spacing'></div>
      <a class="button small" href="{{site.url}}{{site.baseurl}}/{{post.url}}">Read more</a>
    </div>
  </div>
  <hr>
  <div class='two spacing'></div>
{% endfor %}


<div class='four spacing'></div>
