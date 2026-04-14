---
title: Computational string theory and AI for HEP-TH
layout: page
description: Large-scale computation and modern machine learning as tools for exploring the string landscape — differentiable physics pipelines, surrogate models, and generative methods.
---

<div style="width: 750px;">
   <p align="justify">
    The string landscape is a combinatorially vast and computationally
    hard object: estimates of its size range from
    <a href="https://iopscience.iop.org/article/10.1088/1126-6708/2004/01/060" target="_blank">10<sup>500</sup></a>
    to <a href="https://link.springer.com/article/10.1007%2FJHEP12%282015%29164" target="_blank">10<sup>272000</sup></a>
    vacua, and finding solutions with prescribed phenomenological properties
    appears to be <i>NP-hard</i> in general. A sustained thread of my work
    is to address this challenge with a combination of large-scale
    computation and modern machine learning &mdash; not ML for its own
    sake, but as a principled acceleration of physics pipelines.
   </p>
</div>
<br>

### Search algorithms for the landscape

<div style="width: 750px;">
   <p align="justify">
    Early work demonstrated that search-based learning can find flux vacua
    in regimes where systematic enumeration is infeasible &mdash; see
    <a href="https://arxiv.org/abs/1907.10072" target="_blank">arXiv:1907.10072</a>
    (genetic algorithms) and the ML4PS NeurIPS&nbsp;2021 proceedings
    <a href="https://arxiv.org/abs/2111.11466" target="_blank">arXiv:2111.11466</a>
    on reinforcement learning and genetic algorithms for flux vacua.
   </p>
</div>
<br>

### Differentiable physics and JAX-native pipelines

<div style="width: 750px;">
   <p align="justify">
    In <a href="https://arxiv.org/abs/2306.06160" target="_blank">arXiv:2306.06160</a>
    we introduced <b>JAXVacua</b>, a JAX-based framework for sampling string
    vacua that exposes flux-vacuum potentials as smooth, differentiable loss
    surfaces amenable to gradient-based optimisation and ML composition. The
    same infrastructure underpins the large-scale studies in
    <a href="https://arxiv.org/abs/2501.03984" target="_blank">arXiv:2501.03984</a>
    and is the computational backbone of the software ecosystem described
    on the <a href="{{ '/software/' | relative_url }}">Software</a> page.
   </p>
</div>
<br>

### Generative and representational approaches

<div style="width: 750px;">
   <p align="justify">
    Probing flux-vacuum distributions with generative methods was the
    subject of
    <a href="https://arxiv.org/abs/2307.15749" target="_blank">arXiv:2307.15749</a>
    (<i>W&#8320;_sample = np.random.normal(0,1)?</i>). More recently,
    <a href="https://arxiv.org/abs/2603.04941" target="_blank">arXiv:2603.04941</a>
    studied parameter compression in the flux landscape, probing the
    intrinsic dimensionality of the vacuum data.
   </p>
</div>
<br>

### Machine learning meets Calabi&ndash;Yau geometry

<div style="width: 750px;">
   <p align="justify">
    On the geometric side,
    <a href="https://arxiv.org/abs/2310.06820" target="_blank">arXiv:2310.06820</a>
    addressed counting problems for Calabi&ndash;Yau threefolds, and
    <a href="https://arxiv.org/abs/2405.08871" target="_blank">arXiv:2405.08871</a>
    ("The DNA of Calabi&ndash;Yau hypersurfaces") uncovered structural
    invariants that ML methods can exploit for fast classification and
    navigation of the landscape.
   </p>
</div>
<br>

### Teaching and community

<div style="width: 750px;">
   <p align="justify">
    I have delivered a lecture series on
    <i>Machine Learning Techniques in the String Landscape</i> at the
    <a href="https://agenda.infn.it/event/42186/" target="_blank">XX Avogadro Meeting</a>
    &mdash; materials on
    <a href="https://github.com/AndreasSchachner/ml-string-landscape" target="_blank">GitHub</a>
    &mdash; and I supervise student projects at the LMU AI Lab (SoSe
    2024/25) on neural-network methods for PDEs in physics.
   </p>
</div>
<br>

### Ongoing directions

<div style="width: 750px;">
<ul>
<li>Scaling differentiable flux-vacuum searches to full
    Calabi&ndash;Yau ensembles on GPU/TPU hardware.</li>
<li>Coupling JAX-native physics pipelines to surrogate and generative
    ML models for high-dimensional moduli spaces.</li>
<li>Public releases under the
    <a href="https://github.com/ASchachnerGroup" target="_blank">ASchachnerGroup</a>
    GitHub organisation &mdash; see the
    <a href="{{ '/software/' | relative_url }}">Software</a> page.</li>
</ul>
</div>