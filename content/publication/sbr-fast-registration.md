+++
abstract = "We extend Bayesian models of non-rigid image registration to allow not only for the automatic determination of registration parameters (such as the trade-off between image similarity and regularization functionals), but also for a data-driven, multiscale, spatially adaptive parametrization of deformations. Adaptive parametrizations have been used with success to promote both the regularity and accuracy of registration schemes, but so far on non probabilistic grounds – either as part of multiscale heuristics, or on the basis of sparse optimization. Under the proposed model, a sparsity-inducing prior on transformation parameters complements the classical smoothness-inducing prior, and favors parametrizations that use few degrees of freedom. As a result, ﬁner bases get introduced only in the presence of coherent image information and motion, while coarser bases ensure better extrapolation of the motion to textureless, uninformative regions. The space of possible parametrizations consists of arbitrary combinations of basis functions chosen among any preset, widely overcomplete (and typically multiscale) dictionary. Inference is tackled in an efficient Variational Bayes framework. In addition we propose a flexible mixture-of-Gaussian model of data that proves to be more faithful for a variety of image modalities than the sum-of-squared differences. The performance of the proposed approach is demonstrated on time series of (cine and tagged) magnetic resonance and echocardiographic cardiac images. The proposed algorithm matches the state-of-the-art on benchmark datasets evaluating accuracy of motion and strain, and is highly automated."
abstract_short = "Medical image registration takes a pair of images and returns a transformation of space that captures the underlying non rigid motion, so that images are correctly 'aligned'. This is challenging because of changing organ appearance, random imaging artefacts, because 3D volumes are large, and because many transformations could possibly yield the same observed motion. Intuitively, we'd like to find a smooth solution, whose mathematical representation is multiscale and just complex enough to capture the observed motion - no more, no less. We introduce a probabilistic formulation of registration that does just that. The back-end is an efficient algorithm for structured sparse Bayesian inference."
authors = ["L. Le Folgoc", "H. Delingette", "A. Criminisi", "N. Ayache"]
date = "2017-02-01"
image_preview = ""
math = true
publication_types = ["2"]
publication = "In *Medical Image Analysis (MedIA)*, Elsevier."
publication_short = "In *MedIA*, Feb 2017"
selected = true
title = "Structured Sparse Bayesian Modelling for Medical Image Registration"
#url_code = "#"
#url_dataset = "#"
url_pdf = "https://hal.inria.fr/hal-01149544v2/document"
url_project = "project/bayesian-registration/"
url_slides = "#"
#url_video = "#"

#[[url_custom]]
#name = "Custom Link"
#url = "http://www.example.org"

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/SBR-header-no-cap.png"
caption = "Cardiac motion tracking on cine MRI data. The data is a time series of images. The aim is to recover the motion of the cardiac muscle over time."

# More details can easily be written below using *Markdown* and $\rm \LaTeX$ math code.

+++
