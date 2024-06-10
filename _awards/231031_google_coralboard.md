---
layout: page
title: <b>[Navible&#58 Navigation for Blinds] 1st place</b> in <a href="https://www.youtube.com/watch?v=sdZUG7mFNM0&t=6s">Google Coral-board Challenge</a>.
description: My team (Jupyo, Sehyun, Dongik and me) took 1st place in Google Coral-baord Competition 2022.😄
img: assets/img/awards/231031_coralboard/coralboard-award.jpg
importance: 3
# category: work
related_publications: false
---

### <b>Ambient AI Bootcamp & Competition</b>   

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/coralboard-award.jpg" title="award" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    <iframe src="https://drive.google.com/file/d/1nrZ772JX_iV1et_t5Ufu2LcuKqayzHjC/preview" width="640" height="480" allow="autoplay"></iframe>
    <p>Navible demo video.</p>
</div>

<div class="caption">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/rzmtgCsuhdI?si=SU30K1621cC6xKsb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    <p>Navible presentation video. <a href="https://docs.google.com/presentation/d/1TuugeDejNbxHjk7PxlzHsoxGEJME4_qQ/edit?usp=sharing&ouid=102642115745426098221&rtpof=true&sd=true">[slides]</a></p>
</div>

##### <b>[Competetion description]</b>
- Develop a Coral board AI application with a free topic in 3 weeks.  
- Host: SNU GSDS.    
- Sponsorship: Google Coral AI.  


##### <b>[Proposed Solution]</b>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/navible-scenario.png" title="scenario" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    NaviBl Scenario:
    <p>Provide the visually impaired with correct directional guidance and hazard alerts based on real-time traffic conditions,  
    leveraging a Coral board and auditory feedback.</p>
    </div> 
</div>

To support a real-time scenario, we adopt the following strategies:
- **Light-weight Models**: We applied 8-bit quantization to two YOLOv5-based detection models and converted them to EdgeTPU-compatible formats to run on the Coral board.
- **Efficient Resource Scheduling**: Prioritized scheduling for vehicle detection (2.5 fps) and crosswalk/traffic light detection (1 fps).
- **Computation Minimization**: Reduce computation for feedback operations based on priority.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/system-design-navible.png" title="scenario" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    [Starategy 1 and 2] Light-weight model and system design for NaviBl with an efficient resource scheduling.
    </div>     
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/navible-algorithm.png" title="scenario" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">    
    [Starategy 3] Priority based feedback algorithm.
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/navible-prototype.png" title="scenario" class="img-fluid rounded z-depth-1" %}
    </div>    
    <div class="caption">    
    [Prototypes]: Wearable device for Navible
    </div>
</div>

##### <b>[Results]</b>
<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/coral-summary.png" title="performance" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Summary of Navible system performance.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/awards/231031_coralboard/coral-feedback.png" title="feedback" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Feedbacks to Google Coral.
</div>
