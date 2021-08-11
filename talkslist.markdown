---
layout: page
title: Talkslist
permalink: /talklist/
---

{%  for post in site.talklist reversed %}
  <div class='big mod modBlogPost no_bg'>
    <div class='content'>
    
     {% assign currentdate = post.date | date: "%Y" %}
     {% if currentdate != date %}
        <hr>
        <hr>
        <h3><span>{{ post.date | date: '%Y' }}</span></h3>
        {% assign date = currentdate %} 
     {% endif %}

      <p class='info'>
       <!-- /
        <span>
          <a href="#">4 commetns</a>
        </span>-->
      </p>
      <h1>< href="{{ post.url }}">{{ post.title }} </></h1>
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
