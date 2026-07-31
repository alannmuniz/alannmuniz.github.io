---
layout: page
title: Publications
eyebrow: Papers and preprints
description: Published articles, current preprints, and selected related work.
permalink: /publications/
---

## Preprints

{% for paper in site.data.preprints %}
  {% include publication.html item=paper %}
{% endfor %}

## Published articles

{% for paper in site.data.publications %}
  {% include publication.html item=paper %}
{% endfor %}

## Other contributions

- Contribution to *BRIDGES Lectures: G2 in action, and a mathematical theory of exceptions* by Laurent Manivel. [arXiv](https://arxiv.org/abs/2508.12757)
- Appendix to *Logarithmic sheaves of complete intersections* by Daniele Faenzi, Marcos Jardim, and Jean Vallès. [Journal page](https://journals.sns.it/index.php/annaliscienze/article/view/6128)

## PhD thesis

- *Polynomial bounds for automorphism groups of foliations*, under the supervision of Maurício Corrêa at UFMG.
