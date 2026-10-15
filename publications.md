---
layout: page
title: Publications
eyebrow: Papers and preprints
description: Published articles, current preprints, and selected related work.
permalink: /publications/
---

<style>
  .paper-description { margin-top: .7rem; color: var(--ink); font-size: 1rem; line-height: 1.55; }
  .other-contributions li { margin-bottom: 1.5rem; }
  .other-contributions p { margin-bottom: .4rem; }
</style>


## Preprints

{% for paper in site.data.preprints %}
  {% include publication.html item=paper %}
{% endfor %}

## Published articles

{% for paper in site.data.publications %}
  {% include publication.html item=paper %}
{% endfor %}

## Other contributions

<ul class="other-contributions">
  <li>
    <p>Contribution to <em>BRIDGES Lectures: G2 in action, and a mathematical theory of exceptions</em> by Laurent Manivel. <a href="https://arxiv.org/abs/2508.12757">arXiv</a></p>
    <p class="paper-description">Lecture notes on the geometry of G₂ and other exceptional complex Lie groups.</p>
  </li>
  <li>
    <p>Appendix to <em>Logarithmic sheaves of complete intersections</em> by Daniele Faenzi, Marcos Jardim, and Jean Vallès. <a href="https://journals.sns.it/index.php/annaliscienze/article/view/6128">Journal page</a></p>
    <p class="paper-description">Studies logarithmic tangent sheaves via Jacobian syzygies, including freeness, stability, and pencils of quadrics.</p>
  </li>
</ul>

## PhD thesis

- *Polynomial bounds for automorphism groups of foliations*, under the supervision of Maurício Corrêa at UFMG.
