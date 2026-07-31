---
layout: page
title: Events
eyebrow: Meetings and conferences
description: Mathematical meetings connected with my academic activities.
permalink: /events/
---

## Upcoming

<div class="event-list">
{% for event in site.data.events.upcoming %}
  <article class="event">
    <div>
      <h3>{% if event.url %}<a href="{{ event.url }}">{{ event.title }}</a>{% else %}{{ event.title }}{% endif %}</h3>
      <p>{{ event.date }}{% if event.location %} · {{ event.location }}{% endif %}</p>
    </div>
    <span class="event-status">Upcoming</span>
  </article>
{% endfor %}
</div>

## Past meetings

<div class="event-list">
{% for event in site.data.events.past %}
  <article class="event">
    <div>
      <h3>{% if event.url %}<a href="{{ event.url }}">{{ event.title }}</a>{% else %}{{ event.title }}{% endif %}</h3>
      {% if event.date %}<p>{{ event.date }}</p>{% endif %}
    </div>
  </article>
{% endfor %}
</div>
