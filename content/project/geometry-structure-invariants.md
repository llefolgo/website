+++
# Date this page was created.
date = "2016-04-27"

# Project title.
title = "Geometry of data, structure, quasi-invariants"

# Project summary to display on homepage.
summary = "Sparse priors have a manyfold motivation -- from robust regularization, to reducing the computational complexity of algorithms, to model selection & interpretable machine learning. Sometimes we want to combine the benefits of sparse learning with structured priors that encode a notion of 'smoothness' for the problem at hand. I am interested in scalable inference schemes for structured sparse learning, in particular with Bayesian priors."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "headers/qi-header.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["bayesian-modelling"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/qi-header.png"
width = "width50"

+++

We are interested in classification and regression tasks (or in fact, generalized linear models) in which the output variables can be well predicted using a small (but unknown) subset of variables among a large candidate set of explanatory variables (or basis functions). Moreover the predicted variables are known to vary 'smoothly' as a function of the input variables. A typical application in medical imaging is to regress activated brain regions in functional MRI. In that case, smooth could be synonymous to 'contiguous'. As for me, the real-world application was to regress sparse multiscale representations of (physically plausible) displacement fields for [medical image registration](../../publication/sbr-fast-registration).

We investigate strongly sparse Bayesian priors that combine a structured Gaussian part (the probabilistic counterpart of Tikhonov regularization) and a point mass whenever a variable is 'inactive'. The model relates to Spike-&-Slab and to ARD priors. It generalizes Mike Tipping's sparse Bayesian model of [RVM](http://miketipping.com/sparsebayes.htm). The RVM (under a specific inference scheme, type-II ML) is also a form of (degenerate) [sparse Gaussian process](https://pdfs.semanticscholar.org/dd2e/9d4f9e94ba57b0d0ed1c2f1b1338ada63d97.pdf). We pursue two approaches for inference under such models: a generalized variational Bayes (fast) inference scheme (that can be seen as an extension of Tipping's scheme), and a reversible jump (not as fast?) MCMC approach. Interestingly, the former does tend to give good estimates of the mean but as expected, often inconsistent estimates of uncertainty. We looked into the root causes for such behaviour -- it is linked to the choice of variational approximation, which does open future avenues to correct this behaviour within a fast VB inference scheme.

MATLAB code is available, for the time being on demand.