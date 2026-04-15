---
layout: page
title: Talks
permalink: /talks/
---

A reverse-chronological list of seminars, colloquia, plenary talks, and
lecture series. Dates follow the DD/MM/YYYY convention.

{% assign today = site.time | date: "%Y-%m-%d" %}
{% assign all_talks = site.data.talks | sort: "date" | reverse %}
{% assign upcoming = all_talks | where_exp: "t", "t.date > today" %}
{% assign past     = all_talks | where_exp: "t", "t.date <= today" %}

{% if upcoming.size > 0 %}
## Upcoming

{% for t in upcoming %}
{%- include talk_entry.html t=t -%}
{% endfor %}
{% endif %}

{% assign section_defs = "invited-plenary:::Invited plenary talks and lectures|lectures:::Lecture series|invited-seminar:::Invited seminars|colloquium:::Colloquia|contributed:::Contributed talks and posters" | split: "|" %}

{% for pair in section_defs %}
  {% assign parts = pair | split: ":::" %}
  {% assign key = parts[0] %}
  {% assign title = parts[1] %}
  {% assign items = past | where: "type", key %}
  {% if items.size > 0 %}

## {{ title }}

{% for t in items %}
{%- include talk_entry.html t=t -%}
{% endfor %}

  {% endif %}
{% endfor %}