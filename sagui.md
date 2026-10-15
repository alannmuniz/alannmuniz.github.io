---
layout: page
title: SAGüi
eyebrow: Seminário de Álgebra e Geometria
description: Seminário do grupo de Álgebra Comutativa e Geometria Algébrica do Departamento de Matemática da UFPE.
permalink: /sagui/
lang: pt-BR
---

<style>
  .sagui-page { overflow-wrap: anywhere; }
  .sagui-page [hidden] { display: none !important; }
  .sagui-contact { margin-bottom: 2rem; }
  .sagui-intro { color: var(--muted); }
  .sagui-years { display: flex; flex-wrap: wrap; gap: .65rem; margin: 1.5rem 0 2.5rem; }
  .sagui-years a { border: 1px solid var(--line); border-radius: 999px; padding: .35rem .9rem; text-decoration: none; font-weight: 700; }
  .sagui-page h2 { font-size: clamp(1.8rem, 4vw, 2.5rem); }
  .sagui-year { margin-top: 2.5rem; scroll-margin-top: 6rem; }
  .sagui-year > h3 { color: var(--green); font-size: 1.7rem; padding-bottom: .75rem; border-bottom: 1px solid var(--line); }
  .sagui-entry { display: grid; grid-template-columns: 3.5rem minmax(0, 1fr); gap: 1rem; padding: 1.5rem 0; border-bottom: 1px solid var(--line); scroll-margin-top: 6rem; }
  .sagui-entry h4 { margin: 0 0 .4rem; font-family: Georgia, "Times New Roman", serif; font-size: 1.3rem; line-height: 1.3; }
  .sagui-speaker { margin-bottom: .65rem; font-weight: 700; }
  .sagui-speaker span { color: var(--muted); font-weight: 400; }
  .sagui-meta { display: flex; flex-wrap: wrap; gap: .2rem 1rem; color: var(--muted); font-size: .94rem; }
  .sagui-meta time { font-weight: 600; }
  .sagui-status { display: inline-block; margin-bottom: .65rem; padding: .2rem .7rem; border-radius: 999px; color: var(--green); background: var(--cream); font-size: .78rem; font-weight: 800; }
  .sagui-upcoming { margin: 2rem 0 3.5rem; }
  .sagui-upcoming .sagui-entry { margin-top: 1rem; padding: 1.5rem; border: 1px solid var(--line); border-radius: var(--radius); background: white; box-shadow: var(--shadow); }
  .sagui-abstract { margin-top: 1rem; }
  .sagui-abstract summary { cursor: pointer; color: var(--green); font-weight: 700; }
  .sagui-abstract p { margin: .8rem 0 0; }
  .sagui-abstract-body { font-size: 1rem; line-height: 1.7; }
  .sagui-abstract-body li { margin-bottom: .4rem; }
  .sagui-abstract-body mjx-container[display="true"] { max-width: 100%; overflow-x: auto; overflow-y: hidden; }
  @media (max-width: 620px) {
    .sagui-entry { grid-template-columns: 1fr; gap: .4rem; }
    .sagui-meta { flex-direction: column; }
    .sagui-upcoming .sagui-entry { padding: 1.1rem; }
  }
</style>

