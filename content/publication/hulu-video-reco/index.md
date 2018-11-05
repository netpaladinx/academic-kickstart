+++
title = "Hulu video recommendation: from relevance to reasoning"
date = 2018-09-27T00:00:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Xiaoran Xu", "Laming Chen", "Songpeng Zu", "Hanning Zhou"]

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
publication = "In *Proceedings of the 12th ACM Conference on Recommender Systems*"
publication_short = "In *RecSys 2018*"

# Abstract and optional shortened version.
abstract = """Online Video Streaming services such as Hulu hosts tens of millions of premium videos, which requires an effective recommendation system to help viewers discover what they enjoy. In this talk, we will introduce Hulu's recent technical progresses in recommender systems and deep-dive into the topic of generating recommendation reason from knowledge graph. We have two user scenarios: the store-shelf and autoplay. The first requires a list of videos to maximize the chance that a viewer would pick one of them to watch. The second requires a sequence of video recommendations such that the viewer would continuously watch within the current session.

In the model layer, we designed specific models to match with each user scenario, balancing both exploitation and exploration. For example, we leverage the contextual-bandit model in the store-shelf scenario to adapt the ranking strategy to various types of user feedbacks. To optimize exploitation, we tested several granularity levels for parameter sharing among the arms. For more effective exploration, we incorporate Thomason sampling. For the autoplay scenario, we use a contextual recurrent neural network to predict the next video that the viewer is going to watch.

In the feature and data layer, we train embeddings for content, user and contextual info. For example, to train content embeddings, we collect factual tags from metadata, sentiment tags from reviews, and keywords from the captions and object/action recognized using computer vision techniques.

Next we will deep-dive into one important topic: generating recommendation reason from knowledge graph.

A fact is defined by a tuple of related entities and their relation, which is normally a pair of entities tagged by a relationship. In our problem setting, recommendation results are the targets, viewed as inputs for the reasoning task, consisting of pairs of relevant entities, i.e. a source node and a destination node in a knowledge graph. The recommendation reasoning task is to learn a path or a small directed acyclic subgraph, connecting the source node to the destination node.

Since the facts in a knowledge graph have different confidence values for different reasoned targets, we need to conduct a probabilistic inference. The challenge is we do not know a predefined set of logic rules to guide the search through the knowledge graph, which prevents us from directly applying the probabilistic logic methods. Inspired by recent advances in deep learning and reinforcement learning, especially in graph neural networks, attention mechanism and deep generative models, we propose two ways to model the reasoning process: the differentiable reasoning approach and the stochastic reasoning approach.

Differentiable reasoning approaches are based on graph neural networks [1,2] with attention flow and information flow. The attention dynamics is an iterative process of redistributing and aggregating attention over the knowledge graph, starting at the source node. The final attention aggregated at the destination node serves for the prediction to compute the loss. Instead of the prediction accuracy, we care more about how the learned attention dynamics draws its reasoning track in a knowledge graph.

Stochastic reasoning approaches frame the reasoning process as learning a probabilistic graphical model consisting of stochastic discrete operations, such as selecting a node and selecting an edge, to build a reason subgraph extracted from the knowledge graph. The model is known as stochastic computation graphs (SCGs), and to learn it, we propose a generalized back-propagation framework Backprop-Q [3] to overcome the gradient-blocking issues in applying standard back-propagation. In summary, we give an overview of the recommendation research in Hulu and deep-dive into our differentiable reasoning approach and stochastic reasoning approach for generating recommendation reasons based on a knowledge graph."""
abstract_short = ""

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = "https://dl.acm.org/citation.cfm?id=3241730"
#url_preprint = ""
#url_code = ""
#url_dataset = ""
#url_project = ""
#url_slides = ""
#url_video = ""
#url_poster = ""
#url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Digital Object Identifier (DOI)
doi = ""

# Does this page contain LaTeX math? (true/false)
math = true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = "Hulu video recommendation"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++
