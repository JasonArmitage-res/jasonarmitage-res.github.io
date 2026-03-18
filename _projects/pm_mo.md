---
layout: page
title: pm+mo
description: training multimodal systems to generalise with multiple objectives
img: assets/img/two_meshes_clean_flat_1.png
importance: 4
category: papers
---
{% raw %}
```
Paper: https://ceur-ws.org/Vol-2611/paper5.pdf
Citation: see end of page.
```
{% endraw %}

<a href="https://ceur-ws.org/Vol-2611/paper5.pdf">Our paper</a> proposes training a framework for multimodal classification with an additional objective trained using variational inference. 

Machine learning systems trained with supervised learning rely on the availability of large-scale labelled data. In the case of multimodal learning, this further requires combined inputs for each entity. In cases where data are limited, variance is high and neural networks learn sampling noise with subsequent impacts on generalisation.  

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/fig_1_var.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance on the validation partition of MM-IMDb (weighted-F1) for the baseline GMU model. A variant that excludes regularisation underpforms from early on during training.
</div>

We propose a novel system for multimodal classification that makes use of a second objective to learn representations with variational inference. We go on to demonstrate that a combination of ELBO+KL scaling and L2 regularisation offsets overfitting. On the MM-IMDb benchmark, our best variant outperforms the baseline GMU model (<a href="https://arxiv.org/abs/1702.01992">Arevalo et al., (2017)</a>) and versions of the same architecture that exclude the variational inference objective. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pmmo_results.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance on the test partition of MM-IMDb (weighted-F1 and mean over 5 cycles) for our best variant, the baseline GMU model, and a version of the model excluding variational inference as a secondary objective.
</div>

Further results and analysis are available <a href="https://ceur-ws.org/Vol-2611/paper5.pdf">in the paper</a>. Please cite our work if you find it useful for your own research:

Jason Armitage, Shramana Thakur, Rishi Tripathi, and Jens Lehmann, and Maria Maleshkova. 2020. Training Multimodal Systems for Classification with Multiple Objectives. Proceedings of the 1st International Workshop on Cross-lingual Event-centric Open Analytics co-located with the 17th Extended Semantic Web Conference (ESWC 2020).

BibTeX:
{% raw %}
```
@inproceedings{armitage2020training,
  title={Training Multimodal Systems for Classification with Multiple Objectives},
  author={Armitage, Jason and Thakur, Shramana and Tripathi, Rishi and Lehmann, Jens and Maleshkova, Maria},
  booktitle={Proceedings of the 1st International Workshop on Cross-lingual Event-centric Open Analytics co-located with the 17th Extended Semantic Web Conference (ESWC 2020)},
  year={2020}
}
```
{% endraw %}
