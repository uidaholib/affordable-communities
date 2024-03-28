---
title: About
layout: about
permalink: /about.html
---

{% include feature/jumbotron.html objectid="/objects/syringacover.jpg" %} 

{% include feature/nav-menu.html sections="The Affordable Communities Project;People" %}

## The Affordable Communities Project

The Affordable Communities Project started with research with residents in Syringa Mobile Home Park, who faced water contamination then involuntary relocation as a result of community closure in June 2018. In 2024 Dr. Leontina Hormel's book Trailer Park America: Reimagining Working-Class Communities, which includes a Foreword chapter written by grassroots community activist and UI alumna Dawn Tachell, was published. This website is a culmination of resources collected from Syringa's experiences and the ongoing dilemmas of shrinking housing affordability and access to living within sustainable communities. This site is built for those who wish to learn with these resources and to collaborate toward solutions to these social issues affecting Idaho, the Northwest, and beyond. 

The Affordable Communities Project presents research surrounding housing crises and ideas for securing affordable, stable, and healthy communities in Moscow, the state of Idaho, across the country, and globally. It is meant to offer resources for studying threats to working-class communities and the different forms of housing that are imagined for addressing housing scarcity for families.

Dr. Leontina Hormel is a Professor of Sociology at the University of Idaho, who has conducted community research for over two decades. This website brings together materials and discussions about affordable housing community development in the city of Moscow, the state of Idaho, across the United States, and elsewhere globally. 

The roots of this particular community development project site were established in Hormel's community action project with Syringa Mobile Home Park residents. From 2015 through 2018 she worked with and documented Syringa residents' experiences with water contamination and their efforts to improve their safety and living conditions in their community. Unfortunately, despite efforts to save their homes, residents were forced to relocate from Syringa when the park closed June 5, 2018. Syringa was constructed in the 1960s just three miles outside of Moscow, Idaho in Latah County. The park closed after several years of the park owner's insufficient in the water and wastewater disposal systems. 

The closure of the park brought on the mass-eviction of several working-class people and families. The case of Syringa helps highlight the need for affordable housing in the state of Idaho and across the nation. 

## People

{% assign core = site.data.people | where: 'group','Core' %}
{% for p in core %}
<div class="d-flex m-2">
  <div class="flex-shrink-0">
    <img style="max-width: 200px" class="img-fluid m-2 rounded" src="{{ p.image_thumb | relative_url }}" alt="{{ p.name }}">
  </div>
  <div class="flex-grow-1 ms-3">
    <h3>{{ p.name }}, {{ p.role }} ({{ p.dates }})</h3>
    <p>{{ p.biography }}</p>
  </div>
</div>
{% endfor %}

## Other Collaborators
{% assign others = site.data.people | where_exp: 'g', 'g.group != "Core"' %}
{% for p in others %}
- {{ p.name }}, {{ p.major }}, {{ p.dates }}{% endfor %}
