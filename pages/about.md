---
title: About
layout: page-narrow
permalink: /about.html
---

{% include feature/jumbotron.html objectid="/objects/syringacover.jpg" %} 

## The Affordable Communities Project

The Affordable Communities Project started with research with residents in Syringa Mobile Home Park, who faced water contamination then involuntary relocation as a result of community closure in June 2018. In 2024 Dr. Leontina Hormel's book [*Trailer Park America: Reimagining Working-Class Communities*](https://www.rutgersuniversitypress.org/trailer-park-america/9781978829466/), which includes a Foreword chapter written by grassroots community activist and University of Idaho alumna Dawn Tachell, was published. 

This website is a culmination of resources collected from Syringa's experiences and the ongoing dilemmas of shrinking housing affordability and access to living within sustainable communities. This site is built for those who wish to learn with these resources and to collaborate toward solutions to these social issues affecting Idaho, the Northwest, and beyond. 

The Affordable Communities Project presents research surrounding housing crises and ideas for securing affordable, stable, and healthy communities in Moscow, the state of Idaho, across the country, and globally. It is meant to offer resources for studying threats to working-class communities and the different forms of housing that are imagined for addressing housing scarcity for families.

------
{:.narrow-content .mb-5}

## People

<div class="narrow-content mt-3">
{% assign core = site.data.people | where: 'group','Core' %}
{% for p in core %}
<div class="d-flex mb-2">
  <div class="flex-shrink-0">
    <img style="max-width: 200px" class="img-fluid mt-2 rounded" src="{{ p.image_thumb | relative_url }}" alt="{{ p.name }}">
  </div>
  <div class="flex-grow-1 ms-3">
    <h3>{{ p.name }}</h3>
    <p class="h5">{{ p.role }} ({{ p.dates }})</p>
    <p>{{ p.biography }}</p>
  </div>
</div>
{% endfor %}
</div>

## Other Collaborators
{% assign others = site.data.people | where_exp: 'g', 'g.group != "Core"' %}
{% for p in others %}
- {{ p.name }}, {{ p.major }}, {{ p.dates }}{% endfor %}
