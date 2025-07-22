---
layout: page
title: ColonOOD
description: "ColonOOD: A Complete Pipeline for Optical Diagnosis of Colorectal Polyps Integrating Out‑of‑Distribution Detection and Uncertainty Quantification<p style='text-align:right; color:gray'>2024.04 - 2025.06</p>"
img: assets/img/publication_preview/colonood-preview.png
importance: 3
category: research
related_publications: false
---

#### [Key Concept]
Colorectal cancer diagnosis demands accurate and reliable polyp assessment during colonoscopy. **ColonOOD** is an integrated system for polyp localization, uncertainty-aware classification, and Out-of-Distribution (OOD) detection. By handling both familiar and novel polyp types with calibrated confidence, it improves clinical reliability. Validated across multiple hospitals and datasets, ColonOOD brings CAD systems closer to real-world adoption.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/gastro/gastro-main.png" title="Colood goal" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption mt-0">
    Research Goal and the target sceanrio.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/publication_preview/colonood-preview.png" title="Colood framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption mt-0">
    The overview of the proposed framework named ColonOOD.
</div>

#### [Publications]
<div class="publications">
   {% bibliography --query @*[tags=colonood] %}
</div>