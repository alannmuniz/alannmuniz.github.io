---
layout: page
title: CV
eyebrow: Curriculum vitae
description: Academic appointments, education, supervision, fellowships, and service.
permalink: /cv/
---

<style>
  .cv-actions { display: flex; flex-wrap: wrap; gap: .75rem; align-items: center; margin-bottom: 1rem; }
  .cv-updated, .cv-detail { color: var(--muted); }
  .cv-updated { font-size: .9rem; }
  .cv-navigation { display: flex; flex-wrap: wrap; gap: .45rem 1rem; margin: 1.5rem 0 2.5rem; font-size: .92rem; }
  .cv-entry { display: grid; grid-template-columns: 7.5rem minmax(0, 1fr); gap: 1.25rem; padding: 1.25rem 0; border-bottom: 1px solid var(--line); }
  .cv-period { color: var(--green); font-weight: 700; }
  .cv-entry h3 { margin-bottom: .4rem; font-size: 1.22rem; }
  .cv-entry p { margin-bottom: .4rem; }
  .cv-entry p:last-child { margin-bottom: 0; }
  .cv-list li { margin-bottom: .85rem; }
  .prose > h2[id] { scroll-margin-top: 6.5rem; }
  @media (max-width: 620px) {
    .cv-entry { grid-template-columns: 1fr; gap: .4rem; }
    .cv-actions .button { flex: 1 1 12rem; }
  }
</style>

<div class="cv-actions">
  <a class="button primary" href="{{ '/assets/files/alan-muniz-cv.pdf' | relative_url }}" download="Alan-Muniz-CV.pdf">Download CV (PDF)</a>
  <a class="button secondary" href="{{ site.lattes_url }}">Lattes CV</a>
  <a href="https://orcid.org/0000-0003-1844-2790" rel="me">ORCID</a>
</div>
<p class="cv-updated">Page updated 15 October 2026.</p>

<nav class="cv-navigation" aria-label="CV sections">
  <a href="#current-position">Current position</a>
  <a href="#education">Education</a>
  <a href="#appointments">Previous appointments</a>
  <a href="#fellowships">Fellowships</a>
  <a href="#supervision">Supervision</a>
  <a href="#talks">Invited talks</a>
  <a href="#service">Academic service</a>
  <a href="#presentations">Slides and recordings</a>
</nav>

<h2 id="current-position">Current position</h2>

<p><strong>Assistant Professor, Universidade Federal de Pernambuco (UFPE)</strong>, since 2024.<br>
Department of Mathematics, Centro de Ciências Exatas e da Natureza, Recife, Brazil.</p>
<p><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>

<h2 id="education">Education</h2>

<div class="cv-entry">
  <div class="cv-period">2012–2016</div>
  <div>
    <h3>Ph.D. in Mathematics</h3>
    <p>Universidade Federal de Minas Gerais (UFMG), Belo Horizonte, Brazil.</p>
    <p class="cv-detail">Algebraic geometry and holomorphic foliations.<br>
    Thesis: <em>Polynomial Bounds for Automorphism Groups of Foliations</em>.<br>
    Advisor: Maurício Corrêa.</p>
  </div>
</div>
<div class="cv-entry">
  <div class="cv-period">2010–2012</div>
  <div>
    <h3>Master’s degree in Mathematics</h3>
    <p>Universidade Federal Fluminense (UFF), Niterói, Brazil.</p>
    <p class="cv-detail">Thesis: <em>Integrais primeiras de folheações holomorfas</em>.<br>
    Advisor: Thiago Fassarella.</p>
  </div>
</div>
<div class="cv-entry">
  <div class="cv-period">2006–2010</div>
  <div>
    <h3>Licentiate degree in Mathematics</h3>
    <p>Universidade do Estado do Rio de Janeiro (UERJ), Brazil.</p>
  </div>
</div>

<h2 id="appointments">Previous appointments</h2>

<div class="cv-entry">
  <div class="cv-period">2022–2023</div>
  <div><h3>Postdoctoral researcher</h3><p>Universidade Estadual de Campinas (UNICAMP), Campinas, Brazil.</p><p class="cv-detail">Supervisor: Marcos Jardim.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2021–2022</div>
  <div><h3>Postdoctoral researcher</h3><p>Université de Bourgogne, Dijon, France.</p><p class="cv-detail">Supervisor: Daniele Faenzi.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2018–2019</div>
  <div><h3>Postdoctoral researcher</h3><p>Universidade Federal do Espírito Santo (UFES), Vitória, Brazil.</p><p class="cv-detail">Supervisor: Leonardo Câmara.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2017–2018</div>
  <div><h3>Temporary professor</h3><p>Universidade Federal Fluminense (UFF), Brazil.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2016–2018</div>
  <div><h3>Postdoctoral researcher</h3><p>Universidade Federal Fluminense (UFF), Niterói, Brazil.</p><p class="cv-detail">Supervisor: Thiago Fassarella.</p></div>
</div>

<h2 id="fellowships">Fellowships</h2>

<ul class="cv-list">
  <li><strong>CNPq Research Productivity Fellowship, Level C.</strong> Grant 305599/2026-7.</li>
  <li><strong>INCTMat Postdoctoral Fellowship.</strong> CNPq grant 160934/2022-2.</li>
  <li><strong>CAPES–COFECUB Postdoctoral Fellowship.</strong> Fellowship 88887.468856/2019-00, project 88887.191919/2018-00.</li>
  <li><strong>PNPD/CAPES Postdoctoral Fellowships.</strong> November 2016–October 2018 and November 2018–October 2019.</li>
  <li><strong>CAPES–REUNI Doctoral Scholarship.</strong> March 2012–February 2016.</li>
  <li><strong>CAPES Master’s Scholarship.</strong> March 2010–February 2012.</li>
