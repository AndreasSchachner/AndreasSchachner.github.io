---
layout: page
title: Talks
permalink: /talklist/
---


<div>
    <h4>Some statistics</h4>
        <table>
            <tr>
                <td>Format</td>
                <td>Number</td>
            </tr>
                {% for category in  site.talklist.format%}
                   <tr>
                        <td> category[0] <td>
                        <td> category[1]  <td>
                   </tr>
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
          <a href="#">4 commetns</a>
        </span>-->
      </p>
      <h4><a href="{{ post.url }}">{{ post.title }} </a></h4>
      <span>
      Title: {{post.talktitle}}
      </span>
      <br>
      <br>
      {% if post.preview %}
        <div class='row'>
          <div class='small-6 medium-4 large-4 columns'>
            <img alt="" src="{{site.url}}{{site.baseurl}}/{{post.preview}}" />
          </div>
          <div class='small-6 medium-8 large-8 columns'>
            <p>Abstract: {{post.excerpt}}</p>
          </div>
        </div>
      {% else %}
        <p>Abstract: {{post.excerpt}}</p>
      {% endif %}
      <span>
      Based on:
      <a class="button small" href="{{post.paperurl}}">iNSPIRE HEP</a>
      </span>
      <br>
      <span>
      Format: {{post.format}}
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
      <a class="button small" href="{{site.url}}{{site.baseurl}}/{{post.url}}">Read more</a>
    </div>
  </div>
  <hr>
  <div class='two spacing'></div>
{% endfor %}


<div class='four spacing'></div>



### Conference/workshop talks

* String Phenomenology 2019 (Parallel session):  27.06.2019

### Invited seminar talks

* Bologna 02.07.2021

* Heidelberg 16.12.2019

### Conferences

| Date        | Title        | Type |   Location   |
|:-------------|:------------------|:------|:------|
| 02.07.2021       | Bla  | Seminar talk | Bologna |
|  |    |   |    |
|           |     |   |     |
|           |  |   |    |

### Outreach

* Blog post for the "Accelerate Programme for Scientific Discovery" which can be found under the following link: [acceleratescience](https://acceleratescience.github.io//2021/07/08/Andreas-Schachner-ML-for-string-theory) 
