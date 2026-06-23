---
layout: page
permalink: /members/
title: members
description: The Dynamics and Control Lab at the University of South Carolina.
nav: true
nav_order: 2
---

<style>
  .members-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 1.5rem;
    margin-bottom: 2rem;
  }
  .member-card { text-align: center; }
  .member-photo {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50%;
    margin: 0 auto 0.75rem;
    display: block;
  }
  .member-name { font-weight: 600; line-height: 1.2; }
  .member-degree { font-size: 0.85rem; color: var(--global-text-color-light); }
  .member-bio { font-size: 0.9rem; margin: 0.5rem 0 0.35rem; }
  .member-topic { font-size: 0.85rem; color: var(--global-text-color-light); }
</style>

{% assign groups = "Director,Ph.D. Candidate,Undergraduate Researchers,Alumni" | split: "," %}
{% for g in groups %}
  {% assign people = site.data.members | where: "group", g %}
  {% if people.size > 0 %}
<h2>{{ g }}</h2>
<div class="members-grid">
  {% for m in people %}
  <div class="member-card">
    <img class="member-photo" src="{{ m.image | relative_url }}" alt="{{ m.name }}" loading="lazy">
    <div class="member-name">{{ m.name }}</div>
    {% if m.degree %}<div class="member-degree">{{ m.degree }}</div>{% endif %}
    <p class="member-bio">{{ m.bio }}</p>
    {% if m.topic %}<div class="member-topic"><strong>Research:</strong> {{ m.topic }}</div>{% endif %}
  </div>
  {% endfor %}
</div>
  {% endif %}
{% endfor %}
