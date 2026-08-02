---
layout: page
title: SAGüi
eyebrow: Seminário de Álgebra e Geometria
description: O SAGüi é um seminário quinzenal do grupo de Álgebra Comutativa e Geometria Algébrica do DMat–UFPE. Envie um e-mail para entrar na lista de divulgação. 
permalink: /sagui/
lang: pt-BR
---

<div class="seminar-list">
{% for talk in site.data.sagui reversed %}
  <article class="seminar-item">
    <div class="seminar-number">#{{ talk.number }}</div>
    <div>
      <h2>{{ talk.speaker }} <small>({{ talk.affiliation }})</small></h2>
      <p>{{ talk.title }}</p>
    </div>
  </article>
{% endfor %}
</div>
