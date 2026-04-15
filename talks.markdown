---
layout: page
title: Talks
permalink: /talks/
---

A reverse-chronological list of seminars, colloquia, plenary talks, and
lecture series. Dates follow the DD/MM/YYYY convention.

{%- comment -%}
Render helpers:
- `today` comparison uses the ISO date string from the data file so the
  page never needs regenerating for a date rollover.
- Types map to human-readable section titles.
{%- endcomment -%}

{% assign today = site.time | date: "%Y-%m-%d" %}
{% assign all_talks = site.data.talks | sort: "date" | reverse %}

{% assign upcoming = "" | split: "" %}
{% assign past     = "" | split: "" %}
{% for t in all_talks %}
  {% if t.date > today %}
    {% assign upcoming = upcoming | push: t %}
  {% else %}
    {% assign past = past | push: t %}
  {% endif %}
{% endfor %}

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