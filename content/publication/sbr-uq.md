+++
abstract = "We investigate uncertainty quantification under a sparse Bayesian model of medical image registration. Bayesian modelling has proven powerful to automate the tuning of registration hyperparameters, such as the trade-off between the data and regularization functionals. Sparsity-inducing priors have recently been used to render the parametrization itself adaptive and data-driven. The sparse prior on transformation parameters effectively favors the use of coarse basis functions to capture the global trends in the visible motion while finer, highly localized bases are introduced only in the presence of coherent image information and motion. In earlier work, approximate inference under the sparse Bayesian model was tackled in an efficient Variational Bayes (VB) framework. In this paper we are interested in the theoretical and empirical quality of uncertainty estimates derived under this approximate scheme vs. under the exact model. We implement an (asymptotically) exact inference scheme based on reversible jump Markov Chain Monte Carlo (MCMC) sampling to characterize the posterior distribution of the transformation and compare the predictions of the VB and MCMC based methods. The true posterior distribution under the sparse Bayesian model is found to be meaningful: orders of magnitude for the estimated uncertainty are quantitatively reasonable, the uncertainty is higher in textureless regions and lower in the direction of strong intensity gradients. "
abstract_short = ""
authors = ["L. Le Folgoc", "A. V. Nori", "A. Criminisi"]
date = "2017-07-19"
image_preview = "headers/SK-header.png"
math = true
publication_types = ["1"]
publication = "In *Transactions on Medical Imaging* (TMI), IEEE"
publication_short = "In *TMI*, Nov. 2016"
selected = false
title = "Quantifying Registration Uncertainty with Sparse Bayesian Modelling"
url_code = ""
url_dataset = ""
url_pdf = "https://hal.inria.fr/hal-01378844/document"
url_project = "project/bayesian-registration/"
url_slides = ""
url_video = ""

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/SBR-UQ-header.png"
caption = "Three samples from the posterior distribution of displacement fields"

# More details can easily be written below using *Markdown* and $\rm \LaTeX$ math code.

+++
