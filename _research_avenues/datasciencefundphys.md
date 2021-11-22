---
title: Data Science and Fundamental Physics
layout: page
description: 
---

<div style="width: 750px;">
   <p align="justify">

    While the string landscape encompasses a vast number of low energy effective field theories, only a small subset of them are phenomenologically viable. The landscape's enormity, with as many as <a href="https://link.springer.com/article/10.1007%2FJHEP12%282015%29164" target="_blank"><i>10<sup>272,000</sup></i></a> vacua, makes exhaustive searches or random samplings impractical. While in simple string models <i>generic</i> solutions may be found easily, practicioners usually seek to construct solutions having special properties such as weak couplings to ensure theoretical control or similarity to our universe. These additional criteria impose an auxiliary landscape structure (i.e. optimisation target) for which constrained systems of equations must be solved. For this problem, the landscape's vastness is exacerbated by computational complexity; finding specific string vacua appears to be <a href="https://www.sciencedirect.com/science/article/abs/pii/S0003491606001382?via%3Dihub" target="_blank"><i>NP-hard</i></a>, though for some toy examples <a href="https://journals.aps.org/prd/abstract/10.1103/PhysRevD.96.103512" target="_blank"><i>heuristic algorithms</i></a> may have success. On this level, the situation of the string landscape is comparable to <a href="https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.35.1792" target="_blank"><i>spin-glass systems</i></a> and <a href="https://link.springer.com/article/10.1007/BF02460703" target="_blank"><i>protein folding</i></a>.
    
    </p>
</div>
<br>


<div style="width: 750px;">
   <p align="justify">
    A key objective of my future work is to develop a systematic framework to constructing string vacua utilising the impressive machinary of <i>Artificial Intelligene</i> (AI) and <i>Data Science</i> (DS) techniques.
    
    
    Building upon that, I explore the effectiveness of such strategies in revealing universal correlations among UV parameters characterising the local structure in the landscape. Recall that, since in String Theory the value of couplings is set by vacuum expectation values of fields, these are highly non-trivial and much sought-after insights. Moreover, combinations of supervised and unsupervised <i>Machine Learning</i> (ML) methods are prerequisites to determine boundaries of physical parameter spaces which is particularly attractive in the context of the landscape-swampland program.

    </p>
</div>
<br>

### Search for suitable Calabi-Yau orentifolds

<div style="width: 750px;">
   <p align="justify">
    Among others, I explore the set of Calabi-Yau hypersurfaces in the <a href="http://hep.itp.tuwien.ac.at/~kreuzer/CY/" target="_blank"><i>Kreuzer-Skarke database</i></a> using the <a href="https://cytools.liammcallistergroup.com" target="_blank"><i>CYTools</i></a> software package. For instance, we favour compact geometries that are capable of hosting realistic particle phenomenologies and whose string spectra satisfy bounds from black hole superradiance. However, the issue of efficiently finding background geometries for viable N=1 string compactifications remains largely unexplored. Here, I am interested in developing innovative strategies to obtaining orientifold and D-brane configurations of maximal D3-charge as well as suitable divisor structures with sufficiently many invariant rigid divisors supporting non-perturbative effects for moduli stabilisation. We have merely scratched the surface 
    </p>
</div>
<br>

### Search for fully-stabilised string vacua

<div style="width: 750px;">
   <p align="justify">
   Given a background geometry together with an O-plane/D-brane configuration with vanishing tadpoles (i.e. satisfying generalised Gauß' law constraints), a fully-consistent EFT requires the specification of further UV parameters such as fluxes. More generally, the dynamics of the low energy theory needs to be analysed to find vacua with fully stabilised moduli. It remains a top challenge to design efficient optimization methods to search for realistic vacua that may at the same time reveal hidden structure in the landscape. Regarding this latter point, string theorists are interested not only in the construction of realistic vacua but also the statistical distribution surrounding such vacua, which has implications for <a href="https://iopscience.iop.org/article/10.1088/1126-6708/2004/05/072" target="_blank"><i>various dynamics-based proposals for the measure problem</i></a>. In recent years, stochastic optimisation with <a href="https://link.springer.com/article/10.1007%2FJHEP11%282019%29045" target="_blank"><i>Genetic Algorithms</i></a> (GAs) and <a href="https://arxiv.org/pdf/2107.04039.pdf" target="_blank"><i>Reinforcement Learning</i></a> (RL) have been utilised to search for viable string vacua, outperforming searches based on <a href="https://en.wikipedia.org/wiki/Metropolis–Hastings_algorithm" target="_blank"><i>Metropolis-Hastings</i></a>.
    </p>
</div>

<style>
figure {
  display: inline-block;
  text-align: center;
  margin: 100px; 
}
figure img {
  vertical-align: top;
}
figure figcaption {
  text-align: center;
}

</style>

<HTML>
<BODY>
    <figure>
        <IMG SRC="images/GA_tsne.gif" width="120%" height="auto">
        <figcaption class="figure-caption text-center">Visualisation of GA searches for flux vacua via dimensional reduction using <a href="https://en.wikipedia.org/wiki/T-distributed_stochastic_neighbor_embedding" target="_blank"><i>t-SNE</i></a>. Starting from a random sample of vacua, the GA detects solutions satisfying special search criteria such as small string coupling g<sub>s</sub>. This is highlighted by the color coding characterising the distance to the optimal solution with blue (red) indicating vacua small (large) distances. Initially, the search leads to many intermediate clusters corresponding to local minima of the fitness function before the population settles to an optimal locus in moduli space. This is visualised by the formation of large clusters of dark blue color in t-SNE.</figcaption>
    </figure>
</BODY>
</HTML>
