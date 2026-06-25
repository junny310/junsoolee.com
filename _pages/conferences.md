---
layout: page
permalink: /conferences/
title: Conferences
description: A running list of conferences relevant to the Dynamics and Control Lab — control systems, robotics and autonomy, and machine learning. Submission deadlines change year to year; please confirm dates on each conference's official site.
nav: true
nav_order: 7
---

{% assign confs = site.data.conferences | sort: "start" %}
{% assign year_groups = confs | group_by: "year" %}
{% assign cats = "Control Systems,Aerospace & Mechanical,Robotics & Autonomous Systems,Machine Learning & AI" | split: "," %}

{% for yg in year_groups %}
<h2>{{ yg.name }}</h2>
{% for cat in cats %}
{% assign items = yg.items | where: "category", cat %}
{% if items.size > 0 %}
<h3>{{ cat }}</h3>
<div class="table-responsive">
  <table class="table table-sm">
    <thead>
      <tr><th>Conference</th><th>Dates</th><th>Location</th><th>Deadline</th></tr>
    </thead>
    <tbody>
      {% for c in items %}
      <tr>
        <td>{% if c.url %}<a href="{{ c.url }}" target="_blank" rel="noopener noreferrer">{{ c.name }}</a>{% else %}{{ c.name }}{% endif %} — {{ c.full_name }}</td>
        <td>{{ c.dates }}</td>
        <td>{{ c.location }}</td>
        <td>{{ c.deadline | default: "TBD" }}</td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</div>
{% endif %}
{% endfor %}
{% endfor %}

<h2>Other venues we follow</h2>

<p>Beyond the editions listed above, the lab also regularly targets <strong>CDC</strong>, <strong>CCTA</strong>, <strong>L4DC</strong>, and <strong>MED</strong> (control); <strong>AIAA SciTech</strong> and <strong>IMECE</strong> (aerospace &amp; mechanical); <strong>ICRA</strong> and <strong>IROS</strong> (robotics); and <strong>ICML</strong>, <strong>NeurIPS</strong>, <strong>ICLR</strong>, and <strong>AAAI</strong> (machine learning). New editions are announced on a rolling basis — check each conference's website for the latest call for papers.</p>
