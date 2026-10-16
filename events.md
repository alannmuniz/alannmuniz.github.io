---
layout: page
title: Events
eyebrow: Meetings and conferences
description: Conferences, workshops, and academic programmes in which I have participated as an organizer, speaker, or attendee.
permalink: /events/
---

<style>
.event .event-role {
  margin-top: 0.35rem;
  color: var(--ink);
  font-size: 0.95rem;
}
</style>

## Upcoming

<div class="event-list">
{% for event in site.data.events.upcoming %}
  <article class="event">
    <div>
      <h3>{% if event.url %}<a href="{{ event.url | escape }}">{{ event.title | escape }}</a>{% else %}{{ event.title | escape }}{% endif %}</h3>
      <p>{{ event.date | escape }}{% if event.location %} · {{ event.location | escape }}{% endif %}</p>
      {% if event.role %}<p class="event-role"><strong>Role:</strong> {{ event.role | escape }}</p>{% endif %}
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
      <h3>{% if event.url %}<a href="{{ event.url | escape }}">{{ event.title | escape }}</a>{% else %}{{ event.title | escape }}{% endif %}</h3>
      <p>{{ event.date | escape }}{% if event.location %} · {{ event.location | escape }}{% endif %}</p>
      {% if event.role %}<p class="event-role"><strong>Role:</strong> {{ event.role | escape }}</p>{% endif %}
    </div>
  </article>
{% endfor %}
</div>
