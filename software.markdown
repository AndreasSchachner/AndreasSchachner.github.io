---
layout: page
title: Software
permalink: /software/
---

I develop open-source, JAX-native scientific software for the systematic
exploration of the string landscape. The **StringJAX ecosystem** brings
together a family of interoperating, separately-versioned, separately-citable
Python packages that make the geometry &rarr; effective theory &rarr;
moduli-stabilisation pipeline *fast, differentiable, and reproducible* on
CPU, GPU, or TPU.

## The StringJAX ecosystem

### Packages

- **stringjax** ([GitHub](https://github.com/StringJAX/stringjax) &middot;
  [docs](https://stringjax.readthedocs.io)) &mdash; the umbrella. A thin
  metapackage that pins compatible versions of the member packages and
  routes new users to the right entry point.

- **jaxvacua** ([GitHub](https://github.com/StringJAX/jaxvacua) &middot;
  [docs](https://jaxvacua.readthedocs.io)) &mdash; Type&nbsp;IIB flux-vacuum
  engine. Periods, K&auml;hler potential, GVW superpotential, F-terms, ISD
  samplers and a linearised optimiser, Newton refinement, flux bounding,
  and conifold / coni-LCS limits.

- **stringforge** ([GitHub](https://github.com/StringJAX/stringforge) &middot;
  [docs](https://stringforge.readthedocs.io)) &mdash; data layer. Curated
  Calabi&ndash;Yau geometry databases (TDF / CICY / KKLT) plus the
  persistent vacua vault, served from HuggingFace and cached locally.
  Solver-light: a single `LCSDatabase(...).load_model(...)` call hands you
  a JAXVacua-ready model.

- **jaxpolylog** ([GitHub](https://github.com/StringJAX/jaxpolylog) &middot;
  [docs](https://jaxpolylog.readthedocs.io)) &mdash; JAX-native
  polylogarithms with custom JVPs that survive arbitrary-order autodiff
  down to $|z| \approx 10^{-30}$. Used by `jaxvacua` for worldsheet-instanton
  sums; standalone-useful for anything needing differentiable
  $\mathrm{Li}_s(z)$.

- **stringjax_tools** ([GitHub](https://github.com/StringJAX/stringjax_tools) &middot;
  [docs](https://stringjax-tools.readthedocs.io)) &mdash; shared
  JAX-helpers layer used across the ecosystem: rank-checked auto-vectorisation,
  cached `jit(vmap(...))` wrappers, static-argument JIT helpers, persistent
  compilation-cache setup, and configurable pytree registration for
  stateful model classes. Application-agnostic &mdash; no
  domain-specific conventions leak into the shared helper layer.

### Datasets (HuggingFace)

- [**cy-database**](https://huggingface.co/datasets/aschachner/cy-database)
  &mdash; lazy parquet shards of precomputed Calabi&ndash;Yau threefold
  data, organised as sub-datasets:
  - `tdf/` &mdash; all FRST phases of all double-favourable, trilayer
    polytopes in KS up to $h^{1,1} = 11$, plus GV data and $h^{1,2} = 2$
    conifolds.
  - `cicy/` &mdash; complete-intersection Calabi&ndash;Yau threefolds.
  - `kklt/` &mdash; curated index over TDF matching the working IDs of
    our current de Sitter constructions.

  Catalogues are ~10&nbsp;MB; individual model shards pull on demand via
  `stringforge` or plain `pandas` + `huggingface_hub`.

- [**vacua_vault**](https://huggingface.co/datasets/aschachner/vacua_vault)
  &mdash; community vault of designated flux-vacuum records with
  provenance. Currently scaffolding only; will be populated as members of
  the group submit vetted vacua. Pushed and fetched via
  `stringforge.VacuaWriter` / `LCSDatabase.push_vacua_to_hub`; readable
  as plain parquet for analysis or ML training.

### Status

All five packages are `pip install`-able, GPL-3.0, Python&nbsp;&ge;&nbsp;3.12,
run on CPU and GPU, and ship with quickstart notebooks in the docs. Happy
to demo on a call &mdash; [get in touch](/collaborators/).