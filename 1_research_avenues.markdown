---
layout: page
title: Research
permalink: /research/
---
<div style="width: 750px;">
   <p align="justify">
    My research interests lie primarily in string phenomenology, quantum gravity, cosmology, and the non-perturbative aspects of quantum field theory. The enduring motivation for studying string theory is its unique potential to provide a consistent quantum framework that unifies all fundamental interactions, including gravity. A central focus of my work is to uncover novel mechanisms within string theory and its compactifications, achieved through systematic analyses of symmetries, dualities, and underlying geometrical structures.
    
    </p>
</div>
<br>



The list below gives a more detailed account of my research interests:

{% for themes in site.research_avenues %}

<a href="{{ themes.url | prepend: site.baseurl }}">
    {{ themes.title }}
</a>

<p class="post-excerpt">{{ themes.description | truncate: 160 }}</p>

{% endfor %}

If you are interested in hearing more about my research, please do not hesitate to get in touch.


