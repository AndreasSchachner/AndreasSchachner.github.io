---
layout: page
title: Research
permalink: /research/
---

My research lies at the interface of string theory, quantum gravity, and
machine learning, with an emphasis on explicit constructions of string
compactifications and the systematic extraction of low-energy information
from them. I develop mathematical and computational tools to probe the
landscape of string vacua, characterise the four-dimensional effective
theories obtained by compactification, and confront them with cosmological
and laboratory data. A central guiding question is whether string theory
admits controlled, phenomenologically viable vacua &mdash; and what
structural constraints the theory itself imposes on them.

The sections below describe the principal threads of my work.

<nav class="research-toc" aria-label="Research avenues">
  <ul>
    <li><a href="#moduli-stabilisation">String compactifications and moduli stabilisation</a></li>
    <li><a href="#de-sitter-vacua">de Sitter vacua in string theory</a></li>
    <li><a href="#higher-derivative">Higher-derivative corrections</a></li>
    <li><a href="#axiverse">Axions, the axiverse, and fundamental cosmology</a></li>
    <li><a href="#computational-ai">Computational string theory and AI for HEP-TH</a></li>
  </ul>
</nav>

---

## String compactifications and moduli stabilisation {#moduli-stabilisation}

<!-- figure: TBD -->

A central theme of my research is the construction and systematic study of
four-dimensional effective field theories obtained from string
compactifications, with a particular focus on Type&nbsp;IIB orientifolds and
their vacuum structure. The guiding question is whether &mdash; and how
&mdash; the enormous degeneracies of the string landscape give rise to
controlled, phenomenologically viable theories.

### Moduli stabilisation with explicit data

