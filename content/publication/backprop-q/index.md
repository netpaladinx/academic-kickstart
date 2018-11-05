+++
title = "Backprop-Q: Generalized Backpropagation for Stochastic Computation Graphs"
date = 2018-07-25T10:06:24
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Xiaoran Xu", "Songpeng Zu", "Hanning Zhou"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = ""
publication_short = ""

# Abstract and optional shortened version.
abstract = "In real-world scenarios, it is appealing to learn a model carrying out stochastic operations internally, known as stochastic computation graphs (SCGs), rather than learning a deterministic mapping. However, standard backpropagation is not applicable to SCGs. We attempt to address this issue from the angle of cost propagation, with local surrogate costs, called Q-functions, constructed and learned for each stochastic node in an SCG. Then, the SCG can be trained based on these surrogate costs using standard backpropagation. We propose the entire framework as a solution to generalize backpropagation for SCGs, which resembles an actor-critic architecture but based on a graph. For broad applicability, we study a variety of SCG structures from one cost to multiple costs. We utilize recent advances in reinforcement learning (RL) and variational Bayes (VB), such as off-policy critic learning and unbiased-and-low-variance gradient estimation, and review them in the context of SCGs. The generalized backpropagation extends transported learning signals beyond gradients between stochastic nodes while preserving the benefit of backpropagating gradients through deterministic nodes. Experimental suggestions and concerns are listed to help design and test any specific model using this framework."
abstract_short = "A generalized backpropagation framework, Backprop-Q, was introduced to address the issue of gradient propagation on stochastic computation graphs, unifying recent advances in reinforcement learning and variational Bayes and proposing a total credit assignment solution from a graph-level architecture view."

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = [""]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Backpropagation", "Credit Assignment", "Stochastic Computation Graphs"]

# Links (optional).
url_pdf = "https://arxiv.org/pdf/1807.09511.pdf"
url_preprint = "https://arxiv.org/abs/1807.09511"
#url_code = "#"
#url_dataset = "#"
#url_project = "#"
#url_slides = "#"
#url_video = "#"
#url_poster = "#"
#url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
#url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Digital Object Identifier (DOI)
doi = ""

# Does this page contain LaTeX math? (true/false)
math = true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = "Backprop-Q"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  #focal_point = ""
+++
