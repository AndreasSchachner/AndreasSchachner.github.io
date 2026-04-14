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

{%- comment -%}
Ordered list of (cluster-key, section-title) pairs.
Clusters with no entries are skipped silently.
{%- endcomment -%}
{% assign section_defs = "flux-moduli:::Flux vacua and moduli stabilisation|de-sitter:::de Sitter vacua in string theory|higher-derivative:::Higher-derivative corrections (α′ and g_s)|axions-axiverse:::Axions, the axiverse, and WISPs|ml-computational:::Machine learning and computational methods|cy-geometry:::Calabi–Yau geometry and counting|gw-bsm:::Gravitational waves and BSM|early-qft:::Early / QFT work|lectures-reviews:::Lectures and reviews|thesis:::Thesis" | split: "|" %}

{% for pair in section_defs %}
  {% assign parts = pair | split: ":::" %}
  {% assign cluster_key = parts[0] %}
  {% assign section_title = parts[1] %}
  {% assign papers = site.data.publications | where: "cluster", cluster_key | sort: "earliest_date" | reverse %}
  {% if papers.size > 0 %}

### {{ section_title }}

{% for p in papers %}
**{{ p.title }}**
{% for a in p.authors %}{{ a }}{% unless forloop.last %}, {% endunless %}{% endfor %}{% if p.authors.size == 0 %}_authors TBD_{% endif %}{% if p.year %} &middot; {{ p.year }}{% endif %}
{% if p.published %}*{{ p.published }}*{% if p.arxiv or p.doi %} &middot; {% endif %}{% endif %}{% if p.arxiv %}[arXiv:{{ p.arxiv }}](https://arxiv.org/abs/{{ p.arxiv }}){% endif %}{% if p.doi and p.doi != "" %}{% if p.arxiv %} &middot; {% endif %}[DOI:{{ p.doi }}](https://doi.org/{{ p.doi }}){% endif %}{% if p.type == "proceedings" %} &middot; *proceedings*{% elsif p.type == "lectures" %} &middot; *lectures*{% elsif p.type == "thesis" %} &middot; *thesis*{% endif %}
{% if p.also.size > 0 %}<small>Also: {% for c in p.also %}{{ c }}{% unless forloop.last %}, {% endunless %}{% endfor %}.</small>{% endif %}

{% endfor %}

  {% endif %}
{% endfor %}