---
layout: page
title: TravNet
description: Using computer vision to automate spike-sorting - saving hours per day!
img: assets/img/projects/TravNet_repo.jpg
importance: 1
category: work
related_publications: true
---

One of the time consuming steps in acquiring electrophysiology data is the sorting of the signals from noise. This process typically takes hours each day, and as more channels are added to electrodes this problem is expanding explonentially. In the past half-century many methods have been attempted to solve this problem, all requiring some mathematical representation of waveform template matching. 

This project takes a different strategy - instead of trying to perfectly match waveform, it tries to match expert humans in the field at sorting. In other words, we create an AI agent that can sort neurons with expert performance, then automate the task. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/clusters.jpg" title="expert sorting" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/color_image.jpg" title="file structure for color image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/Waveblob.jpg" title="waveform represented in image file format" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The typical procedure is for a human to process the raw waveforms, cluster with principal componenets and circle the neurons based on experience. We used the traditional image-file format of a shape and 3 layers (RGB) and instead created a new form: a Waveblob that consists of the neural waveform, and at each location we put the value of the principal component (PC1, PC2, PC3 for RGB).
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/performance.jpg" title="expert performance" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    TravNet sorts neurons 85% as well as an expert! How accurate could you resort spikes ;-)
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.