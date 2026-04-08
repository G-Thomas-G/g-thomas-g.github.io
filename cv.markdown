---
layout: default
title: Curriculum Vitae
---

<div class="cv-page">

<section class="cv-section">
  <h2>Education</h2>

  <ul class="cv-list">
    {% for item in site.data.education %}
      <li class="cv-item">
        <div class="cv-main">
          <strong>{{ item.degree }}</strong>
          <span class="cv-institution">{{ item.institution }}</span>
        </div>
        <div class="cv-meta">
          ({{ item.time }})
          {% if item.supervisor %}
          Supervisor: {{ item. supervisor }}
          {% endif %}
        </div>
        {% if item.details %}
          <div class="cv-details">{{ item.details }}
          </div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<section class="cv-section">
  <h2>Teaching assistant (TA) and supervision</h2>

  <ul class="cv-list">
  {% for activity in site.data.teaching_assistant %}
    <li class="cv-item">
      <div class="cv-main">
        <strong>{{ activity.course }}</strong>
        <span class="ta-tag"> 
          {{ activity.tag }}
        </span>
      </div>
      <div class="cv-meta">
        {{ activity.institution }} — 
        <span title="{{ activity.detail-period }}">
        {{ activity.period }}
        </span> — {{ activity.language }}
      </div>
      {% if activity.details %}
      <div class="cv-details">
        {{ activity.details }}
      </div>
      {% endif %}
    </li>
  {% endfor %}
  </ul>
</section>



<section class="cv-section">
  <h2>Talks and Presentations</h2>
  <ul class="cv-list">
    {% for talk in site.data.presentations %}
      <li class="cv-item">
        <div class="cv-main">
          <strong>{{ talk.title }}</strong>
          <span class="cv-institution">
            {{ talk.event }}
          </span>
        </div>
        <div class="cv-meta">
          {{ talk.date }}{% if talk.location %} · {{ talk.location }}{% endif %}
        </div>
        {% if talk.details %}
          <div class="cv-details">{{ talk.details }}</div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<section class="cv-section">
  <h2>Conference and school attendance</h2>
  <ul class="cv-list">
    {% for item in site.data.activities %}
      <li class="cv-item">
        <div class="cv-main">
          <strong>{{ item.name }}</strong>
          {% if item.organizer %}
            <span class="cv-institution">{{ item.organizer }}</span>
          {% endif %}
        </div>
        <div class="cv-meta">
          {{ item.period }}
          {% if item.location %} · {{ item.location }}{% endif %}
        </div>
        {% if item.details %}
          <div class="cv-details">{{ item.details }}</div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

</div>