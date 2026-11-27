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

### End-to-end frameworks & platforms

![github](image/alg_R.png) [Robyn](https://github.com/facebookexperimental/Robyn) - Meta Marketing Science's R (with experimental Python) package for automated MMM using multi-objective evolutionary hyperparameter search, Pareto-optimal model selection, and budget allocation.

![github](image/alg_R.png) [Meridian](https://github.com/google/meridian) - Google's open-source Bayesian MMM framework (JAX backend) featuring reach and frequency modeling, priors calibrated from incrementality experiments, and scenario planning.

![github](image/alg_R.png) [PyMC-Marketing](https://github.com/pymc-labs/pymc-marketing) - PyMC Labs' Bayesian marketing-science toolkit in Python covering media mix models, customer lifetime value, and customer choice with a notebook-first developer experience.

![github](image/alg_R.png) [LightweightMMM](https://github.com/google/lightweight_mmm) - Google's archived lightweight Bayesian MMM library (TensorFlow Probability) implementing geometric adstock and Hill-function saturation; superseded by Meridian but still instructive.

![github](image/alg_R.png) [simba-mmm](https://github.com/getsimba-ai/simba-mmm) - Open-source Bayesian marketing mix modeling platform built on PyMC-Marketing for media attribution, budget optimization, and scenario planning.

![github](image/alg_R.png) [VEX-MMM](https://github.com/hammer-mt/VEX-MMM) - Open-source marketing mix modeling codebase powering vexpower.com.

### Composable & lightweight libraries

![github](image/alg_R.png) [Orbit](https://github.com/uber/orbit) - Uber's Python time-series forecasting toolkit whose structural time-series models (e.g., KTR) support Bayesian MMM-style response-curve estimation and demand forecasting.

![github](image/alg_R.png) [mmm_stan](https://github.com/sibylhe/mmm_stan) - Python and Stan implementation of a multiplicative marketing mix model with adstock carryover, ROAS, and marginal ROAS estimation.

![github](image/alg_R.png) [BayesianMMM](https://github.com/leopoldavezac/BayesianMMM) - Python implementation of Bayesian media mix modeling with shape and carryover effects.

![github](image/alg_R.png) [mamimo](https://github.com/RobKuebler/mamimo) - Lightweight Python package for building and evaluating marketing mix models with scikit-learn-compatible transformers.

![github](image/alg_R.png) [AutoMMM](https://github.com/nialloulton/AutoMMM) - Experimental open-source automated marketing mix modeling and feature-selection tool in Python.

![github](image/alg_R.png) [hommmer](https://github.com/hammer-mt/hommmer) - Simple, accessible marketing mix modeling library for Python.

![github](image/alg_R.png) [Karpiu](https://github.com/edwinnglabs/karpiu) - Python MMM package built on Uber's Orbit, providing adstock and saturation transforms, channel attribution, and budget optimization (beta).

![github](image/alg_R.png) [Epsilon.jl](https://github.com/shawcharles/epsilon) - Julia framework for Bayesian marketing mix modeling.

![github](image/alg_R.png) [CausalMMM](https://github.com/ChaunceyKung/CausalMMM) - Research implementation for learning causal structure in marketing mix modeling.

![github](image/alg_R.png) [weibull-adstock](https://github.com/annalectnl/weibull-adstock) - R/Python utilities for modeling media adstock effects using Weibull transformations.

### Validation, benchmarking & data quality

![github](image/alg_R.png) [mmm-eval](https://github.com/mutinex/mmm-eval) - Comprehensive evaluation framework for benchmarking and validating marketing mix models.

![github](image/alg_R.png) [robyn-data-validation](https://github.com/yanhong-zhao-ef/robyn-data-validation) - Data validation module accompanying Robyn, checking input-data quality (spend positivity, date continuity, missingness) before model fitting.

![github](image/alg_R.png) [ml-in-mmm](https://github.com/annalectnl/ml-in-mmm) - Research code from Annalect comparing the accuracy and usability of machine-learning models versus regression for MMM analyses.

---

## Geo-Lift & Incrementality Testing

*Tools for designing, running, and analyzing geo-experiments and quasi-experimental incrementality studies.*

### Experiment design & lift estimation

![github](image/alg_R.png) [GeoLift](https://github.com/facebookincubator/GeoLift) - Meta's R package for end-to-end geo experiments using augmented synthetic control, with data-driven market selection, power simulations, and lift estimation.

![github](image/alg_R.png) [Meridian GeoX](https://github.com/google/meridian-geox) - Google's open-source geo-experimentation library for holdback, go-dark, and heavy-up designs combining time-based regression with stratified sampling, feeding experiment priors back into Meridian.

![github](image/alg_R.png) [CausalImpact](https://github.com/google/CausalImpact) - Google's R package implementing Bayesian structural time-series for estimating the causal impact of an intervention, the reference implementation of Brodersen et al. (2015).

![github](image/alg_R.png) [CausalPy](https://github.com/pymc-labs/causalpy) - PyMC Labs' Python library for Bayesian difference-in-differences, synthetic control, interrupted time series, and event studies.

![github](image/alg_R.png) [Trimmed Match](https://github.com/google/trimmed_match) - Google's Python library implementing trimmed-match pairing for randomized paired geo experiments (Chen, Longfils & Remy).

![github](image/alg_R.png) [Matched Markets](https://github.com/google/matched_markets) - Google's archived Python research code for designing geo lift studies using time-based regression and matched markets.

![github](image/alg_R.png) [GeoexperimentsResearch](https://github.com/google/GeoexperimentsResearch) - Google's archived R package implementing the geo-experiment methodology (GBR/TBR) behind Kerman, Wang & Vaver (2017).

![github](image/alg_R.png) [murray](https://github.com/entropyx/murray) - Python toolkit for geographic experiment design and evaluation, covering power analysis, market selection, and lift estimation for geo tests.

![github](image/alg_R.png) [geo-rct-methodology](https://github.com/rickcentralcontrolcom/geo-rct-methodology) - Open-source best practices for running geographic randomized controlled trials, from randomization and power to analysis and reporting.

### Synthetic control & panel estimators

![github](image/alg_R.png) [augsynth](https://github.com/ebenmichael/augsynth) - R package for the augmented synthetic control method of Ben-Michael, Feller & Rothstein, the estimation engine underneath GeoLift.

![github](image/alg_R.png) [tidysynth](https://github.com/edunford/tidysynth) - R tidyverse-style implementation of the synthetic control method for constructing valid counterfactuals in geo and panel comparisons.

![github](image/alg_R.png) [synthdid](https://github.com/synth-inference/synthdid) - R implementation of synthetic difference-in-differences (Arkhangelsky et al., 2021), combining synthetic control weights with unit and time fixed effects.

![github](image/alg_R.png) [gsynth](https://github.com/xuyiqing/gsynth) - R package for the generalized synthetic control method, a factor-model approach to causal inference with panel data.

![web](image/alg_I.png) [did](https://cran.r-project.org/package=did) - R package (Callaway & Sant'Anna) for difference-in-differences with multiple time periods and staggered treatment timing, the modern standard for staged marketing-rollout evaluation.

![github](image/alg_R.png) [fixest](https://github.com/lrberge/fixest) - Fast fixed-effects estimators in R, including staggered difference-in-differences (`sunab`) and event-study plots.

![github](image/alg_R.png) [pyfixest](https://github.com/py-econometrics/pyfixest) - Python implementation of the fixest syntax for high-dimensional fixed-effects regression, with DiD and event-study support.

![github](image/alg_R.png) [HonestDiD](https://github.com/asheshrambachan/HonestDiD) - R package for robust inference in difference-in-differences and event-study designs when parallel trends may be violated (Rambachan & Roth).

![github](image/alg_R.png) [did2s](https://github.com/kylebutts/did2s) - R package implementing Gardner's two-stage difference-in-differences estimator, robust to heterogeneous treatment effects.

### Benchmarks & measurement guides

![github](image/alg_R.png) [Recast Geo-Experiment Simulation Study](https://github.com/getrecast/geolift-simulation-study) - Open benchmark of ~32,000 simulated geo experiments comparing GeoLift, CausalImpact, CausalPy, and Matched Markets under known ground truth; companion essay at [research.getrecast.com/geolift-sim-study](https://research.getrecast.com/geolift-sim-study).

![github](image/alg_R.png) [marketing_messages_measurement](https://github.com/fbsamples/marketing_messages_measurement) - Meta's sample code and best practices for measuring WhatsApp marketing messages with conversion lifts and holdout designs.

---

## Multi-Touch Attribution (MTA) & Causal Inference

*Libraries for Markov-chain attribution, uplift modeling, and modern causal inference.*

### Attribution modeling libraries

![github](image/alg_R.png) [ChannelAttribution](https://github.com/DavideAltomare/ChannelAttribution) - R package implementing heuristic and data-driven (Markov chain) multi-channel attribution with removal-effects analysis and channel-response estimation.

![github](image/alg_R.png) [markovattribution](https://github.com/kailin-lu/markovattribution) - Python implementation of graph-based multi-touch attribution with Markov chains, following Anderl et al. (2016).

![github](image/alg_R.png) [mta](https://github.com/eeghor/mta) - Python multi-touch attribution library with heuristic and Markov-chain models plus budget-reallocation utilities.

![github](image/alg_R.png) [Marketing-Attribution-Models](https://github.com/DP6/Marketing-Attribution-Models) - Python implementations of first-touch, last-touch, linear, time-decay, position-based, and Markov-chain attribution models.

![github](image/alg_R.png) [shapley-attribution](https://github.com/ianchute/shapley-attribution) - Scikit-learn-compatible library that uses Shapley values to measure each marketing channel's contribution.

![github](image/alg_R.png) [markov-chain-attribution](https://github.com/jerednel/markov-chain-attribution) - Proof-of-concept fractional attribution model leveraging first-order Markov chains over conversion paths.

![github](image/alg_R.png) [Multi-Touch-Attribution_ShapleyValue](https://github.com/bernard-mlab/Multi-Touch-Attribution_ShapleyValue) - Python implementation of Shapley-value multi-touch attribution for ordered conversion paths.

![github](image/alg_R.png) [Markov-Chain](https://github.com/MatCyt/Markov-Chain) - R-based marketing attribution and basic budget optimization using Markov chains.

![github](image/alg_R.png) [bayesian-marketing-attribution](https://github.com/olivierzach/bayesian-marketing-attribution) - Bayesian marketing-attribution analysis producing channel conversion estimates with uncertainty intervals.

![github](image/alg_R.png) [DeepAttribution](https://github.com/leopoldavezac/DeepAttribution) - Deep-neural-network multi-touch attribution pipeline over customer journeys.

![github](image/alg_R.png) [channel-attribution-model](https://github.com/jeremite/channel-attribution-model) - Attention-based recurrent neural network for supervised multi-touch attribution over conversion sequences.

![github](image/alg_R.png) [DCRMTA](https://github.com/jmtitan/DCRMTA) - Deep causal representation learning for multi-touch attribution (paper code).

![github](image/alg_R.png) [CausalMTA](https://github.com/yaodi833/CausalMTA) - Code and data for CausalMTA, which removes user-confounding bias in causal multi-touch attribution.

### Attribution in the warehouse (dbt & SQL)

![github](image/alg_R.png) [tasman-dbt-mta](https://github.com/TasmanAnalytics/tasman-dbt-mta) - dbt package implementing a multi-touch attribution engine inside the warehouse.

![github](image/alg_R.png) [dbt-snowplow-attribution](https://github.com/snowplow/dbt-snowplow-attribution) - Incremental dbt package for marketing attribution analysis on Snowplow event data.

![github](image/alg_R.png) [multi-touch-attribution (Databricks)](https://github.com/databricks-industry-solutions/multi-touch-attribution) - Databricks solution accelerator connecting marketing spend to sales with multi-touch attribution pipelines.

![github](image/alg_R.png) [ra_attribution](https://github.com/rittmananalytics/ra_attribution) - LookML example of a multi-cycle, multi-touch revenue and cost attribution model.

### Uplift & heterogeneous treatment effects

![github](image/alg_R.png) [CausalML](https://github.com/uber/causalml) - Uber's Python toolkit for uplift modeling and causal inference with tree-based, metalearner, and neural implementations.

![github](image/alg_R.png) [EconML](https://github.com/py-why/econml) - Microsoft Research/py-why library for heterogeneous treatment-effect estimation (CATE) using double machine learning, meta-learners, and instrumental variables.

![github](image/alg_R.png) [DoWhy](https://github.com/py-why/dowhy) - Python library for causal inference that makes assumptions explicit and supports identification, estimation, and refutation testing — essential hygiene for both MTA and MMM findings.

![github](image/alg_R.png) [DoubleML](https://github.com/DoubleML/doubleml-for-py) - Python (and R) object-oriented implementation of double/debiased machine learning (Chernozhukov et al., 2018) for valid inference when using ML nuisance models.

![github](image/alg_R.png) [scikit-uplift](https://github.com/maks-sh/scikit-uplift) - Uplift modeling in scikit-learn style, with meta-learners and uplift evaluation metrics.

![github](image/alg_R.png) [UpliftML](https://github.com/bookingcom/upliftml) - Booking.com's Python package for scalable uplift modeling with meta-learners and model-selection tools.

![github](image/alg_R.png) [CausalLift](https://github.com/Minyus/causallift) - Python package for causality-based uplift modeling with propensity scoring, including a real-world business workflow.

![github](image/alg_R.png) [pylift](https://github.com/wayfair/pylift) - Wayfair's archived uplift modeling package implementing uplift trees and evaluation curves.

![github](image/alg_R.png) [fractional_uplift](https://github.com/google-marketing-solutions/fractional_uplift) - Google Marketing Solutions' archived Python package for cost-aware uplift modelling.

![github](image/alg_R.png) [grf](https://github.com/grf-labs/grf) - Generalized random forests for estimation and inference of heterogeneous treatment effects (Athey, Tibshirani & Wager).

### Causal discovery & general causal inference

![github](image/alg_R.png) [causal-learn](https://github.com/py-why/causal-learn) - CMU's Python causal discovery library implementing constraint-based, score-based, and functional causal models.

![github](image/alg_R.png) [YLearn](https://github.com/DataCanvasIO/YLearn) - Python causal inference library covering causal discovery, effect estimation, and policy learning.

![github](image/alg_R.png) [tfcausalimpact](https://github.com/WillianFuks/tfcausalimpact) - Python port of Google's CausalImpact built on TensorFlow Probability, for Bayesian structural time-series causal estimation.

### Experiment analysis

![github](image/alg_R.png) [confidence](https://github.com/spotify/confidence) - Spotify's Python library for A/B test analysis: variance reduction, sequential tests, and experiment metrics.

---

## Foundational Papers & Technical Whitepapers

*Peer-reviewed research, preprints, and industry whitepapers that define modern MMM and causal marketing measurement.*

### MMM methodology & practice

![web](image/alg_I.png) [Vidale & Wolfe (1957) - An Operations-Research Study of Sales Response to Advertising](https://doi.org/10.1287/opre.5.3.370) - Operations Research 5(3):370-381; the classic sales-decay and saturation-level response model underlying diminishing-returns curves.

![web](image/alg_I.png) [Nerlove & Arrow (1962) - Optimal Advertising Policy under Dynamic Conditions](https://doi.org/10.2307/2551549) - Economica 29(114):129-142; the origin of the goodwill-stock (adstock) formulation that still underpins carryover modeling.

![web](image/alg_I.png) [Clarke (1976) - Econometric Measurement of the Duration of Advertising Effect on Sales](https://doi.org/10.1177/002224377601300404) - Journal of Marketing Research 13(4):345-357; foundational empirical treatment of adstock duration and decay rates.

![web](image/alg_I.png) [Jin et al. (2017) - Bayesian Methods for Media Mix Modeling with Carryover and Shape Effects](https://research.google/pubs/bayesian-methods-for-media-mix-modeling-with-carryover-and-shape-effects/) - The canonical Google Research paper introducing Bayesian MMM with geometric adstock (carryover), Hill-function saturation, and ROAS/mROAS derived from posterior samples.

![web](image/alg_I.png) [Chan & Perry (2017) - Challenges and Opportunities in Media Mix Modeling](https://research.google/pubs/challenges-and-opportunities-in-media-mix-modeling/) - Google's critical review of where MMMs fail — identification, prior sensitivity, aggregation bias — and what rigorous practice looks like.

![web](image/alg_I.png) [Wang et al. (2017) - A Hierarchical Bayesian Approach to Improve Media Mix Models Using Category Data](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45999.pdf) - Hierarchical Bayesian modeling across brands within a category to pool information and stabilize channel-effect estimates for sparse spenders.

![web](image/alg_I.png) [Sun et al. (2017) - Geo-level Bayesian Hierarchical Media Mix Modeling](https://research.google/pubs/geo-level-bayesian-hierarchical-media-mix-modeling/) - Extends Jin et al. (2017) to sub-national data, showing geo-level hierarchical models tighten credible intervals and reduce ad-targeting bias.

![web](image/alg_I.png) [Runge et al. (2024) - Packaging Up Media Mix Modeling: An Introduction to Robyn's Open-Source Approach](https://arxiv.org/abs/2403.14674) - The definitive methodological description of Robyn's nevergrad-based calibration, Pareto frontiers, and open-source MMM workflow.

![web](image/alg_I.png) [Ravid (2025) - Marketing Mix Modeling in Lemonade](https://arxiv.org/abs/2501.01276) - Applied case study validating a Bayesian MMM for an online insurer against A/B tests, holdouts, and convex budget-allocation scenarios.

![web](image/alg_I.png) [Dekimpe & Hanssens (1995) - The Persistence of Marketing Effects on Sales](https://doi.org/10.1287/mksc.14.1.1) - Marketing Science 14(1):1-21; introduces persistence modeling (unit-root tests, Granger causality) to separate temporary from sustained carryover in marketing effects.

![web](image/alg_I.png) [Vakratsas & Ambler (1999) - How Advertising Works: What Do We Really Know?](https://doi.org/10.1177/002224299906300103) - Journal of Marketing 63(1):26-43; reviews 250+ articles to organize advertising-response models into a hierarchy-of-effects framework.

![web](image/alg_I.png) [Assmus, Farley & Lehmann (1984) - How Advertising Affects Sales: Meta-Analysis of Econometric Results](https://doi.org/10.1177/002224378402100107) - Journal of Marketing Research 21(1):65-74; meta-analysis of 128 econometric advertising-sales models quantifying short- versus long-term elasticities.

![web](image/alg_I.png) [Lodish et al. (1995) - A Summary of Fifty-Five In-Market Experiments of the Long-Term Effect of TV Advertising](https://doi.org/10.1287/mksc.14.3.g133) - Marketing Science 14(3):G133-G140; 55 split-cable TV experiments estimating long-term advertising effects.

![web](image/alg_I.png) [Runge & Pauwels (2026) - Open-Source Media and Marketing Mix Modeling: Overview, Challenges, Opportunities](https://msi.org/working-paper/open-source-media-and-marketing-mix-modeling-overview-challenges-opportunities/) - Marketing Science Institute Working Paper 26-106; practice-oriented review of Robyn, Meridian, and PyMC-Marketing, with a workflow for embedding open-source m/MMM in analytics processes.

![web](image/alg_I.png) [Chen & Lim (2026) - When Predictive Fit Misleads: Selecting MMMs Using Experimental RoAS Benchmarks](https://arxiv.org/abs/2611.06111) - Shows that predictive fit can diverge from RoAS recovery, and proposes calibrating MMM specifications against estimand-aligned experimental benchmarks.

![web](image/alg_I.png) [Heusch (2026) - Structural Estimation of Marketing Mix Model Parameters from Geo-Experiments](https://arxiv.org/abs/2608.21128) - Structural estimator that recovers adstock decay, saturation, and effectiveness directly from geo-experimental time series by differencing treated and control regions.

![web](image/alg_I.png) [Heusch (2026) - A Synthetic Benchmark Dataset with Endogenous Marketing Spend for Validating MMMs](https://arxiv.org/abs/2608.21130) - Parameterized generator and reference instance of a 156-week synthetic retail MMM dataset with endogenous spend, geometric adstock, logistic saturation, and a recorded ground-truth decomposition.

![web](image/alg_I.png) [Tirumala (2025) - DeepCausalMMM: A Deep Learning Framework for MMM with Causal Inference](https://arxiv.org/abs/2510.13087) - Neural approach to marketing mix modeling that combines representation learning with causal constraints.

![web](image/alg_I.png) [Lai, Cheng & Liu (2026) - Trustworthy AI for Marketing Measurement](https://doi.org/10.1057/s41270-026-00515-w) - Journal of Marketing Analytics; systematic review of 108 studies across attribution, MMM, causal calibration, and privacy-preserving measurement, proposing a Measure–Validate–Protect framework.

### Incrementality, experiments & measurement

![web](image/alg_I.png) [Kerman, Wang & Vaver (2017) - Estimating Ad Effectiveness using Geo Experiments in a Time-Based Regression Framework](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45950.pdf) - The TBR paper formalizing counterfactual projection of control markets for geo-experiment readouts.

![web](image/alg_I.png) [Brodersen et al. (2015) - Inferring Causal Impact Using Bayesian Structural Time-Series Models](https://arxiv.org/abs/1506.00356) - Annals of Applied Statistics 9(1):247-274; the state-space/synthetic-control framework implemented by CausalImpact.

![web](image/alg_I.png) [Chen, Longfils & Remy (2021) - Trimmed Match Design for Randomized Paired Geo Experiments](https://arxiv.org/abs/2105.07060) - Extends Trimmed Match with optimal subset pairing and sample splitting for robust, cost-effective iROAS estimation from paired geo tests.

![web](image/alg_I.png) [Lewis & Rao (2015) - The Unfavorable Economics of Measuring the Returns to Advertising](https://doi.org/10.1093/qje/qjv023) - Quarterly Journal of Economics 130(4):1941-1973; 25 large-scale RCTs show observational ad ROI estimates are orders of magnitude too high and confidence intervals are enormous.

![web](image/alg_I.png) [Lewis, Rao & Reiley (2011) - Here, There, and Everywhere: Correlated Online Behaviors Can Lead to Overestimates of the Effects of Advertising](https://doi.org/10.1145/1963405.1963431) - WWW 2011:157-166; documents how endogenous browsing and search activity inflates measured ad effects.

![web](image/alg_I.png) [Blake, Nosko & Tadelis (2015) - Consumer Heterogeneity and Paid Search Effectiveness: A Large-Scale Field Experiment](https://doi.org/10.3982/ECTA12423) - Econometrica 83(1):155-174; eBay field experiments showing experimental returns to paid search are a fraction of non-experimental estimates.

![web](image/alg_I.png) [Johnson, Lewis & Nubbemeyer (2017) - Ghost Ads: Improving the Economics of Measuring Online Ad Effectiveness](https://doi.org/10.1509/jmr.15.0297) - Journal of Marketing Research 54(6):867-884; the "ghost ads" method for constructing valid control groups in online ad experiments.

![web](image/alg_I.png) [Konitzer (2026) - Media Measurement and the Assisted Own Goal: Attribution, Marketing-Mix Models, and Individual-Level Incrementality](https://arxiv.org/abs/2607.09608) - Shows how conversion diversion makes attribution under-credit demand-generating platforms and MMM re-credit it through endogenous spend, then proposes ambient audience-level randomization for unbiased ITT measurement.

![web](image/alg_I.png) [Goldfarb & Tucker (2011) - Privacy Regulation and Online Advertising](https://doi.org/10.1287/mnsc.1100.1246) - Management Science 57(1):57-71; EU privacy regulation reduced display-ad effectiveness by roughly 65% relative to non-EU markets.

![web](image/alg_I.png) [Tucker (2014) - Social Networks, Personalized Advertising, and Privacy Controls](https://doi.org/10.1509/jmr.10.0355) - Journal of Marketing Research 51(5):546-562; giving users privacy controls increased the effectiveness of personalized advertising.

![web](image/alg_I.png) [Kato, Honma & Kato (2026) - Generative Marketing Mix Modeling: A Causal Inference Framework Linking GEO and GEM to Business Impact](https://arxiv.org/abs/2609.11915) - Extends MMM logic to generative engine optimization and generative engine marketing, using notice probabilities and question counts to identify effects.

### Attribution

![web](image/alg_I.png) [Shao & Li (2011) - Data-Driven Multi-Touch Attribution Models](https://doi.org/10.1145/2020408.2020453) - KDD 2011; early data-driven MTA via bagged logistic regression and probabilistic models comparing converters vs. non-converters.

![web](image/alg_I.png) [Anderl et al. (2016) - Mapping the Customer Journey: Lessons Learned from Graph-Based Online Attribution Modeling](https://doi.org/10.1016/j.ijresmar.2016.03.001) - International Journal of Research in Marketing 33(3):457-474; graph/Markov-chain attribution on Bing journeys at scale.

![web](image/alg_I.png) [Kireyev, Pauwels & Gupta (2016) - Do Display Ads Influence Search? Attribution and Dynamics in Online Advertising](https://doi.org/10.1016/j.ijresmar.2015.09.007) - International Journal of Research in Marketing 33(3):475-490; display advertising lifts branded search, with dynamics that make last-click attribution understate upper-funnel effects.

![web](image/alg_I.png) [Kannan & Li (2017) - Digital Marketing: A Framework, Review and Research Agenda](https://doi.org/10.1016/j.ijresmar.2016.11.006) - International Journal of Research in Marketing 34(1):22-45; framework for digital marketing, including attribution and measurement.

![web](image/alg_I.png) [Gutierrez & Gérardy (2017) - Causal Inference and Uplift Modelling: A Review of the Literature](https://proceedings.mlr.press/v67/gutierrez17a.html) - PMLR 67:1-13; connects the uplift modeling and causal inference literatures.

![web](image/alg_I.png) [Yadlowsky et al. (2021) - Evaluating Treatment Prioritization Rules via Rank-Weighted Average Treatment Effects](https://arxiv.org/abs/2111.07966) - RATE metrics for comparing and testing treatment-prioritization rules, generalizing Qini/AUUC-style uplift evaluation.

### Synthetic control & difference-in-differences

![web](image/alg_I.png) [Abadie & Gardeazabal (2003) - The Economic Costs of Conflict: A Case Study of the Basque Country](https://doi.org/10.1257/000282803321455188) - American Economic Review 93(1):113-132; introduces the synthetic control method.

![web](image/alg_I.png) [Abadie, Diamond & Hainmueller (2010) - Synthetic Control Methods for Comparative Case Studies](https://doi.org/10.1198/jasa.2009.ap08746) - Journal of the American Statistical Association 105(490):493-505; the canonical synthetic control estimator for comparative case studies.

![web](image/alg_I.png) [Doudchenko & Imbens (2016) - Balancing, Regression, Difference-In-Differences and Synthetic Control Methods: A Synthesis](https://doi.org/10.3386/w22791) - NBER Working Paper 22791; generalizes synthetic control to allow negative weights and unit fixed effects, nesting DiD and synthetic control in one framework.

![web](image/alg_I.png) [Ben-Michael, Feller & Rothstein (2021) - The Augmented Synthetic Control Method](https://doi.org/10.1080/01621459.2021.1929245) - Journal of the American Statistical Association 116(536):1789-1803; augments synthetic control with a ridge outcome model to correct imperfect pre-treatment fit.

![web](image/alg_I.png) [Arkhangelsky et al. (2021) - Synthetic Difference-in-Differences](https://doi.org/10.1257/aer.20190159) - American Economic Review 111(12):4088-4118; doubly-robust panel estimator combining synthetic control weights with unit and time fixed effects.

![web](image/alg_I.png) [Callaway & Sant'Anna (2021) - Difference-in-Differences with Multiple Time Periods](https://doi.org/10.1016/j.jeconom.2020.12.001) - Journal of Econometrics 225(2):200-230; doubly robust DiD for staggered adoption, the estimator implemented by the `did` R package.

![web](image/alg_I.png) [Goodman-Bacon (2021) - Difference-in-Differences with Variation in Treatment Timing](https://doi.org/10.1016/j.jeconom.2021.03.014) - Journal of Econometrics 225(2):254-277; shows two-way fixed-effects DiD decomposes into weighted 2×2 comparisons that can carry negative weights.

![web](image/alg_I.png) [Sun & Abraham (2021) - Estimating Dynamic Treatment Effects in Event Studies with Heterogeneous Treatment Effects](https://doi.org/10.1016/j.jeconom.2020.09.006) - Journal of Econometrics 225(2):175-199; interaction-weighted estimator for heterogeneous dynamic effects in event studies.

![web](image/alg_I.png) [de Chaisemartin & D'Haultfœuille (2020) - Two-Way Fixed Effects Estimators with Heterogeneous Treatment Effects](https://doi.org/10.1257/aer.20181169) - American Economic Review 110(9):2964-2996; TWFE estimators can be negatively weighted under heterogeneous treatment effects.

![web](image/alg_I.png) [Roth et al. (2023) - What's Trending in Difference-in-Differences? A Synthesis of the Recent Econometrics Literature](https://doi.org/10.1016/j.jeconom.2023.03.008) - Journal of Econometrics 235(2):2218-2244; synthesis of recent DiD advances with concrete recommendations for practitioners.

![web](image/alg_I.png) [Rambachan & Roth (2023) - A More Credible Approach to Parallel Trends](https://doi.org/10.1093/restud/rdad018) - Review of Economic Studies 90(5):2555-2591; robust inference under explicit restrictions on how much parallel trends may be violated.

### Heterogeneous effects & double machine learning

![web](image/alg_I.png) [Chernozhukov et al. (2018) - Double/Debiased Machine Learning for Treatment and Structural Parameters](https://doi.org/10.1111/ectj.12097) - The Econometrics Journal 21(1):C1-C68; the DML framework behind EconML and DoubleML.

![web](image/alg_I.png) [Wager & Athey (2018) - Estimation and Inference of Heterogeneous Treatment Effects using Random Forests](https://doi.org/10.1080/01621459.2017.1319839) - Journal of the American Statistical Association 113(523):1228-1242; causal forests with valid asymptotic inference.

![web](image/alg_I.png) [Athey, Tibshirani & Wager (2019) - Generalized Random Forests](https://doi.org/10.1214/18-AOS1709) - Annals of Statistics 47(2):1148-1178; the method implemented by `grf`.

![web](image/alg_I.png) [Künzel et al. (2019) - Metalearners for Estimating Heterogeneous Treatment Effects using Machine Learning](https://doi.org/10.1073/pnas.1804597116) - PNAS 116(10):4156-4165; S-, T-, and X-learner meta-learners underlying most uplift libraries.

![web](image/alg_I.png) [Shalit, Johansson & Sontag (2017) - Estimating Individual Treatment Effect: Generalization Bounds and Algorithms](https://arxiv.org/abs/1606.03976) - ICML 2017; TARNet/CFR representation-learning approach to individual treatment effect estimation.

![web](image/alg_I.png) [Johansson, Shalit & Sontag (2016) - Learning Representations for Counterfactual Inference](https://arxiv.org/abs/1505.02428) - ICML 2016; balanced representations for counterfactual prediction, foundational for deep-learning MTA.

### Industry standards & guidance

![web](image/alg_I.png) [IAB - Modernizing MMM: Best Practices for Marketers](https://www.iab.com/guidelines/modernizing-mmm-best-practices-for-marketers/) - Vendor-neutral industry guidance (December 2025) on MMM inputs, refresh cadence, calibration against experimentation, and organizational adoption, with a companion MMM Request-for-Information template.

---

## Synthetic Data & Public Datasets

*Simulators and open datasets for benchmarking MMM pipelines before touching production spend.*

### Synthetic data generators & simulators

![github](image/alg_R.png) [siMMMulator](https://github.com/facebookexperimental/siMMMulator) - Meta's R package for simulating synthetic MMM datasets with adstock, diminishing returns, seasonality, and trend, used to benchmark Robyn before touching real spend data.

![github](image/alg_R.png) [PySiMMMulator](https://github.com/RyanAugust/PySiMMMulator) - Open-source Python marketing simulation package for generating synthetic MMM datasets.

![github](image/alg_R.png) [dammmdatagen](https://github.com/DoktorMike/dammmdatagen) - Synthetic data generator designed specifically for testing and validating marketing mix models.

![github](image/alg_R.png) [media_mix_sim](https://github.com/alexhallam/media_mix_sim) - Stan media-mix model with simulated data, useful for validating adstock and saturation estimation.

### Public datasets

![web](image/alg_I.png) [Advertising (ISLR/IS2)](https://www.statlearning.com/s/Advertising.csv) - The classic 200-market TV/radio/newspaper vs. sales dataset from *An Introduction to Statistical Learning*; the standard toy example for response-curve fitting.

![web](image/alg_I.png) [Sample Media Spends Data](https://www.kaggle.com/datasets/yugagrawal95/sample-media-spends-data) - ~3,000 rows of channel-by-week marketing spend with sales outcomes, suited to a first end-to-end MMM on Kaggle infrastructure.

![web](image/alg_I.png) [M5 Forecasting — Accuracy](https://www.kaggle.com/competitions/m5-forecasting-accuracy) - Walmart unit-sales data with calendar, prices, and events; a realistic retail sandbox for demand modeling with exogenous marketing-adjacent drivers.

![web](image/alg_I.png) [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales) - Daily store-level sales with promotions and competition context; well suited to promo-lift and store-level hierarchical modeling exercises.

![web](image/alg_I.png) [Marketing Funnel by Olist](https://www.kaggle.com/datasets/olistbr/marketing-funnel-olist) - 8k marketing qualified leads and closed deals from Brazilian marketplace Olist, joinable to 100k orders for funnel and attribution exercises.

![web](image/alg_I.png) [Sales Conversion Optimization](https://www.kaggle.com/datasets/loveall/clicks-conversion-tracking) - 1,143 Facebook ads with impressions, clicks, spend, and approved conversions broken down by campaign, age, and gender.

![web](image/alg_I.png) [Marketing Campaign](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign) - Customer demographics, product spend, and campaign response across channels for a direct-marketing campaign.

![web](image/alg_I.png) [Marketing A/B Testing](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing) - 588k users randomized into an ad group versus a public-service-announcement control, with conversion and ad-exposure counts.

![web](image/alg_I.png) [Social Media Advertising Dataset](https://www.kaggle.com/datasets/jsonk11/social-media-advertising-dataset) - Synthetic multi-platform campaign data with impressions, clicks, spend, demographic targeting, and conversion rates.

![web](image/alg_I.png) [Criteo Display Advertising Challenge](https://www.kaggle.com/c/criteo-display-ad-challenge) - ~45M-row click-through-rate benchmark with 13 numeric and 26 categorical features from Criteo's display ads.

![web](image/alg_I.png) [Avazu CTR Prediction](https://www.kaggle.com/c/avazu-ctr-prediction) - Eleven days of mobile ad impressions with click labels and 24 features; a standard CTR prediction benchmark.

![web](image/alg_I.png) [Internet Advertisements (UCI)](https://archive.ics.uci.edu/dataset/51/internet+advertisements) - 3,279 labeled ad/non-ad images with URL, anchor-text, and geometry features; the classic ad-detection dataset.

![web](image/alg_I.png) [dunnhumby — The Complete Journey](https://www.dunnhumby.com/source-files/) - Two years of household grocery transactions for 2,500 households plus campaigns, coupons, and display/mailer flags, suited to promo-lift and holdout-style analyses.

---

## Tutorials, Notebooks & Courses

*Hands-on guides, workshops, and reference implementations for practitioners.*

### Official documentation & reference demos

![github](image/alg_R.png) [Meridian Demo Notebooks](https://github.com/google/meridian/tree/main/demo) - Official Colab-ready walkthroughs: getting started, reach/frequency, prior calibration, ROI & mROI curves, and scenario planning.

![web](image/alg_I.png) [Meridian Documentation](https://developers.google.com/meridian) - Official guides and API reference covering model specification, priors, calibration from incrementality experiments, and deployment.

![web](image/alg_I.png) [Robyn Documentation](https://facebookexperimental.github.io/Robyn/) - Official docs covering installation, an analyst's guide to MMM, key features, case studies, and Robyn Python (beta).

![github](image/alg_R.png) [Robyn Demo](https://github.com/facebookexperimental/Robyn/tree/main/demo) - End-to-end R demo of model input validation, automated hyperparameter optimization, Pareto selection, allocation, and export.

![web](image/alg_I.png) [GeoLift Documentation](https://facebookincubator.github.io/GeoLift/) - Official walkthroughs for market selection, power analysis, inference, multi-cell tests, and commuting-zone definitions.

![web](image/alg_I.png) [PyMC-Marketing Documentation](https://www.pymc-marketing.io) - Official docs with worked MMM and CLV notebooks, including prior setup, saturation/adstock configuration, and budget optimization.

![web](image/alg_I.png) [Orbit Documentation](https://orbit-ml.readthedocs.io/en/stable/) - Tutorials for Bayesian forecasting with Orbit's local global trend, KTR, and DLT models, the structural time-series backbone of Karpiu.

![web](image/alg_I.png) [Karpiu Documentation](https://edwinng.com/karpiu/) - API reference and worked examples for Karpiu's MMM workflow: adstock, saturation, attribution, and budget optimization.

### Tutorials, courses & reference implementations

![web](image/alg_I.png) [Media Effect Estimation with PyMC: Adstock, Saturation & Diminishing Returns](https://juanitorduz.github.io/pymc_mmm/) - Deep-dive tutorial replicating Google's carryover/shape-effects methodology in PyMC with companion notebooks and ROAS/mROAS extraction.

![github](image/alg_R.png) [ad_response_tutorial](https://github.com/eleafeit/ad_response_tutorial) - R tutorial comparing last-click attribution, experiments, marketing mix models, and attribution models on the same synthetic dataset.

![github](image/alg_R.png) [marketing-science-in-python](https://github.com/takechanman1228/marketing-science-in-python) - Practical Python guide covering marketing analytics, causal inference, marketing mix modeling, pricing, and forecasting.

![github](image/alg_R.png) [media-mix-modeling (Databricks)](https://github.com/databricks-industry-solutions/media-mix-modeling) - Databricks solution accelerator demonstrating scalable media mix modeling pipelines.

![github](image/alg_R.png) [mmm-workshop](https://github.com/xtreamsrl/mmm-workshop) - Code and workshop materials for building Bayesian media mix models.

![github](image/alg_R.png) [Digital-Marketing-Analytics](https://github.com/Nikhilkohli1/Digital-Marketing-Analytics) - Project collection covering marketing mix modeling, attribution modeling, budget optimization, RFM analysis, segmentation, and recommendation systems.

![github](image/alg_R.png) [Market-Mix-Modelling](https://github.com/Better-Boy/Market-Mix-Modelling) - Step-by-step market mix modelling walkthrough with code and econometric explanation.

![github](image/alg_R.png) [bayesian_mmm](https://github.com/slavakx/bayesian_mmm) - Notebooks accompanying "Modeling Marketing Mix using PyMC3", covering adstock, saturation, and ROAS extraction.

![github](image/alg_R.png) [marketing-mix-modelling](https://github.com/Practical-ML/marketing-mix-modelling) - R code and discussion of MMM specification choices, adstock transformations, and model validation.

![github](image/alg_R.png) [Market-Mix-Modeling](https://github.com/ashish-kamboj/Market-Mix-Modeling) - End-to-end R MMM case study for an e-commerce firm estimating channel elasticities and reallocating budget.

![github](image/alg_R.png) [A_Full_MMM_Guide](https://github.com/mpabon10/A_Full_MMM_Guide) - Self-contained Jupyter notebook covering marketing mix modeling from theory through implementation.

![web](image/alg_I.png) [Causal Inference for the Brave and True](https://matheusfacure.github.io/python-causality-handbook/landing-page.html) - Free online book on causal inference with Python code, covering experiments, panel methods, instrumental variables, and sensitivity analysis.

![github](image/alg_R.png) [causal-inference-visual-guides](https://github.com/kathoffman/causal-inference-visual-guides) - Visual guides to causal inference concepts — DAGs, identification, estimands, and common pitfalls — for applied scientists.

![github](image/alg_R.png) [Deep-Learning-for-Causal-Inference](https://github.com/kochbj/Deep-Learning-for-Causal-Inference) - Tutorials on deep learning for heterogeneous treatment effects, with selection-based and representation-learning approaches.

![web](image/alg_I.png) [Introduction to Causal Inference — Brady Neal](https://www.bradyneal.com/causal-inference-course) - Free, modern causal-inference course (potential outcomes, backdoors, DML, DiD) with lectures and problem sets; essential groundwork for incrementality work.

![web](image/alg_I.png) [Marketing Mix Modeling (MMM) Implementation — Kaggle Notebook](https://www.kaggle.com/code/subhrasmukherjee/marketing-mix-modelling-mmm-implementation) - Practical end-to-end notebook on product-advertising data including lag-structure estimation and spend-elasticity visualization.

---

## Books, Blogs & Communities

*Textbooks, technical blogs, related awesome lists, and practitioner communities.*

### Books

![web](image/alg_I.png) [Causal Inference: The Mixtape — Scott Cunningham](https://mixtape.scunning.com) - Free, open online textbook covering DiD, synthetic control, IV, RDD, and matching — the causal toolkit behind modern incrementality testing.

![web](image/alg_I.png) [Causal Inference: What If — Hernán & Robins](https://miguelhernan.org/whatifbook) - Free textbook on the potential-outcomes framework, with code in R, Stata, SAS, Python, and Julia.

![web](image/alg_I.png) [The Effect — Nick Huntington-Klein](https://theeffectbook.net/) - Free book on research design and causality, covering DiD, regression discontinuity, instrumental variables, and matching.

![web](image/alg_I.png) [Forecasting: Principles and Practice — Hyndman & Athanasopoulos](https://otexts.com/fpp3/) - Free time-series forecasting text covering the baseline models and evaluation practices MMMs build on.

![web](image/alg_I.png) [Market Response Models: Econometric and Time Series Analysis — Hanssens, Parsons & Schultz](https://link.springer.com/book/10.1007/b109775) - The definitive econometric treatment of aggregate advertising response models (Springer, 2001).

### Blogs, research & industry bodies

![web](image/alg_I.png) [Recast Blog](https://getrecast.com/blog) - Opinionated, technical essays on MMM practice: saturation curves, channel interactions, budget allocation, and the limits of deterministic last-click measurement.

![web](image/alg_I.png) [Marketing Triangulation](https://marketingtriangulation.com/) - Practitioner articles on combining MMM, incrementality tests and attribution, with sourced guides to Google Meridian, geo experiments and incremental ROAS.

![web](image/alg_I.png) [Recast Research](https://research.getrecast.com) - Open research and benchmarks from the Recast team, including large-scale geo-experiment simulation studies with reproducible code.

![web](image/alg_I.png) [PyMC Labs Blog](https://www.pymc-labs.com) - Applied Bayesian case studies and launches from the PyMC Labs team, including funnel-aware MMMs and `do`-operator causal analysis with PyMC-Marketing.

![web](image/alg_I.png) [Marketing Science Institute](https://www.msi.org/) - Research organization publishing working papers and research recaps on marketing measurement, including open-source MMM.

### Communities & forums

![web](image/alg_I.png) [PyMC Discourse](https://discourse.pymc.io) - Official community forum for PyMC and PyMC-Marketing; the fastest route to unblocking priors, sampler diagnostics, and model-specification questions.

![web](image/alg_I.png) [Stan Forums](https://discourse.mc-stan.org/) - Community forum for Stan and its ecosystem, covering priors, sampler diagnostics, and model specification for Stan-based MMM implementations.

![web](image/alg_I.png) [MeasureCamp](https://measurecamp.org) - Global, free-to-attend analytics unconference and community; practitioner sessions on MMM, geo-testing, and privacy-durable measurement.

![web](image/alg_I.png) [r/Bayesian](https://www.reddit.com/r/Bayesian/) - Broad Bayesian-modeling community with recurring, substantive threads on marketing mix and media-response modeling.

![github](image/alg_R.png) [Robyn GitHub Discussions](https://github.com/facebookexperimental/Robyn/discussions) - Direct channel to the Robyn team and a searchable archive of real-world MMM spec, calibration, and allocation questions.

### Related awesome lists

![github](image/alg_R.png) [awesome-marketing-machine-learning](https://github.com/station-10/awesome-marketing-machine-learning) - Curated list of machine learning libraries for marketing, including media mix models, multi-touch attribution, and causal inference.

![github](image/alg_R.png) [Awesome-Marketing-Science](https://github.com/shakostats/Awesome-Marketing-Science) - Curated list of marketing science resources covering geo incrementality testing, media mix models, and causal inference.

![github](image/alg_R.png) [awesome-causal-inference](https://github.com/matteocourthoud/awesome-causal-inference) - Curated list of causal inference libraries, resources, and applications.

![github](image/alg_R.png) [Awesome-Uplift-Model](https://github.com/JackHCC/Awesome-Uplift-Model) - Curated list of uplift modeling and causal ML resources, from theory to real-world deployment.

![github](image/alg_R.png) [awesome-marketing-measurement](https://github.com/lifesight/awesome-marketing-measurement) - Vendor-neutral curated list of tools, libraries, research, and resources for measuring marketing effectiveness.

![github](image/alg_R.png) [awesome-attribution](https://github.com/mbuzzco/awesome-attribution) - Curated list of attribution, measurement, and marketing analytics resources.

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