<div class="sagui-page" id="sagui-programme">
  <p class="sagui-contact">Os encontros acontecem no DMat–UFPE, em Recife. Para receber os anúncios das próximas palestras, <a href="mailto:{{ site.email }}?subject=Lista%20de%20divulga%C3%A7%C3%A3o%20do%20SAG%C3%BCi">envie um e-mail para entrar na lista de divulgação</a>.</p>
  <p class="sagui-intro">{{ site.data.sagui | size }} edições anunciadas desde 2024.</p>

  <section class="sagui-upcoming" id="sagui-upcoming" aria-labelledby="sagui-upcoming-heading" hidden>
    <h2 id="sagui-upcoming-heading">Próxima palestra</h2>
    <div id="sagui-upcoming-list"></div>
  </section>

  <section class="sagui-archive" aria-labelledby="sagui-archive-heading">
    <h2 id="sagui-archive-heading">Programação e histórico</h2>
    <nav class="sagui-years" aria-label="Navegar por ano">
      {% assign previous_year = "" %}
      {% for talk in site.data.sagui reversed %}
        {% assign talk_year = talk.year | append: "" %}
        {% unless talk_year == previous_year %}
          <a href="#sagui-{{ talk_year }}" data-sagui-year-link="{{ talk_year }}">{{ talk_year }}</a>
          {% assign previous_year = talk_year %}
        {% endunless %}
      {% endfor %}
    </nav>

    {% assign previous_year = "" %}
    {% for talk in site.data.sagui reversed %}
      {% assign talk_year = talk.year | append: "" %}
      {% unless talk_year == previous_year %}
        {% unless forloop.first %}</div></section>{% endunless %}
        <section class="sagui-year" id="sagui-{{ talk_year }}" data-sagui-year="{{ talk_year }}" aria-labelledby="sagui-year-heading-{{ talk_year }}">
          <h3 id="sagui-year-heading-{{ talk_year }}">{{ talk_year }}</h3>
          <div class="sagui-year-list" data-sagui-year-list="{{ talk_year }}">
        {% assign previous_year = talk_year %}
      {% endunless %}

      <article class="sagui-entry" id="sagui-talk-{{ talk.number }}" data-sagui-date="{{ talk.date }}" data-sagui-year-value="{{ talk.year }}" aria-labelledby="sagui-title-{{ talk.number }}">
        <div class="seminar-number">#{{ talk.number }}</div>
        <div>
          <span class="sagui-status" hidden>Próxima palestra</span>
          <h4 id="sagui-title-{{ talk.number }}">{{ talk.title | escape }}</h4>
          <p class="sagui-speaker">{{ talk.speaker | escape }} <span>({{ talk.affiliation | escape }})</span></p>
          <div class="sagui-meta">
            <time datetime="{{ talk.date }}">{{ talk.date_label }}</time>
          </div>
          {% if talk.abstract %}
          <details class="sagui-abstract">
            <summary aria-label="Resumo da palestra de {{ talk.speaker | escape }}">Resumo</summary>
            <div class="sagui-abstract-body">{{ talk.abstract }}</div>
          </details>
          {% endif %}
          {% if talk.poster %}
          <p><a href="{{ talk.poster | relative_url }}">Cartaz da palestra #{{ talk.number }} (PDF)</a></p>
          {% endif %}
        </div>
      </article>
    {% endfor %}
    {% if site.data.sagui.size > 0 %}</div></section>{% endif %}
  </section>
</div>

<script>
(() => {
  const programme = document.getElementById('sagui-programme');
  if (!programme) return;
  const upcoming = document.getElementById('sagui-upcoming');
  const upcomingList = document.getElementById('sagui-upcoming-list');
  const entries = Array.from(programme.querySelectorAll('[data-sagui-date]'));

  function updateProgramme() {
    // Use the seminar's local date; the archive remains current between Jekyll builds.
    const parts = new Intl.DateTimeFormat('en', {
      timeZone: 'America/Sao_Paulo', year: 'numeric', month: '2-digit', day: '2-digit'
    }).formatToParts(new Date());
    const date = Object.fromEntries(parts.map(part => [part.type, part.value]));
    const today = `${date.year}-${date.month}-${date.day}`;
    const future = [];

    entries.sort((a, b) => b.dataset.saguiDate.localeCompare(a.dataset.saguiDate));
    entries.forEach(entry => {
      const isUpcoming = entry.dataset.saguiDate >= today;
      entry.querySelector('.sagui-status').hidden = !isUpcoming;
      if (isUpcoming) {
        future.push(entry);
      } else {
        programme.querySelector(`[data-sagui-year-list="${entry.dataset.saguiYearValue}"]`).append(entry);
      }
    });
    future.sort((a, b) => a.dataset.saguiDate.localeCompare(b.dataset.saguiDate));
    future.forEach(entry => upcomingList.append(entry));
    upcoming.hidden = future.length === 0;
    document.getElementById('sagui-upcoming-heading').textContent = future.length === 1 ? 'Próxima palestra' : 'Próximas palestras';
    programme.querySelectorAll('[data-sagui-year]').forEach(section => {
      const empty = !section.querySelector('.sagui-entry');
      section.hidden = empty;
      programme.querySelector(`[data-sagui-year-link="${section.dataset.saguiYear}"]`).hidden = empty;
    });
    document.getElementById('sagui-archive-heading').textContent = 'Histórico de palestras';
  }

  updateProgramme();
  window.addEventListener('pageshow', updateProgramme);
  document.addEventListener('visibilitychange', () => {
    if (!document.hidden) updateProgramme();
  });
  programme.querySelectorAll('.sagui-abstract').forEach(details => {
    details.addEventListener('toggle', () => {
      if (details.open && window.MathJax && window.MathJax.typesetPromise) {
        window.MathJax.startup.promise.then(() => window.MathJax.typesetPromise([details])).catch(() => {});
      }
    });
  });
})();
</script>

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
