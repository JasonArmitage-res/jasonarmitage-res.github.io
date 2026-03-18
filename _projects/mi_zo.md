---
layout: page
title: mi-zo
description: multi-information for 3D viewpoint control
img: assets/img/geo_mizo_seg_icon.png
importance: 1
category: papers
---
{% raw %}
```
Paper: https://arxiv.org/abs/2512.24826
Project: https://mi-zo.github.io/mi-zo/
Citation: see end of page.
```
{% endraw %}

<a href="https://arxiv.org/abs/2512.24826">MI-ZO</a> is a method to improve the performance of cross-modal systems trained on 2D visual inputs when reasoning over 3D scenes. A 3D scene can be converted into a sequence of 2D viewpoints for a vision-language model (VLM) - but the dimensional shift can lead to errors on assessing objects in the scene. Our framework consists of a controller that uses outputs from a novel information theoretic measurement method over the multimodal inputs to identify optimal camera viewpoints.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/front_page_figure_mars_10.svg" title="MI-ZO overview placeholder" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    An optimal sequence of viewpoints reduces errors on 3D scenes by a VLM trained on 2D inputs
</div>

The motivating application is planetary science: when generating or analysing 3D reconstructions of Mars, analysis depends on resolving colours and fine-grained surface details. Matching a description to a scene becomes harder when it refers to differences between similar objects such as boulders in the same outcrop.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/geo_prop_web.svg" title="UC-3DS-MI placeholder" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    GeoProperties-3DS is a new benchmark for planetary science.
</div>

We assume the number of mistakes made by VLMs is related to scene complexity and provide a diagnostic called UC-3DS-MI with uniform and complex scenes to demonstrate how complexity and VLM errors are related. Our MI-ZO measurement method distributes scores in relation to the correctness of a system’s responses.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <figure>
            <div class="row text-center">
                <div class="col-lg-6 col-md-12 mb-3">
                    <p class="mb-2"><strong>GO-LED-OL</strong></p>
                    <div class="row">
                        <div class="col-6">
                            <img src="{{ 'assets/img/go_led_cv_score_adj_all_hist.png' | relative_url }}" class="img-fluid rounded z-depth-1" alt="GO-LED-OL chart 1" title="GO-LED-OL chart 1" data-zoomable />
                        </div>
                        <div class="col-6">
                            <img src="{{ 'assets/img/gla_score_all_hist.png' | relative_url }}" class="img-fluid rounded z-depth-1" alt="GO-LED-OL chart 2" title="GO-LED-OL chart 2" data-zoomable />
                        </div>
                    </div>
                </div>
                <div class="col-lg-6 col-md-12 mb-3">
                    <p class="mb-2"><strong>GH-LED</strong></p>
                    <div class="row">
                        <div class="col-6">
                            <img src="{{ 'assets/img/ghled_score_adj_all_hist.png' | relative_url }}" class="img-fluid rounded z-depth-1" alt="GH-LED chart 1" title="GH-LED chart 1" data-zoomable />
                        </div>
                        <div class="col-6">
                            <img src="{{ 'assets/img/gla_score_all_hist.png' | relative_url }}" class="img-fluid rounded z-depth-1" alt="GH-LED chart 2" title="GH-LED chart 2" data-zoomable />
                        </div>
                    </div>
                </div>
            </div>
            <figcaption class="caption">
                Variants of our multi-information metrics with active regret minimisation (MI-ar) distribute scores in relation to the decisions of a VLM.
            </figcaption>
        </figure>
    </div>
</div>

Our method combines MI-ZO with an in-scene camera controller that predicts an optimal sequence of 2D viewpoints along the x-, y-, and z-axes that is most likely to return an accurate assessment by the VLM. A measurement round is followed by a correction round with controller-predicted actions. In contrast to expensive fine-tuning or training an adapter, our controller improves model performance after a couple of demonstrations - and so is tailored to settings with limited data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3d_setup_plan_mars_web.svg" title="Results placeholder" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Actions of the in-scene camera are predicted by an efficient controller guided by the MI-ZO measures.
</div>

On our GeoProperties-3DS benchmark, balanced error rate drops by 19 points. We also introduce two additional benchmarks focusing on feature identification and object occlusions. Further details are available on the <a href="https://mi-zo.github.io/mi-zo/">MI-ZO project page</a>.

Please cite our work if you find it useful:

Armitage, Jason and Rico Sennrich. Video and Language Alignment in 2D Systems for 3D Multi-object Scenes with Multi-Information Derivative-Free Control. arXiv preprint arXiv:2512.24826 (2025).

BibTeX:
{% raw %}
```
@misc{armitage2025mizo,
  title        = {Video and Language Alignment in {2D} Systems for {3D} Multi-object Scenes with Multi-Information Derivative-Free Control},
  author       = {Armitage, Jason and Sennrich, Rico},
  year         = {2025},
  eprint       = {2512.24826},
  archivePrefix= {arXiv},
  primaryClass = {cs.CV},
  doi          = {10.48550/arXiv.2512.24826},
  note={Accepted for publication at the IEEE/CVF Winter Conference on Applications of Computer Vision 2026}
}
```
{% endraw %}
.