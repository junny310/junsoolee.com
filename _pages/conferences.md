---
layout: page
permalink: /conferences/
title: Conferences
description: A running list of conferences relevant to the Dynamics and Control Lab — control systems, robotics and autonomy, and machine learning. Submission deadlines change year to year; please confirm dates on each conference's official site.
nav: true
nav_order: 5
---

{% assign confs = site.data.conferences | sort: "start" %}
{% assign year_groups = confs | group_by: "year" %}
{% assign cats = "Control Systems,Robotics & Autonomous Systems,Machine Learning & AI" | split: "," %}

{% for yg in year_groups %}
<h2>{{ yg.name }}</h2>
{% for cat in cats %}
{% assign items = yg.items | where: "category", cat %}
{% if items.size > 0 %}
<h3>{{ cat }}</h3>
<div class="table-responsive">
  <table class="table table-sm">
    <thead>
      <tr><th>Conference</th><th>Dates</th><th>Location</th></tr>
    </thead>
    <tbody>
      {% for c in items %}
      <tr>
        <td><a href="{{ c.url }}" target="_blank" rel="noopener noreferrer">{{ c.name }}</a> — {{ c.full_name }}</td>
        <td>{{ c.dates }}</td>
        <td>{{ c.location }}</td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</div>
{% endif %}
{% endfor %}
{% endfor %}

<h2>2027</h2>

<p>Dates and locations for the next cycle are announced on a rolling basis. The lab typically targets the same venues — <strong>ACC</strong>, <strong>ECC</strong>, <strong>CDC</strong>, and <strong>CCTA</strong> (control); <strong>ICRA</strong> and <strong>IROS</strong> (robotics); and <strong>ICML</strong>, <strong>NeurIPS</strong>, <strong>ICLR</strong>, and <strong>AAAI</strong> (machine learning) — along with <strong>MED</strong> (Mediterranean Conference on Control and Automation). Check each conference's website for the latest call for papers.</p>
