---
layout: page
title: Timeline
permalink: /timeline/
---

### TEST:

{% assign steps = site.timestamps | sort: 'date' %}
{% for step in steps %}
<div class="item">
    <i class="vertical-line"></i>
    <h2 class="item-date">{{ step.date | date: '%m/%Y' }}{% if step.enddate %} - {{ step.enddate | date: '%m/%Y' }}{% endif %}</h2>
    <div class="card-panel">
        <h3 class="card-title">
            {{ step.title }}
        </h3>
        <p>
            {{ step.content }}
        </p>
    </div>
</div>
{% endfor %}

