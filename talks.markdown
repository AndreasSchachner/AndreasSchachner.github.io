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

    

{%  for post in site.talklist reversed %}
  <div class='big mod modBlogPost no_bg'>
    <div class='content'>
    
     {% assign currentdate = post.date | date: "%Y" %}
     {% if currentdate != date %}
        <br>
        <br>
        <br>
        <h1><span>{{ post.date | date: '%Y' }}</span></h1>
        <hr>
        {% assign date = currentdate %} 
     {% endif %}

      <p class='info'>
       <!-- /
        <span>
          <a href="#">4 comments</a>
        </span>-->
      </p>
      <h4><a href="{{post.eventurl}}">{{ post.title }} </a></h4>
      <span>
      Title: {{post.talktitle}}
      </span>
      <br>
      <span>
      Based on:
      <a class="button small" href="{{post.paperurl}}">iNSPIRE HEP</a>
      </span>
      <br>
      <span>
      Format: {{post.categories}}
      </span>
      <br>
      <span>
      Event website:
      <a class="button small" href="{{post.eventurl}}">{{post.title}}</a>
      </span>
      <br>
      <span>Date: {{post.date | date: "%B %d, %Y" }}</span>
      <br>
      <span>Location: {{post.place}}</span>
      <br>
      <br>
      <div class='spacing'></div>
      <a class="button small" href="{{post.url}}">Read more</a>
    </div>
  </div>
  <hr>
  <div class='two spacing'></div>
{% endfor %}


<div class='four spacing'></div>




### Outreach

* Blog post for the "Accelerate Programme for Scientific Discovery" which can be found under the following link: [acceleratescience](https://acceleratescience.github.io//2021/07/08/Andreas-Schachner-ML-for-string-theory) 
