---
layout: page
title: Talks
permalink: /talklist/
---


### <b> Summary </b>

<div>
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
                      <td> {{post.categories}}s </td>
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
       margin-bottom: -0.6cm;
  }
</style>

<style>
  .right{
       text-align: right;
       margin-top: -0.6cm;
  }
</style>



<br>
<br>

{% assign blog = "Blog post" %}
{% assign total = 0 %}

### <b> List of talks, posters and seminars </b>

{%  for post in site.talklist reversed %}
  <div class='big mod modBlogPost no_bg'>
    <div class='content'>
    
     {% assign currentdate = post.date | date: "%Y" %}
     {% if currentdate != date %}
        {% if total!=0 %}
            <br>
            <br>
        {% endif %}
        <h1><span>{{ post.date | date: '%Y' }}</span></h1>
        <hr>
        {% assign date = currentdate %} 
        {% assign total = total | plus: 1 %}
     {% endif %}
     
     <p class="rightbm">
      {{post.date | date: "%B %d, %Y" }}
     </p>
      <p class="bo">
       <a href="{{post.eventurl}}">{{ post.title }} </a>
      </p>
      <span>
        Title: <a class="button small" href="{{post.url}}">{{post.talktitle}}</a>
      </span>
      <br>
      <span>
        Format: {{post.categories}} ({{post.length}})
      </span>
      <br>
      <br>
    </div>
  </div>
  <hr>
{% endfor %}


<div class='four spacing'></div>


