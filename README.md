# Probabilistic Machine Learning

A collection of probabilistic machine learning experiments developed across three CSC412 project parts. The work explores classification under uncertainty, inference in graphical models, Bayesian skill estimation, approximate posterior inference, generative models, and clustering.

> **Project scope:** This repository brings together related experiments rather than one end-to-end model. The Python modules in `src/` are standalone reference implementations; the reported numerical results and figures come from the original project reports and have not been independently reproduced by these modules.

## Project overview

| Part | Topics | Key techniques |
| --- | --- | --- |
| **Pt1** | Decision theory and classification | Expected loss, Bernoulli Naive Bayes, maximum likelihood and MAP estimation |
| **Pt2** | Graphical models and Bayesian ranking | Markov random fields, loopy belief propagation, TrueSkill, posterior sampling |
| **Pt3** | Approximate inference and unsupervised learning | Variational inference, ELBO optimization, variational autoencoders, K-Means, Gaussian mixture models |

## Selected experimental results

| Experiment | Reported result |
| --- | --- |
| Fashion-MNIST classification with Bernoulli Naive Bayes | **65.0%** training accuracy; **63.7%** test accuracy |
| Binary image denoising with loopy belief propagation | Experiments on **96 × 96** image crops |
| Bayesian chess skill comparison | **65.81%** posterior probability for a particular player comparison |
| Two-player variational inference | **800** optimization iterations, **50** Monte Carlo samples per iteration |
| Clustering comparison | **22%** K-Means error versus **6%** GMM error on the evaluated exercise |

These metrics describe different tasks and are **not directly comparable**. In particular, the TrueSkill percentage is a posterior comparison probability, not classification accuracy.

## Methods

### Pt1 — Decision theory and Naive Bayes

Explores probabilistic decision rules and classification with a Bernoulli Naive Bayes model. Fashion-MNIST images are binarized, and class-conditional pixel probabilities are estimated using maximum likelihood or a Beta-prior MAP approach.

### Pt2 — Loopy belief propagation and TrueSkill

Uses a binary grid-structured Markov random field for image denoising, with sum-product loopy belief propagation to estimate pixel marginals. Also investigates Bayesian player-skill estimation from chess match outcomes using TrueSkill-style latent skill models and posterior sampling.

### Pt3 — Variational inference, generative models, and clustering

Investigates Gaussian variational approximations optimized using the evidence lower bound (ELBO) and reparameterized sampling. The original experiments also include variational autoencoder visualizations and a comparison of K-Means with Gaussian mixture models fitted using expectation-maximization (EM).

## Repository structure

```text
.
├── README.md
├── src/
│   ├── part1.py
│   ├── part2.py
│   └── part3
├── figures/
│   ├── FIGURE_GALLERY.md
│   ├── FIGURE_INDEX.csv
│   ├── 01-decision-theory-naive-bayes-graphical-models/
│   ├── 02-loopy-bp-trueskill-hmc/
│   └── 03-variational-inference-vae-clustering/
└── reports/
    ├── part1.pdf (Received 97% score)
    ├── part2.pdf (Received 100% scire)
    └── part3.pdf (TBD)
```

The `figures/` directory contains plots and images extracted from the original reports. Browse the [figure gallery](figures/FIGURE_GALLERY.md) or consult the [figure index](figures/FIGURE_INDEX.csv) for source-page references.
