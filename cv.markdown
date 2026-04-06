---
layout: default
title: Curriculum Vitae
---

<h2>Education</h2>

<ul>
  {% for item in site.data.education %}
    <li>
      <strong>{{ item.degree }}</strong>, {{ item.institution }}
      ({{ item.time }})
      {% if item.details %}
        <br><em>{{ item.details }}</em>
      {% endif %}
    </li>
  {% endfor %}
</ul>

<h2>Teaching assistant</h2>

<ul class="ta-list">
{% for activity in site.data.teaching_assistant %}
  <li>
    <div class="ta-course"><strong>{{ activity.course }}</strong></div>
    <div class="ta-details">
      {{ activity.institution }} — {{ activity.period }} — {{ activity.language }}
    </div>
  </li>
{% endfor %}
</ul>

