---
layout: default
title: Research
published: true
permalink: /research/
---

{% comment %}

<section class="publications-section">
  <h2>Publications</h2>

  <ol class="pub-list">
  {% for publication in site.data.publications %}
    <li class="pub-item">
        <div class="pub-title">
            <strong>{{ publication.title }}</strong>
        </div>
        <div class="pub-coauthors">
            {{ publication.coauthors }}
        </div>
        <div>
        <span class="pub-meta">
            {{ publication.place }},
            {{ publication.year }}
        </span>
        {% if publication.link %}
        <span class="pub-link">
            <a href="{{ publication.link }}"> 
                {{ publication.link }}
            </a>
        </span>
        {% endif %}
        </div>
    </li>
  {% endfor %}
  </ol>
</section>

{% endcomment %}


<p>
    <div>I am currently working on my first article, which I will also link here.
    </div>
    <div>
    In the mean time, you could check out this
    position paper:
    <a href="https://doi.org/10.48550/arXiv.2501.18915">Algebra Unveils Deep Learning -- An Invitation to Neuroalgebraic Geometry</a>
    by Marchetti, Shahverdi, Mereta, Trager and Kohn.
    </div>
</p>

{% comment %}
<p>
    If you are interested in more papers from this area,
    <a href="https://neuroalgebraicgeometry.ai/">here</a> is a website attempting to collect them in one place. 
</p>

{% endcomment %}
