---
layout: page
title: "Samsung AI Challenge"
description: "Competition on Developing Domain Adaptive Semantic Segmentation Algorithms for Autonomous Driving (1st place)<p style='text-align:right; color:gray'>2024.09</p>"
img: assets/img/awards/231030_ss_ai/ss_problem.png
importance: 1
category: competition
related_publications: false
---

<div class="row justify-content-sm-center">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/teams.png" title="Team" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/zoomshot.jpg" title="award 1" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/fullshot.jpg" title="award 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Keondo and I were invited to the Samsung AI Forum, where we received the 1st place award in the Samsung AI Challenge.
    <p>(Prize: 10 million KRW)</p>
</div>
   
  
    
##### <b>[Problem]</b>
Autonomous driving leverages various sensors to perceive the surrounding environment and control the vehicle accordingly. In the case of camera sensors, differences between images (Domain Gap) occur depending on factors like the installation position, type of sensor, and driving environment. Previous studies have widely applied Unsupervised Domain Adaptation techniques to overcome recognition performance degradation due to discrepancies in photometry and texture between images. However, most existing research does not consider the geometric distortions caused by the optical properties of cameras. Therefore, in this competition, we propose **the development of AI algorithms that perform high-performance Semantic Segmentation on distorted images (Target Domain: *Fisheye) by utilizing non-distorted images (Source Domain) and their labels.**
- *Fisheye: Images captured with a fisheye lens that has a 200° Field of View (200° F.O.V)

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/ss_problem.png" title="problem" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
  

##### <b>[Our solution]</b>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/vit-adapter.png" title="model" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We fine-tuned the ViT-Adapter-L model [2], pre-trained on Cityscapes [1], on the competition dataset.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/barrel-distortion.png" title="strategy-1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [ Strategy 1 ] Barrel distortion data augmentation: We obtain target domain images and labels from source domain data by applying barrel distortion and cropping the valid areas from the distorted images.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/background-extraction.png" title="strategy-2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [ Strategy 2 ] Fisheye background area extraction:We extract the fisheye background area from the target domain data and synthesize it with the barrel-distorted image for model training.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/ensemble.png" title="strategy-3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [ Strategy 3 ] Pseudo-labels generation for target images using ensemble.
</div>

##### <b>[Results]</b>
<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231030_ss_ai/result.png" title="strategy-3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We achieved 1st place in both the public and private scores!
    <p>(Public score: mIoU 0.67502 , Private score: mIoU 0.67711)</p>
</div>

##### <b>[References]</b>
[1] M. Cordts et al, “The Cityscapes Dataset for Semantic Urban Scene Understanding,” in Proc. of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016.  
[2] https://github.com/czczup/ViT-Adapter  