</ul>

<h2 id="supervision">Supervision</h2>

<h3>Doctoral students</h3>
<div class="cv-entry">
  <div class="cv-period">2026–present</div>
  <div><h3>Mateus Ferreira de Melo</h3><p>Universidade Federal de Pernambuco.</p><p class="cv-detail"><em>Decidability in the class of tame henselian fields.</em></p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2024–present</div>
  <div><h3>Pedro Pfarrius Barbassa</h3><p>Universidade Estadual de Campinas.</p><p class="cv-detail"><em>Moduli spaces of distributions on projective spaces.</em><br>Co-advised with Marcos Jardim.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2022–present</div>
  <div><h3>Victor Zaher</h3><p>Universidade Estadual de Campinas.</p><p class="cv-detail"><em>Folheações por curvas no espaço projetivo.</em><br>Co-advised with Marcos Jardim.</p></div>
</div>

<h3>Master’s students</h3>
<div class="cv-entry">
  <div class="cv-period">2026–present</div>
  <div><h3>Gabriel Luz Pachêco</h3><p>Universidade Federal de Pernambuco.</p><p class="cv-detail"><em>Estruturas de Engel em Variedades Complexas: Análise Local e Global.</em></p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2023–2024</div>
  <div><h3>Pedro Pfarrius Barbassa</h3><p>Universidade Estadual de Campinas.</p><p class="cv-detail"><em>Esquema singular de folheações por curvas.</em><br>Co-advised with Marcos Jardim.</p></div>
</div>

<h2 id="publications">Publications</h2>

<p>See the <a href="{{ '/publications/' | relative_url }}">publications page</a> for articles, preprints, and links to arXiv and journal versions.</p>

<h2 id="talks">Selected invited talks and lectures</h2>

<div class="cv-entry">
  <div class="cv-period">2025</div>
  <div><h3>Foliations on Complete Intersections</h3><p class="cv-detail">Foliations, Complex Geometry, and Painlevé Equations, IMPA, Rio de Janeiro, Brazil.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2024</div>
  <div><h3>Foliations on Homogeneous Spaces</h3><p class="cv-detail">From Schubert Calculus to Representation Theory, Universidade Federal de Sergipe, Aracaju, Brazil.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2024</div>
  <div><h3>Distribuições em Espaços Projetivos</h3><p class="cv-detail">Invited lectures, Programa de Verão, Universidade Federal Fluminense, Niterói, Brazil.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2023</div>
  <div><h3>Distribution and syzygies</h3><p class="cv-detail">Bandoleros 2023, Università di Torino, Turin, Italy.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2022</div>
  <div><h3>On the moduli space of rank two logarithmic connections over an elliptic curve</h3><p class="cv-detail">Séminaire de Géométrie Analytique, Université de Rennes, Rennes, France.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2022</div>
  <div><h3>Codimension one Foliations on Homogeneous Spaces</h3><p class="cv-detail">Séminaire de Géométrie Algébrique, Université de Lille, Lille, France.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2022</div>
  <div><h3>Moduli of Distributions via Singular Schemes</h3><p class="cv-detail">Seminari di Matematica, Università di Bari, Bari, Italy.</p></div>
</div>
<div class="cv-entry">
  <div class="cv-period">2018</div>
  <div><h3>Simetrias de foliaciones en el plano proyectivo</h3><p class="cv-detail">III Congreso Internacional de Geometría y Dinámica Compleja, Pontificia Universidad Católica del Perú, Lima, Peru.</p></div>
</div>

<h2 id="service">Academic service</h2>

<ul class="cv-list">
  <li><strong>CNPq research project evaluator.</strong> Since 2026.</li>
  <li><strong>FACEPE research project evaluator.</strong> Since 2024.</li>
  <li><strong>SAGüi — Seminário de Álgebra e Geometria do DMat–UFPE.</strong> Co-organizer since 2024. <a href="{{ '/sagui/' | relative_url }}">Seminar archive</a>.</li>
  <li><strong>Scientific committee:</strong> 3rd International Meeting of Young Researchers in Singularity Theory and Related Fields, 2024.</li>
</ul>

<h2 id="presentations">Slides and recordings</h2>

{% for talk in site.data.talks %}
<div class="talk">
  <h3>{{ talk.title }}</h3>
  <p>
    {% if talk.slides %}<a href="{{ talk.slides }}">Slides</a>{% endif %}
    {% if talk.video %}<span aria-hidden="true"> · </span><a href="{{ talk.video }}">Video</a>{% endif %}
  </p>
</div>
{% endfor %}

<h2 id="useful-links">Useful links</h2>

<ul>
  <li><a href="https://mathoverflow.net/">MathOverflow</a></li>
  <li><a href="https://math.stackexchange.com/">Mathematics Stack Exchange</a></li>
  <li><a href="https://arxiv.org/">arXiv</a></li>
  <li><a href="https://zbmath.org/">zbMATH Open</a></li>
  <li><a href="https://mathscinet.ams.org/mathscinet/">MathSciNet</a></li>
  <li><a href="https://math.stanford.edu/~vakil/conferences.html">Upcoming conferences in algebraic geometry</a></li>
</ul>
