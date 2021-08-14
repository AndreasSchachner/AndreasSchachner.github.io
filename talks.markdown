---
layout: page
title: Talks
permalink: /talklist/
---



<div>
    <h4>Overview</h4>
        <table>
            <tr>
                <td>Format</td>
                <td>Number</td>
            </tr>
            {% assign array = "" | split: ',' %}
            {%  for post in site.talklist reversed %}
                {% assign currentcat = post.categories %}
                {% if currentcat != cat %}
                   {% assign cat= currentcat %} 
                {% endif %}
                {% if array contains cat%}
                {% else %}
                    {% assign array = array | push: cat %}
                    {% assign total = 0 %}
                    {%  for post in site.talklist reversed %}
                        {% if post.categories == cat %}
                            {% assign total = total | plus: 1 %}
                        {% endif %}
                    {% endfor %}
                    <tr>
                      <td> {{post.categories}} </td>
                      <td> {{total}} </td>
                    </tr>
                {% endif %}
              {% endfor %}
        </table>
</div>

<style>
  .bo {
     margin-bottom: 0.25cm;
  }
</style>

<style>
  .bt {
     margin-bottom: 0.5cm;
  }
</style>

<style>
  .rightbm{
       text-align: right;
       margin-bottom: -0.5cm;
  }
</style>




{%  for post in site.talklist reversed %}
  <div class='big mod modBlogPost no_bg'>
    <div class='content'>
     {% assign blog = "" | split: ',' %}
     {% assign blog = array | push: "Blog post" %}
    
     {% assign currentdate = post.date | date: "%Y" %}
     {% if currentdate != date %}
        <br>
        <br>
        <br>
        <h1><span>{{ post.date | date: '%Y' }}</span></h1>
        <hr>
        {% assign date = currentdate %} 
     {% endif %}
     
     <p class="rightbm">
      {{post.date | date: "%B %d, %Y" }}
     </p>
      <p class="bo">
       <a href="{{post.eventurl}}">{{ post.title }} </a>
      </p>
      <span>
      Title: {{post.talktitle}}
      </span>
      <br>
      {% if post.categories == 'Blog post' %}
        {{post.categories}}
      {% endif %}
      {% if post.categories == "Blog post" %}
        {{post.categories}}
      {% endif %}
      {% if post.categories == Blog post %}
        {{post.categories}}
      {% endif %}
      {% if blog contains post.categories%}
        {{post.categories}}
      {% endif %}
      {% if post.categories != 'Blog post' %}
          <span>
          Based on:
          <a class="button small" href="{{post.paperurl}}">iNSPIRE HEP</a>
          </span>
          <br>
          <span>
          Format: {{post.categories}}
          </span>
          <br>
          <span>Location: {{post.place}}</span>
          <br>
      {% endif %}
      <br>
      <a class="button small" href="{{post.url}}">Read more</a>
    </div>
  </div>
  <hr>
  <p class="bt">
  </p>
  <hr>
{% endfor %}


<div class='four spacing'></div>


