---
layout: page
title: projects
permalink: /projects/
description: A growing collection of your cool projects.
nav: true
nav_order: 3
display_categories: [work]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>

## Current Projects

### SLATE: Scalable Localization And Tracking for Autonomous Parking Environment
* Designing Mixture of Scene Coordinate Experts for Visual Localization on large-scale datasets
* Proposal under review for the Austria–Korea Joint Mobility Program (2025–2027)

<img src="/images/MEAL.png" alt="MEAL Model" width="400"/>
<img src="/images/MEAL_Pipeline.png" alt="MEAL Pipeline" width="400"/>

### 4D Multi-Car Accident Reconstruction from Dashcam Footage
* Researching Multi-view Alignment methods for Dynamic 4D Scene Reconstruction
* Proposal under review for the Czech–Korea Joint Research Program (2025–2027)

<img src="/images/Pic.png" alt="4D Reconstruction" width="400"/>

## Past Projects

### Honeywell CO Detector
* Developed Arm Cortex-M3 MCU with integrated sensors for reliable CO detection.