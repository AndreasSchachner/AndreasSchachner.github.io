---
layout: page
title: Publications
permalink: /publications/
---

Detailed information about my publications can also be found on
[InspireHEP](https://inspirehep.net/authors/1635387?ui-citation-summary=true).

{% include coauthor_graph.html %}

{% assign papers = site.data.publications | sort: "earliest_date" | reverse %}
{% assign current_year = "" %}

{% for p in papers %}
{%- assign paper_year = p.earliest_date | slice: 0, 4 -%}
{%- if paper_year != current_year %}

### {{ paper_year }}

{% assign current_year = paper_year -%}
{% endif -%}
**{{ p.title }}**{% if p.published %} &middot; *{{ p.published }}*{% endif %}{% if p.arxiv %} &middot; [arXiv:{{ p.arxiv }}](https://arxiv.org/abs/{{ p.arxiv }}){% endif %}{% if p.doi and p.doi != "" %} &middot; [DOI:{{ p.doi }}](https://doi.org/{{ p.doi }}){% endif %}{% if p.type == "proceedings" %} &middot; *proceedings*{% elsif p.type == "lectures" %} &middot; *lectures*{% elsif p.type == "thesis" %} &middot; *thesis*{% endif %}<br><small>{% if p.authors.size > 10 %}{% for a in p.authors limit:5 %}{{ a }}{% unless forloop.last %}, {% endunless %}{% endfor %}, *et al.* ({{ p.authors.size }} authors){% else %}{% for a in p.authors %}{{ a }}{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}{% if p.authors.size == 0 %}_authors TBD_{% endif %}</small>

{% endfor %}