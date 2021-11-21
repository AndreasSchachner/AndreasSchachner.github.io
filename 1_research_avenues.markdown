---
layout: page
title: Research
permalink: /research/
---
<div style="width: 750px;">
   <p align="justify">
    My research interests include in particular string phenomenology, quantum gravity, cosmology and non-perturbative aspects of QFT. The main argument for the study of string theory remains its potential to explain all natural phenomena, including gravity, within a consistent quantum framework. A central tenet of my research is uncovering novel mechanisms in string theory and its compactifications from methodical analyses of symmetries, dualities and geometries. 
    
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


