---
layout: page
title: Research
permalink: /research/
---

My research interests include in particular string phenomenology, quantum gravity, cosmology and non-perturbative aspects of QFT. Currently, I am working on constructing local effective actions from string theory including higher derivative and string loop corrections in 10 dimensions. Further, I am interested in understanding the systematics of Calabi-Yau orientifold compactifications, in particular an SL(2,Z) invariant framework. This includes the derivation of novel N=1 quantum corrections to the 4-dimensional effective action. Moreover, I study vacuum transitions in field theories with gravity and their implications on early universe cosmology. In a different context, I apply methods from Machine Learning, Search Optimisation and Topological Data Analysis to study the landscape of string theory vacua.




The list below gives a more detailed account of my research interests:

{% for themes in site.research_avenues %}

<a href="{{ themes.url | prepend: site.baseurl }}">
    {{ themes.title }}
</a>

<p class="post-excerpt">{{ themes.description | truncate: 160 }}</p>

{% endfor %}

If you are interested in hearing more about my research, please do not hesitate to get in touch.


