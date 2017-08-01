+++
abstract = "We propose a framework for probabilistic shape clustering based on kernel-space embeddings derived from spectral signatures. Our root motivation is to investigate practical yet principled clustering schemes that rely on geometrical invariants of shapes rather than explicit registration. To that end we revisit the use of the Laplacian spectrum and introduce a parametric family of reproducing kernels for shapes, extending WESD and shape DNA like metrics. Parameters provide control over the relative importance of local and global shape features, can be adjusted to emphasize a scale of interest or set to uninformative values. As a result of kernelization, shapes are embedded in an infinite-dimensional inner product space. We leverage this structure to formulate shape clustering via a Bayesian mixture of kernel-space Principal Component Analysers. We derive simple variational Bayes inference schemes in Hilbert space, addressing technicalities stemming from the inﬁnite dimensionality. The proposed approach is validated on tasks of unsupervised clustering of sub-cortical structures, as well as classification of cardiac left ventricles w.r.t. pathological groups."
abstract_short = ""
authors = ["L. Le Folgoc", "A. V. Nori", "A. Criminisi"]
date = "2017-07-19"
image_preview = "headers/SK-header.png"
math = true
publication_types = ["1"]
publication = "In *Information Processing in Medical Imaging* (IPMI 2017)"
publication_short = "In *IPMI* 2017"
selected = false
title = "Spectral Kernels for Probabilistic Analysis and Clustering of Shapes"
url_code = ""
url_dataset = ""
url_pdf = "https://www.microsoft.com/en-us/research/wp-content/uploads/2017/02/spectral-kernels_ipmi17.pdf"
url_project = "project/deep-learning/"
url_slides = ""
url_video = ""

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/SK-header.png"
caption = ""
width = "width40"

+++

I've recently presented this work at the [IPMI](http://www.ipmi2017.org/workshops) conference. If you'd fancy a high-level walkthrough more than a dry paper, you might be interested in my [slides](https://oops/spectral-kernels.pptx) on the project.
