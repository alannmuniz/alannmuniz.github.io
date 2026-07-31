---
layout: page
title: CV
eyebrow: Curriculum vitae
description: Professional profile, selected talks, and links.
permalink: /cv/
---

## Current position

Professor, Department of Mathematics, Centro de Ciências Exatas e da Natureza, Universidade Federal de Pernambuco.

## Curriculum

My complete academic curriculum is available through the Brazilian Lattes Platform.

<a class="button primary" href="{{ site.lattes_url }}">Open Lattes CV</a>

## Selected presentations

{% for talk in site.data.talks %}
<div class="talk">
  <h3>{{ talk.title }}</h3>
  <p>
    {% if talk.slides %}<a href="{{ talk.slides }}">Slides</a>{% endif %}
    {% if talk.video %}<span aria-hidden="true"> · </span><a href="{{ talk.video }}">Video</a>{% endif %}
  </p>
</div>
{% endfor %}

## Useful links

- [MathOverflow](https://mathoverflow.net/)
- [Mathematics Stack Exchange](https://math.stackexchange.com/)
- [arXiv](https://arxiv.org/)
- [zbMATH Open](https://zbmath.org/)
- [MathSciNet](https://mathscinet.ams.org/mathscinet/)
- [Upcoming conferences in algebraic geometry](https://math.stanford.edu/~vakil/conferences.html)
