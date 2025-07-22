---
layout: page
title: Adaptive Sensing for DNNs
description: "S4D: Providing proper glasses (sensor control) would be better than solely depending on over-training the brain (neural network)!<p style='text-align:right; color:gray'>2023.08 - current</p>"
img: assets/img/projects/s4d/s4d-main.png
importance: 0
category: research
related_publications: false
---

#### [Key Concept]
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/s4d/s4d-main.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Current AI improvement methods focus solely on the 'brain' components.
</div>

#### [ImageNet-ES]
In contrast to conventional robustness benchmarks that rely on digital perturbations, we directly capture 202k images by using a real camera in a controllable testbed. The dataset presents a wide range of covariate shifts caused by variations in light and camera sensor factors. <a href="https://drive.google.com/file/d/1ZCsc4tw_aRNzWii8ahvKV97z3V3xzMDA/view?usp=sharing">Download ImageNet-ES here</a>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/publication_preview/ImageNet-ES.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <b>[ <i>ImageNet-ES</i> ]</b> A new distribution shift dataset, comprising <b>variations in environmental and camera sensor factors by directly capturing 202k images</b> with a real camera in a controllable testbed.
</div>

#### [ES-Studio]
To compensate the missing perturbations in current robustness benchmarks, we construct a new testbed, **ES-Studio** (**E**nvironment and camera **S**ensor perturbation **Studio**). It can control physical light and camera sensor parameters during data collection.
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/s4d/Testbed-2.png" title="testbed-desc" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/s4d/Testbed_actual.jpg" title="testbed" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <b>[ <i>ES-Studio</i> ]</b> Description and actual.
</div>

#### [Publications]
<div class="publications">
   {% bibliography --query @*[tags=s4d] %}
</div>

