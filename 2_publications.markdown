---
layout: page
title: Publications
permalink: /publications/
---

Detailed information about my publications can also be found on
[InspireHEP](https://inspirehep.net/authors/1635387?ui-citation-summary=true).
The list below is generated from the
[`_data/publications.yml`](https://github.com/AndreasSchachner/AndreasSchachner.github.io/blob/master/_data/publications.yml)
data file in this repository; see `inspirehep/scripts/to_publications_yml.py`
in the [`workflows`](https://github.com/AndreasSchachner) repository for the
InspireHEP → YAML migration.

{% assign papers = site.data.publications | sort: "earliest_date" | reverse %}

{% for p in papers %}
**{{ p.title }}**
{% if p.authors.size > 10 %}{% for a in p.authors limit:5 %}{{ a }}{% unless forloop.last %}, {% endunless %}{% endfor %}, *et al.* ({{ p.authors.size }} authors){% else %}{% for a in p.authors %}{{ a }}{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}{% if p.authors.size == 0 %}_authors TBD_{% endif %}{% if p.year %} &middot; {{ p.year }}{% endif %}
{% if p.published %}*{{ p.published }}*{% if p.arxiv or p.doi %} &middot; {% endif %}{% endif %}{% if p.arxiv %}[arXiv:{{ p.arxiv }}](https://arxiv.org/abs/{{ p.arxiv }}){% endif %}{% if p.doi and p.doi != "" %}{% if p.arxiv %} &middot; {% endif %}[DOI:{{ p.doi }}](https://doi.org/{{ p.doi }}){% endif %}{% if p.type == "proceedings" %} &middot; *proceedings*{% elsif p.type == "lectures" %} &middot; *lectures*{% elsif p.type == "thesis" %} &middot; *thesis*{% endif %}

{% endfor %}