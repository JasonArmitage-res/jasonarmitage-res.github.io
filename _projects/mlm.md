---
layout: page
title: mlm
description: multitask learning with multiple languages and modalities #a project with a background image
img: assets/img/mlm_icon_resize.jpg
importance: 3
category: papers
---
{% raw %}
```
Paper: https://dl.acm.org/doi/10.1145/3340531.3412783
Code: https://github.com/GOALCLEOPATRA/MLM
MLM Dataset: https://doi.org/10.5281/zenodo.3885753
Citation: see end of page.
```
{% endraw %}

<a href="https://dl.acm.org/doi/10.1145/3340531.3412783">In this research</a>, we propose a multimodal and multilingual resource that is designed to evaluate the strengths of multitask learning systems. 

Four contributions are presented:
* Multiple Languages and Modalities (MLM) - a dataset consisting of text in three languages (EN, FR, DE), images, location data, and triple classes.
* A generation process that provides a consistent and reproducible approach to build a
resource of diverse data with semantic relationships.
* Specification of a novel benchmark task to evaluate multitask systems consisting of cross-modal retrieval and location estimation.
* Multitask IR+LE framework - a multitask system that
combines several methods to perform in concurrence cross-modal retrieval and location estimation on highly diverse
data.

The MLM resource consists of data on 236k human settlements with text summaries, images, coordinates, and triples for each entity. This is used for a novel benchmark task that is designed to evaluate the ability of multitask machine learning systems to generalise on diverse data. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/mlm_mtl.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Systems are assessed on the combined tasks of retrieving multimodal data for and geo-locating entities.
</div>

We build on an approach for learning from cross-modal data by <a href="https://dl.acm.org/doi/10.1109/TPAMI.2019.2927476">Marin et al</a> and implement a framework that retrieves visual and textual inputs for geographic entities ahead of location estimation: 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/mlm_model.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Multitask IR+LE framework.
</div>

Our <a href="https://doi.org/10.5281/zenodo.3885753">datasets</a> and <a href="https://github.com/GOALCLEOPATRA/MLM">code</a> are openly available for use. If this research is of interest, please consider adding a citation:

Jason Armitage, Endri Kacupaj, Golsa Tahmasebzadeh, Swati, Maria Maleshkova, Ralph Ewerth, and Jens Lehmann. 2020. MLM: A Benchmark Dataset for Multitask Learning with Multiple Languages and Modalities. In Proceedings of the 29th ACM International Conference on Information & Knowledge Management (CIKM '20). Association for Computing Machinery, New York, NY, USA, 2967–2974. https://doi.org/10.1145/3340531.3412783

BibTeX:
{% raw %}
```
@inproceedings{armitage2020mlm,
  title={MLM: A Benchmark Dataset for Multitask Learning with Multiple Languages and Modalities},
  author={Armitage, Jason and Kacupaj, Endri and Tahmasebzadeh, Golsa and Maleshkova, Maria and Ewerth, Ralph and Lehmann, Jens},
  booktitle={Proceedings of the 29th ACM International Conference on Information \& Knowledge Management},
  pages={2967--2974},
  year={2020}
}
```
{% endraw %}
