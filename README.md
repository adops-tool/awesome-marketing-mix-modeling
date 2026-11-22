<div align="center">

[![awesome-marketing-mix-modeling](image/awesome-marketing-mix-modeling.png)](https://github.com/adops-tool/awesome-marketing-mix-modeling/pulls)

[![animated-line](https://github.com/readme-SVG/animated-line/blob/main/STORAGE/line-svg-3D444D.svg)](https://github.com/readme-SVG/animated-line) <!-- -SVG-Line- -->

**A curated list of open-source tools, foundational research, and public datasets for marketing mix modeling (MMM) — built for causal, privacy-durable measurement of marketing effectiveness.**

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)

</div>

> Each entry is marked with the kind of resource it is: ![github](image/alg_R.png) open-source repository, ![web](image/alg_I.png) documentation, specification, or hosted tool. Dormant and archived projects are kept when they still explain an architecture — they are labeled as such.

## About

Every entry below is **open-source, openly published, or publicly reproducible** — this list deliberately excludes closed-source SaaS products and vendor marketing collateral. Inclusion does not imply endorsement, and no link substitutes for sound causal reasoning: prefer [incrementality](#geo-lift--incrementality-testing) over attribution-by-default, and validate every model against an experiment when one is feasible.

## Contents

- [Open-Source MMM Frameworks](#open-source-mmm-frameworks)
- [Geo-Lift & Incrementality Testing](#geo-lift--incrementality-testing)
- [Multi-Touch Attribution (MTA) & Causal Inference](#multi-touch-attribution-mta--causal-inference)
- [Foundational Papers & Technical Whitepapers](#foundational-papers--technical-whitepapers)
- [Synthetic Data & Public Datasets](#synthetic-data--public-datasets)
- [Tutorials, Notebooks & Courses](#tutorials-notebooks--courses)
- [Books, Blogs & Communities](#books-blogs--communities)
- [Contributing](#contributing)
- [License](#license)

---

## Open-Source MMM Frameworks

*End-to-end libraries, Bayesian engines, and evaluation toolkits for building, calibrating, and optimizing marketing mix models.*

![github](image/alg_R.png) [Robyn](https://github.com/facebookexperimental/Robyn) - Meta Marketing Science's R (with experimental Python) package for automated MMM using multi-objective evolutionary hyperparameter search, Pareto-optimal model selection, and budget allocation.

![github](image/alg_R.png) [Meridian](https://github.com/google/meridian) - Google's open-source Bayesian MMM framework (JAX backend) featuring reach and frequency modeling, priors calibrated from incrementality experiments, and scenario planning.

![github](image/alg_R.png) [PyMC-Marketing](https://github.com/pymc-labs/pymc-marketing) - PyMC Labs' Bayesian marketing-science toolkit in Python covering media mix models, customer lifetime value, and customer choice with a notebook-first developer experience.

![github](image/alg_R.png) [LightweightMMM](https://github.com/google/lightweight_mmm) - Google's archived lightweight Bayesian MMM library (TensorFlow Probability) implementing geometric adstock and Hill-function saturation; superseded by Meridian but still instructive.

![github](image/alg_R.png) [Orbit](https://github.com/uber/orbit) - Uber's Python time-series forecasting toolkit whose structural time-series models (e.g., KTR) support Bayesian MMM-style response-curve estimation and demand forecasting.

![github](image/alg_R.png) [mmm_stan](https://github.com/sibylhe/mmm_stan) - Python and Stan implementation of a multiplicative marketing mix model with adstock carryover, ROAS, and marginal ROAS estimation.

![github](image/alg_R.png) [BayesianMMM](https://github.com/leopoldavezac/BayesianMMM) - Python implementation of Bayesian media mix modeling with shape and carryover effects.

![github](image/alg_R.png) [mamimo](https://github.com/RobKuebler/mamimo) - Lightweight Python package for building and evaluating marketing mix models with scikit-learn-compatible transformers.

![github](image/alg_R.png) [AutoMMM](https://github.com/nialloulton/AutoMMM) - Experimental open-source automated marketing mix modeling and feature-selection tool in Python.

![github](image/alg_R.png) [hommmer](https://github.com/hammer-mt/hommmer) - Simple, accessible marketing mix modeling library for Python.

![github](image/alg_R.png) [VEX-MMM](https://github.com/hammer-mt/VEX-MMM) - Open-source marketing mix modeling codebase powering vexpower.com.

![github](image/alg_R.png) [simba-mmm](https://github.com/getsimba-ai/simba-mmm) - Open-source Bayesian marketing mix modeling platform built on PyMC-Marketing for media attribution, budget optimization, and scenario planning.

![github](image/alg_R.png) [mmm-eval](https://github.com/mutinex/mmm-eval) - Comprehensive evaluation framework for benchmarking and validating marketing mix models.

![github](image/alg_R.png) [CausalMMM](https://github.com/ChaunceyKung/CausalMMM) - Research implementation for learning causal structure in marketing mix modeling.

![github](image/alg_R.png) [weibull-adstock](https://github.com/annalectnl/weibull-adstock) - R/Python utilities for modeling media adstock effects using Weibull transformations.

---

## Geo-Lift & Incrementality Testing

*Tools for designing, running, and analyzing geo-experiments and quasi-experimental incrementality studies.*

![github](image/alg_R.png) [GeoLift](https://github.com/facebookincubator/GeoLift) - Meta's R package for end-to-end geo experiments using augmented synthetic control, with data-driven market selection, power simulations, and lift estimation.

![github](image/alg_R.png) [Meridian GeoX](https://github.com/google/meridian-geox) - Google's open-source geo-experimentation library for holdback, go-dark, and heavy-up designs combining time-based regression with stratified sampling, feeding experiment priors back into Meridian.

![github](image/alg_R.png) [CausalImpact](https://github.com/google/CausalImpact) - Google's R package implementing Bayesian structural time-series for estimating the causal impact of an intervention, the reference implementation of Brodersen et al. (2015).

![github](image/alg_R.png) [CausalPy](https://github.com/pymc-labs/causalpy) - PyMC Labs' Python library for Bayesian difference-in-differences, synthetic control, interrupted time series, and event studies.

![github](image/alg_R.png) [Trimmed Match](https://github.com/google/trimmed_match) - Google's Python library implementing trimmed-match pairing for randomized paired geo experiments (Chen, Longfils & Reny).

![github](image/alg_R.png) [Matched Markets](https://github.com/google/matched_markets) - Google's archived Python research code for designing geo lift studies using time-based regression and matched markets.

![github](image/alg_R.png) [augsynth](https://github.com/ebenmichael/augsynth) - R package for the augmented synthetic control method of Ben-Michael, Feller & Rothstein, the estimation engine underneath GeoLift.

![github](image/alg_R.png) [tidysynth](https://github.com/edunford/tidysynth) - R tidyverse-style implementation of the synthetic control method for constructing valid counterfactuals in geo and panel comparisons.

![github](image/alg_R.png) [GeoexperimentsResearch](https://github.com/google/GeoexperimentsResearch) - Google's archived R package implementing the geo-experiment methodology (GBR/TBR) behind Kerman, Wang & Vaver (2017).

![github](image/alg_R.png) [Recast Geo-Experiment Simulation Study](https://github.com/getrecast/geolift-simulation-study) - Open benchmark of ~32,000 simulated geo experiments comparing GeoLift, CausalImpact, CausalPy, and Matched Markets under known ground truth; companion essay at [research.getrecast.com/geolift-sim-study](https://research.getrecast.com/geolift-sim-study).

---

## Multi-Touch Attribution (MTA) & Causal Inference

*Libraries for Markov-chain attribution, uplift modeling, and modern causal inference.*

![github](image/alg_R.png) [ChannelAttribution](https://github.com/DavideAltomare/ChannelAttribution) - R package implementing heuristic and data-driven (Markov chain) multi-channel attribution with removal-effects analysis and channel-response estimation.

![github](image/alg_R.png) [markovattribution](https://github.com/kailin-lu/markovattribution) - Python implementation of graph-based multi-touch attribution with Markov chains, following Anderl et al. (2016).

![github](image/alg_R.png) [DoWhy](https://github.com/py-why/dowhy) - Python library for causal inference that makes assumptions explicit and supports identification, estimation, and refutation testing — essential hygiene for both MTA and MMM findings.

![github](image/alg_R.png) [EconML](https://github.com/py-why/econml) - Microsoft Research/py-why library for heterogeneous treatment-effect estimation (CATE) using double machine learning, meta-learners, and instrumental variables.

![github](image/alg_R.png) [CausalML](https://github.com/uber/causalml) - Uber's Python toolkit for uplift modeling and causal inference with tree-based, metalearner, and neural implementations.

![github](image/alg_R.png) [DoubleML](https://github.com/DoubleML/doubleml-for-py) - Python (and R) object-oriented implementation of double/debiased machine learning (Chernozhukov et al., 2018) for valid inference when using ML nuisance models.

![web](image/alg_I.png) [did](https://cran.r-project.org/package=did) - R package (Callaway & Sant'Anna) for difference-in-differences with multiple time periods and staggered treatment timing, the modern standard for staged marketing-rollout evaluation.

---

## Foundational Papers & Technical Whitepapers

*Peer-reviewed research, preprints, and industry whitepapers that define modern MMM and causal marketing measurement.*

![web](image/alg_I.png) [Jin et al. (2017) - Bayesian Methods for Media Mix Modeling with Carryover and Shape Effects](https://research.google/pubs/bayesian-methods-for-media-mix-modeling-with-carryover-and-shape-effects/) - The canonical Google Research paper introducing Bayesian MMM with geometric adstock (carryover), Hill-function saturation, and ROAS/mROAS derived from posterior samples.

![web](image/alg_I.png) [Chan & Perry (2017) - Challenges and Opportunities in Media Mix Modeling](https://research.google/pubs/challenges-and-opportunities-in-media-mix-modeling/) - Google's critical review of where MMMs fail — identification, prior sensitivity, aggregation bias — and what rigorous practice looks like.

![web](image/alg_I.png) [Wang et al. (2017) - A Hierarchical Bayesian Approach to Improve Media Mix Models Using Category Data](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45999.pdf) - Hierarchical Bayesian modeling across brands within a category to pool information and stabilize channel-effect estimates for sparse spenders.

![web](image/alg_I.png) [Sun et al. (2017) - Geo-level Bayesian Hierarchical Media Mix Modeling](https://research.google/pubs/geo-level-bayesian-hierarchical-media-mix-modeling/) - Extends Jin et al. (2017) to sub-national data, showing geo-level hierarchical models tighten credible intervals and reduce ad-targeting bias.

![web](image/alg_I.png) [Kerman, Wang & Vaver (2017) - Estimating Ad Effectiveness using Geo Experiments in a Time-Based Regression Framework](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45950.pdf) - The TBR paper formalizing counterfactual projection of control markets for geo-experiment readouts.

![web](image/alg_I.png) [Brodersen et al. (2015) - Inferring Causal Impact Using Bayesian Structural Time-Series Models](https://arxiv.org/abs/1506.00356) - Annals of Applied Statistics 9(1):247-274; the state-space/synthetic-control framework implemented by CausalImpact.

![web](image/alg_I.png) [Runge et al. (2024) - Packaging Up Media Mix Modeling: An Introduction to Robyn's Open-Source Approach](https://arxiv.org/abs/2403.14674) - The definitive methodological description of Robyn's nevergrad-based calibration, Pareto frontiers, and open-source MMM workflow.

![web](image/alg_I.png) [Nerlove & Arrow (1962) - Optimal Advertising Policy under Dynamic Conditions](https://doi.org/10.2307/2551549) - Economica 29(114):129-142; the origin of the goodwill-stock (adstock) formulation that still underpins carryover modeling.

![web](image/alg_I.png) [Vidale & Wolfe (1957) - An Operations-Research Study of Sales Response to Advertising](https://doi.org/10.1287/opre.5.3.370) - Operations Research 5(3):370-381; the classic sales-decay and saturation-level response model underlying diminishing-returns curves.

![web](image/alg_I.png) [Clarke (1976) - Econometric Measurement of the Duration of Advertising Effect on Sales](https://doi.org/10.1177/002224377601300404) - Journal of Marketing Research 13(4):345-357; foundational empirical treatment of adstock duration and decay rates.

![web](image/alg_I.png) [Shao & Li (2011) - Data-Driven Multi-Touch Attribution Models](https://doi.org/10.1145/2020408.2020453) - KDD 2011; early data-driven MTA via bagged logistic regression and probabilistic models comparing converters vs. non-converters.

![web](image/alg_I.png) [Anderl et al. (2016) - Mapping the Customer Journey: Lessons Learned from Graph-Based Online Attribution Modeling](https://doi.org/10.1016/j.ijresmar.2016.03.001) - International Journal of Research in Marketing 33(3):457-474; graph/Markov-chain attribution on Bing journeys at scale.

![web](image/alg_I.png) [Ravid (2025) - Marketing Mix Modeling in Lemonade](https://arxiv.org/abs/2501.01276) - Applied case study validating a Bayesian MMM for an online insurer against A/B tests, holdouts, and convex budget-allocation scenarios.

---

## Synthetic Data & Public Datasets

*Simulators and open datasets for benchmarking MMM pipelines before touching production spend.*

![github](image/alg_R.png) [siMMMulator](https://github.com/facebookexperimental/siMMMulator) - Meta's R package for simulating synthetic MMM datasets with adstock, diminishing returns, seasonality, and trend, used to benchmark Robyn before touching real spend data.

![github](image/alg_R.png) [PySiMMMulator](https://github.com/RyanAugust/PySiMMMulator) - Open-source Python marketing simulation package for generating synthetic MMM datasets.

![github](image/alg_R.png) [dammmdatagen](https://github.com/DoktorMike/dammmdatagen) - Synthetic data generator designed specifically for testing and validating marketing mix models.

![web](image/alg_I.png) [Advertising (ISLR/IS2)](https://www.statlearning.com/s/Advertising.csv) - The classic 200-market TV/radio/newspaper vs. sales dataset from *An Introduction to Statistical Learning*; the standard toy example for response-curve fitting.

![web](image/alg_I.png) [Sample Media Spends Data](https://www.kaggle.com/datasets/yugagrawal95/sample-media-spends-data) - ~3,000 rows of channel-by-week marketing spend with sales outcomes, suited to a first end-to-end MMM on Kaggle infrastructure.

![web](image/alg_I.png) [M5 Forecasting — Accuracy](https://www.kaggle.com/competitions/m5-forecasting-accuracy) - Walmart unit-sales data with calendar, prices, and events; a realistic retail sandbox for demand modeling with exogenous marketing-adjacent drivers.

![web](image/alg_I.png) [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales) - Daily store-level sales with promotions and competition context; well suited to promo-lift and store-level hierarchical modeling exercises.

---

## Tutorials, Notebooks & Courses

*Hands-on guides, workshops, and reference implementations for practitioners.*

![github](image/alg_R.png) [Meridian Demo Notebooks](https://github.com/google/meridian/tree/main/demo) - Official Colab-ready walkthroughs: getting started, reach/frequency, prior calibration, ROI & mROI curves, and scenario planning.

![web](image/alg_I.png) [Meridian Documentation](https://developers.google.com/meridian) - Official guides and API reference covering model specification, priors, calibration from incrementality experiments, and deployment.

![github](image/alg_R.png) [Robyn Demo](https://github.com/facebookexperimental/Robyn/tree/main/demo) - End-to-end R demo of model input validation, automated hyperparameter optimization, Pareto selection, allocation, and export.

![web](image/alg_I.png) [PyMC-Marketing Documentation](https://www.pymc-marketing.io) - Official docs with worked MMM and CLV notebooks, including prior setup, saturation/adstock configuration, and budget optimization.

![web](image/alg_I.png) [Media Effect Estimation with PyMC: Adstock, Saturation & Diminishing Returns](https://juanitorduz.github.io/pymc_mmm/) - Deep-dive tutorial replicating Google's carryover/shape-effects methodology in PyMC with companion notebooks and ROAS/mROAS extraction.

![github](image/alg_R.png) [ad_response_tutorial](https://github.com/eleafeit/ad_response_tutorial) - R tutorial comparing last-click attribution, experiments, marketing mix models, and attribution models on the same synthetic dataset.

![github](image/alg_R.png) [marketing-science-in-python](https://github.com/takechanman1228/marketing-science-in-python) - Practical Python guide covering marketing analytics, causal inference, marketing mix modeling, pricing, and forecasting.

![github](image/alg_R.png) [media-mix-modeling (Databricks)](https://github.com/databricks-industry-solutions/media-mix-modeling) - Databricks solution accelerator demonstrating scalable media mix modeling pipelines.

![github](image/alg_R.png) [mmm-workshop](https://github.com/xtreamsrl/mmm-workshop) - Code and workshop materials for building Bayesian media mix models.

![web](image/alg_I.png) [Introduction to Causal Inference — Brady Neal](https://www.bradyneal.com/causal-inference-course) - Free, modern causal-inference course (potential outcomes, backdoors, DML, DiD) with lectures and problem sets; essential groundwork for incrementality work.

![web](image/alg_I.png) [Marketing Mix Modeling (MMM) Implementation — Kaggle Notebook](https://www.kaggle.com/code/subhrasmukherjee/marketing-mix-modelling-mmm-implementation) - Practical end-to-end notebook on product-advertising data including lag-structure estimation and spend-elasticity visualization.

---

## Books, Blogs & Communities

*Textbooks, technical blogs, related awesome lists, and practitioner communities.*

![web](image/alg_I.png) [Causal Inference: The Mixtape — Scott Cunningham](https://mixtape.scunning.com) - Free, open online textbook covering DiD, synthetic control, IV, RDD, and matching — the causal toolkit behind modern incrementality testing.

![web](image/alg_I.png) [Market Response Models: Econometric and Time Series Analysis — Hanssens, Parsons & Schultz](https://link.springer.com/book/10.1007/b109775) - The definitive econometric treatment of aggregate advertising response models (Springer, 2001).

![web](image/alg_I.png) [Recast Blog](https://getrecast.com/blog) - Opinionated, technical essays on MMM practice: saturation curves, channel interactions, budget allocation, and the limits of deterministic last-click measurement.

![web](image/alg_I.png) [Recast Research](https://research.getrecast.com) - Open research and benchmarks from the Recast team, including large-scale geo-experiment simulation studies with reproducible code.

![web](image/alg_I.png) [PyMC Labs Blog](https://www.pymc-labs.com) - Applied Bayesian case studies and launches from the PyMC Labs team, including funnel-aware MMMs and `do`-operator causal analysis with PyMC-Marketing.

![web](image/alg_I.png) [PyMC Discourse](https://discourse.pymc.io) - Official community forum for PyMC and PyMC-Marketing; the fastest route to unblocking priors, sampler diagnostics, and model-specification questions.

![web](image/alg_I.png) [MeasureCamp](https://measurecamp.org) - Global, free-to-attend analytics unconference and community; practitioner sessions on MMM, geo-testing, and privacy-durable measurement.

![web](image/alg_I.png) [r/Bayesian](https://www.reddit.com/r/Bayesian/) - Broad Bayesian-modeling community with recurring, substantive threads on marketing mix and media-response modeling.

![github](image/alg_R.png) [Robyn GitHub Discussions](https://github.com/facebookexperimental/Robyn/discussions) - Direct channel to the Robyn team and a searchable archive of real-world MMM spec, calibration, and allocation questions.

![github](image/alg_R.png) [awesome-marketing-machine-learning](https://github.com/station-10/awesome-marketing-machine-learning) - Curated list of machine learning libraries for marketing, including media mix models, multi-touch attribution, and causal inference.

![github](image/alg_R.png) [Awesome-Marketing-Science](https://github.com/shakostats/Awesome-Marketing-Science) - Curated list of marketing science resources covering geo incrementality testing, media mix models, and causal inference.

---

## Contributing

Contributions are welcome — this list stays useful only if it stays rigorous. Before opening a pull request, please read the full [Contributing Guidelines](CONTRIBUTING.md) and abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

**Quick Submission Rules:**

- **Scope:** Open-source software, peer-reviewed or preprint research, public datasets, and genuinely reproducible tutorials only; no SaaS pitches, affiliate links, or paywalled marketing collateral.
- **Format:** Use the `github` icon (`image/alg_R.png`) when the primary link is a GitHub repository and the `web` icon (`image/alg_I.png`) otherwise:

  ```markdown
  ![github](image/alg_R.png) [Tool Name](https://github.com/org/repo) - Short, objective description of what it does.

  ![web](image/alg_I.png) [Tool Name](https://example.com) - Short, objective description of what it does.
  ```

- **Description:** Concise, objective, and purely informational — focus on utility, methodology, and ecosystem without marketing fluff.
- **License:** By contributing you agree your contribution is dedicated under CC0 1.0 (see [License](#license)).

Found a broken link, an archived repository presented as current, or an outdated recommendation? Open an issue or a pull request — fixes are as valued as additions.

---

## License

This project is dedicated to the public domain under the [CC0 1.0 Universal](LICENSE) public dedication. To the extent possible under law, the author and all contributors waive all copyright and related rights in this work; you may copy, modify, and distribute it for any purpose, commercial or otherwise, without permission.

The projects and papers cited above remain under their own respective licenses; this list makes no claim on them.

[![CC0](https://img.shields.io/badge/CC0-1.0-lightgrey?style=flat-square)](LICENSE)