Concrete progress on moduli stabilisation typically requires both new
analytic ingredients and explicit Calabi&ndash;Yau data. In
[arXiv:2109.14624](https://arxiv.org/abs/2109.14624) I developed, with
collaborators, the systematics of Type&nbsp;IIB moduli stabilisation in the
presence of odd 2-form axions, yielding an efficient analytic handle on
models with fully stabilised moduli. To populate such constructions with
explicit compactification data, we compiled a large database of
Calabi&ndash;Yau orientifolds and their D3-tadpole budgets in
[arXiv:2204.13115](https://arxiv.org/abs/2204.13115).

### Flux vacua at scale

Numerical flux-vacuum searches expose the structure of the landscape far
beyond what analytic methods alone can reach. I constructed new
non-supersymmetric flux vacua in
[arXiv:2308.15525](https://arxiv.org/abs/2308.15525), carried out deep
numerical observations of the Type&nbsp;IIB flux landscape in
[arXiv:2501.03984](https://arxiv.org/abs/2501.03984), and showed in
[arXiv:2507.00615](https://arxiv.org/abs/2507.00615) that numerical
K&auml;hler moduli stabilisation can give rise to coexisting flux string
vacua within a single compactification &mdash; a feature invisible to
analytic approximations.

### Ongoing directions

- Scaling flux-vacuum searches to full Calabi&ndash;Yau ensembles with
  differentiable, GPU-ready samplers.
- Combining moduli stabilisation with realistic particle phenomenology in
  explicit Type&nbsp;IIB compactifications.
- Quantifying how higher-derivative and loop corrections deform the vacuum
  structure extracted at tree level.

---

## de Sitter vacua in string theory {#de-sitter-vacua}

<figure class="avenue-figure">
  <img src="{{ '/images/research/de-sitter-fig1.png' | relative_url }}"
       alt="Candidate de Sitter vacuum: anti-D3-brane uplift from a supersymmetric AdS vacuum (KKLT scenario), and the scalar potentials of the resulting de Sitter and anti-de Sitter vacua in an explicit Calabi–Yau orientifold flux compactification">
  <figcaption>
    Fig. 1 from <a href="https://arxiv.org/abs/2406.13751"
    target="_blank" rel="noopener">arXiv:2406.13751</a>. <em>Top:</em> outcomes of anti-D3-brane uplift from a supersymmetric AdS vacuum in the KKLT scenario. <em>Bottom:</em> scalar potentials of the AdS (black) and dS (pink) vacua in the Calabi&ndash;Yau flux compactification.
  </figcaption>
</figure>

Explaining the observed accelerated expansion of the Universe within a
UV-complete theory of quantum gravity is one of the central open problems
in string phenomenology. Whether controlled de Sitter vacua exist in
string theory remains an active and contested question. My work aims both
to construct explicit candidate vacua and to subject them to increasingly
stringent consistency checks.

### Candidate vacua

In [arXiv:2406.13751](https://arxiv.org/abs/2406.13751) I presented, with
Liam McAllister, Jakob Moritz, and Richard Nally, explicit candidate de
Sitter vacua in a concrete Type&nbsp;IIB compactification, assembling the
required ingredients &mdash; fluxes, non-perturbative effects, and an
uplift sector &mdash; within a single controlled construction. A short
companion overview is available as
[arXiv:2505.00149](https://arxiv.org/abs/2505.00149).

### Uplifts, warping, and pedagogy

In [arXiv:2512.17995](https://arxiv.org/abs/2512.17995) I examined the role
of warping in effective potentials relevant for F-term uplifting,
clarifying under which conditions the standard approximations used in
KKLT-type constructions remain reliable. A pedagogical treatment of the
subject appears in the TASI&nbsp;2025 lectures
[arXiv:2512.17095](https://arxiv.org/abs/2512.17095), co-authored with Liam
McAllister.

### Connecting to phenomenology

A recurring motivation is that a de Sitter solution is useful only once it
coexists with realistic particle physics. This was the guiding question in
[arXiv:2106.11964](https://arxiv.org/abs/2106.11964), where we embedded a
Standard-Model-like quiver gauge theory in de-Sitter-compatible
Type&nbsp;IIB compactifications.

### Ongoing directions

- Stress-testing candidate constructions against higher-derivative and
  loop corrections.
- Large-scale searches for consistent uplift sectors across explicit
  Calabi&ndash;Yau ensembles.
- Clarifying the role of warping and non-perturbative effects in the
  four-dimensional effective potential.

---

## Higher-derivative corrections {#higher-derivative}

<figure class="avenue-figure">
  <img src="{{ '/images/research/higher-derivative-fig3.png' | relative_url }}"
       alt="h^3 phi^2 amplitude: diagrams contributing to the five-point closed-string amplitude at eight derivatives, with intermediate exchange channels (in blue) to be subtracted to isolate the contact term">
  <figcaption>
    Fig. 3 from <a href="https://arxiv.org/abs/2507.07934"
    target="_blank" rel="noopener">arXiv:2507.07934</a>. The
    <em>h</em><sup>3</sup><em>&phi;</em><sup>2</sup> amplitude; diagrams in blue indicate poles to be subtracted.
  </figcaption>
</figure>

Extracting reliable low-energy information from string compactifications
requires a detailed understanding of the UV sensitivity of the resulting
effective field theories. Systematically deriving corrections to the
tree-level string actions &mdash; and tracking their impact under
dimensional reduction &mdash; therefore sits at the heart of string
phenomenology.

### &alpha;&prime; corrections in F-theory and Type IIB

In [arXiv:2106.04592](https://arxiv.org/abs/2106.04592) I studied the
systematics of the &alpha;&prime; expansion in F-theory and its
consequences for four-dimensional effective potentials, with direct
implications for moduli-stabilisation scenarios of KKLT and LVS type.

### Type IIB at eight derivatives

A sustained line of work concerns the eight-derivative sector of Type&nbsp;IIB
superstring theory. In
[arXiv:2205.11530](https://arxiv.org/abs/2205.11530) I combined inputs
from superstrings, superfields, and superparticles to constrain terms at
this order. In [arXiv:2507.07934](https://arxiv.org/abs/2507.07934) the
analysis was extended to five-point axio-dilaton couplings, uncovering
additional structure in the effective action consistent with what
superspace methods anticipate.

### Ongoing directions

- Closing the gap between the low-point couplings accessed via amplitudes
  and the full nonlinear structure at eight derivatives.
- Tracking the impact of these corrections on controlled four-dimensional
  vacua, in particular for de Sitter constructions and Calabi&ndash;Yau
  flux compactifications.
- Extending the systematics to terms involving the 3-form
  <strong>G</strong><sub>3</sub> and 1-form <strong>P</strong><sub>1</sub>
  of Type&nbsp;IIB, where superspace methods suggest a rich but largely
  unexplored ordering principle.

---

## Axions, the axiverse, and fundamental cosmology {#axiverse}

<figure class="avenue-figure avenue-figure--pair">
  <img src="{{ '/images/research/axiverse-fig19-left.png' | relative_url }}"
       alt="Marginalized posterior distribution of axion mass m_a and axion dark-matter fraction Omega_a / Omega_DM, with 68% and 95% credible regions shown">
  <img src="{{ '/images/research/axiverse-fig19-right.png' | relative_url }}"
       alt="Marginalized posterior distribution of the axion decay constant f_a, comparing a Calabi–Yau sampling analysis to an EFT analysis with a single ultralight axion">
  <figcaption>
    Fig. 19 from <a href="https://arxiv.org/abs/2512.00144"
    target="_blank" rel="noopener">arXiv:2512.00144</a>. <em>Left:</em> joint posterior for the axion mass and DM fraction. <em>Right:</em> posterior for the decay constant <em>f<sub>a</sub></em>. Dark/light contours indicate 68% and 95% credible regions.
  </figcaption>
</figure>

String compactifications generically predict a rich spectrum of axion-like
particles spanning many orders of magnitude in mass and coupling &mdash;
the so-called *axiverse*. This makes axions a privileged messenger between
the string landscape and observation, and one of the cleanest ways to
confront explicit compactifications with cosmological and laboratory data.

### Fuzzy axions and the string axiverse

In [arXiv:2412.12012](https://arxiv.org/abs/2412.12012) I studied fuzzy
axion dark matter arising from string compactifications and the associated
cosmological relics. A compact presentation appears in the
COSMIC&nbsp;WISPers&nbsp;2024 proceedings
[arXiv:2502.02256](https://arxiv.org/abs/2502.02256).

### Confronting string theory with data

Turning axiverse predictions into falsifiable statements requires both
large-scale computations of string-theoretic spectra and rigorous
statistical inference. In
[arXiv:2512.00144](https://arxiv.org/abs/2512.00144) I performed Bayesian
inference on Calabi&ndash;Yau moduli spaces, constraining axiverse
parameters directly from experimental data. The wider phenomenological
context of weakly-interacting slim particles is summarised in the
COSMIC&nbsp;WISPers white paper
[arXiv:2603.03433](https://arxiv.org/abs/2603.03433).

### Gravitational-wave signatures of BSM physics

Related to the axiverse, and to fundamental cosmology more broadly, is the
question of what gravitational-wave signals can teach us about physics
beyond the Standard Model. In
[arXiv:2303.01548](https://arxiv.org/abs/2303.01548) I explored how
gravitational waves &mdash; in particular at high frequencies &mdash; can
be used to test BSM scenarios motivated by string compactifications.

### Ongoing directions

- Extending axiverse predictions to realistic ensembles of
  Calabi&ndash;Yau compactifications using differentiable pipelines.
- Sharpening the statistical comparison between string-theoretic axion
  spectra and cosmological / laboratory constraints.
- Building the connection between moduli stabilisation, de Sitter
  construction, and the resulting axion phenomenology in a single
  controlled framework.

---

## Computational string theory and AI for HEP-TH {#computational-ai}

<figure class="avenue-figure">
  <img src="{{ '/images/research/computational-fig3.png' | relative_url }}"
       alt="DNA of Calabi–Yau hypersurfaces: structural invariants extracted from a large ensemble of Calabi–Yau threefolds that can be exploited by machine-learning methods for fast classification and navigation of the landscape">
  <figcaption>
    Fig. 3 from <a href="https://arxiv.org/abs/2405.08871"
    target="_blank" rel="noopener">arXiv:2405.08871</a> (<em>The DNA of Calabi&ndash;Yau hypersurfaces</em>).
  </figcaption>
</figure>

The string landscape is a combinatorially vast and computationally hard
object: estimates of its size range from
[10<sup>500</sup>](https://iopscience.iop.org/article/10.1088/1126-6708/2004/01/060)
to
[10<sup>272&thinsp;000</sup>](https://link.springer.com/article/10.1007%2FJHEP12%282015%29164)
vacua, and finding solutions with prescribed phenomenological properties
appears to be NP-hard in general. A sustained thread of my work is to
address this challenge with a combination of large-scale computation and
modern machine learning &mdash; not ML for its own sake, but as a
principled acceleration of physics pipelines.

### Search algorithms for the landscape

Early work demonstrated that search-based learning can find flux vacua in
regimes where systematic enumeration is infeasible &mdash; see
[arXiv:1907.10072](https://arxiv.org/abs/1907.10072) (genetic algorithms)
and the NeurIPS&nbsp;2021 ML4PS proceedings
[arXiv:2111.11466](https://arxiv.org/abs/2111.11466) on reinforcement
learning and genetic algorithms for flux vacua.

### Differentiable physics and JAX-native pipelines

In [arXiv:2306.06160](https://arxiv.org/abs/2306.06160) I introduced
**JAXVacua**, a JAX-based framework for sampling string vacua that exposes
flux-vacuum potentials as smooth, differentiable loss surfaces amenable to
gradient-based optimisation and ML composition. The same infrastructure
underpins the large-scale studies in
[arXiv:2501.03984](https://arxiv.org/abs/2501.03984).

### Generative and representational approaches

Probing flux-vacuum distributions with generative methods was the subject
of [arXiv:2307.15749](https://arxiv.org/abs/2307.15749) (*W&#8320;_sample =
np.random.normal(0,1)?*). More recently,
[arXiv:2603.04941](https://arxiv.org/abs/2603.04941) studied parameter
compression in the flux landscape, probing the intrinsic dimensionality of
the vacuum data.

### Machine learning meets Calabi&ndash;Yau geometry

On the geometric side,
[arXiv:2310.06820](https://arxiv.org/abs/2310.06820) addressed counting
problems for Calabi&ndash;Yau threefolds, and
[arXiv:2405.08871](https://arxiv.org/abs/2405.08871) (*The DNA of
Calabi&ndash;Yau hypersurfaces*) uncovered structural invariants that ML
methods can exploit for fast classification and navigation of the
landscape.

### Teaching and community

I have delivered a lecture series on *Machine Learning Techniques in the
String Landscape* at the
[XX&nbsp;Avogadro&nbsp;Meeting](https://agenda.infn.it/event/42186/) &mdash;
materials on
[GitHub](https://github.com/AndreasSchachner/ml-string-landscape) &mdash;
and I supervise student projects at the LMU AI Lab on neural-network
methods for PDEs in physics.

### Ongoing directions

- Scaling differentiable flux-vacuum searches to full Calabi&ndash;Yau
  ensembles on GPU / TPU hardware.
- Coupling JAX-native physics pipelines to surrogate and generative ML
  models for high-dimensional moduli spaces.
- Public releases under the
  [ASchachnerGroup](https://github.com/ASchachnerGroup) GitHub
  organisation.

---

If you would like to hear more about any of these directions, or are
interested in collaborating on the software stack behind them, please
[get in touch](/collaborators/).

<style>
.research-toc {
  margin: 1.5rem 0 2rem;
  padding: 0.9rem 1.1rem;
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 8px;
  font-size: 0.93rem;
}
.research-toc ul {
  list-style: none;
  padding-left: 0;
  margin: 0;
}
.research-toc li {
  margin-bottom: 0.15rem;
}
.research-toc a { color: #0969da; }

h2[id] { scroll-margin-top: 1rem; }

.avenue-figure {
  margin: 1.25rem 0 1.5rem;
  padding: 0.5rem;
  border: 1px solid #eaeef2;
  border-radius: 6px;
  background: #fff;
  text-align: center;
}
.avenue-figure img {
  max-width: 100%;
  height: auto;
  display: block;
  margin: 0 auto;
}
.avenue-figure--pair {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  justify-content: center;
  align-items: center;
}
.avenue-figure--pair img {
  flex: 1 1 260px;
  min-width: 0;
}
.avenue-figure--pair figcaption {
  flex-basis: 100%;
}
.avenue-figure figcaption {
  color: #57606a;
  font-size: 0.85rem;
  margin-top: 0.5rem;
  padding: 0 0.25rem;
  text-align: left;
}
</style>