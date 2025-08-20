---
layout: page
title: Emergence of cascading dynamics in interacting tipping elements of ecology and climate
description: Cascading tipping dynamics in coupled climate–ecological systems.
permalink: /projects/klose2020emergence/
img: assets/img/1DcuspManifold.png
importance: 4
category: work
tags: [climate, tipping, complex-systems]
related_publications: true
---


In this work, we investigate how **interacting tipping elements** in ecology and climate can give rise to cascading dynamics, where the tipping of one subsystem triggers others to follow. Examples of such tipping elements include the collapse of fish populations, dieback of tropical forests, and disintegration of ice sheets. When these systems are coupled, their nonlinear feedbacks can synchronize, amplify, or cascade across scales.

We model each subsystem as a **saddle-node bifurcation** described by  
$$
\dot{x}_i = -a_i(x_i - b_i)^3 + c_i + \sum_j d_{ij} x_j,
$$  
where $x_i$ represents the state of tipping element $i$, $a_i$ its nonlinearity, $b_i$ the critical threshold, $c_i$ an external forcing, and $d_{ij}$ coupling strengths between elements. In isolation, each system exhibits critical slowing down near the tipping point. When coupled, however, a tipping in one subsystem can act as an additional forcing on its neighbors, thereby inducing **domino effects**.

Our analysis combines **stochastic simulations**, **bifurcation theory**, and **network modeling** to identify generic conditions for cascading. We find that coupling strengths and network topology crucially determine whether tipping events remain localized or spread system-wide. In particular, a strongly connected network of elements is highly vulnerable to synchronized collapse once a critical density of tipping events has been reached.

One key result is the emergence of **hysteresis loops** in the coupled system: once a cascade has been triggered, reversing external forcing does not necessarily restore the system to its original state. This implies a profound loss of resilience in ecological and climate networks under anthropogenic stressors.  

These findings provide a theoretical framework for understanding **compound climate risks** and **ecological regime shifts**, emphasizing that early-warning signals in one subsystem can be precursors to far-reaching cascades. The work highlights the urgent need for integrated approaches that consider not just individual tipping points, but their interactions across Earth’s complex systems.
{% include figure.liquid path="assets/img/1DcuspManifold.png" alt="cusp catastrophe manifold illustrating tipping response" class="img-fluid rounded z-depth-1 mx-auto d-block" sizes="30vw" max-width="30%" title="Cusp manifold for interacting tipping elements" %}
<div class="d-none">{% cite klose2020emergence %}</div>
