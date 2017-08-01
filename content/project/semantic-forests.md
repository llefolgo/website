+++
# Date this page was created.
date = "2016-04-27"

# Project title.
title = "Decision Forests for Semantic Image Segmentation"

# Project summary to display on homepage.
summary = "The Decision Forest algorithm has been very successful in the space of image segmentation, as a simple, fast and extremely flexible approach well-suited to CPU architectures. I implemented a framework called BONSAI, that cascades small decision forests to allow for semantic reasoning in a more natural manner, for the purpose of structured classification tasks such as image segmentation. Furthermore we investigate hidden semantics within decision forests. We implement a form of guided bagging to seamless address class imbalance, significantly increasing precision and recall."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "headers/ACF-preview.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = []

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/ACF-header.png"
width = "width100"

+++

I've been working on this project as a researcher in the [InnerEye](https://www.microsoft.com/en-us/research/project/medical-image-analysis/#) team at MSR Cambridge, where I develop image processing and machine learning solutions for medical image analysis. The BONSAI framework is a fast CPU-based machine learning C++/C# solution for medical image segmentation tasks, and uses Decision Forests as a building block. 

A surprising limitation of 'vanilla' Decision Forests is that they are not easily capable of semantic reasoning, and BONSAI addresses this in a practical way. Organs of interest in medical images have much structure. They have a mean shape from which they typically deviate in a few plausible ways. Anomalies might have more complex patterns of variability, but also display structure. Organs, as well as sub-structures within organs, are also agenced in specific ways relative to each other. Therefore when trying to make sense of the image content, it is natural for us to supplement ambiguous image information with semantic spatial context. A strong hypothesis for the label assignments of a subset of voxels typically provides powerful cues from which to decide label assignments of neighbouring voxels.

Vanilla segmentation forests however are only capable of intensity-based contextual reasoning. We introduce semantic reasoning via auto-context, cascading layers of decision forests whose output, along with the raw intensity maps, form the input to subsequent layers. This is possible thanks to the efficiency with which individual layers are trained (seconds or minutes). In particular at each node, the information gain-based feature optimization is replaced with a scheme based on minimization of hold-out estimates of generalization error. This is seamless, fast and yields a natural mechanism to control tree complexity (tree pruning). 

Finally, we use a form of guided bagging after initial layers, whereby latent clusters are identified within the training data and cluster-specific subforests are trained. For previously unseen data, cluster assignments are computed and points are tested through their cluster-specific subforest. Clusters are learned in an unsupervised manner from the latent semantics already captured within a previous decision forest layer. Each data point is identified with the collection of tree paths that it traverses, and the decision pathways are clustered. The intuition is that data points will share common semantics whenever clustered together, as they jointly satisfy many predicates. 