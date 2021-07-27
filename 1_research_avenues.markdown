---
layout: page
title: Research
permalink: /research/
---

My research interests include in particular string phenomenology, quantum gravity, cosmology and non-perturbative aspects of QFT. Specifically, I am currently working on higher-derivative corrections in string theory and their effects on EFTs from compactifications to lower dimensions. Moreover, I study vacuum transitions in field theories with gravity and their implications on early universe cosmology. In a different context, I apply methods from Machine Learning, Search Optimisation and Topological Data Analysis to study the landscape of string theory vacua.

The list below gives a more detailed account of my research interests:

{% for themes in site.research_avenues %}

<a href="{{ themes.url | prepend: site.baseurl }}">
    {{ themes.title }}
</a>

<p class="post-excerpt">{{ themes.description | truncate: 160 }}</p>

{% endfor %}

If you are interested in hearing more about my research, please do not hesitate to get in touch.


