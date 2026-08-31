---
layout: default
title: Oportunidades
lang: es
permalink: /opportunities/
---

<section class="page-intro">

  <p class="section-kicker">Oportunidades</p>

  <h1>
    Oportunidades para estudiantes
  </h1>

  <p class="page-lead">
    Explora temas de tesis, proyectos de investigación,
    prácticas y otras oportunidades vinculadas al departamento
    de Ingeniería Electrónica y Mecatrónica.
  </p>

</section>


<section class="section">

  <div class="feature-grid">

    {% assign opportunities_es = site.opportunities
      | where: "lang", "es"
      | sort: "order" %}

    {% for opportunity in opportunities_es %}

    <a class="feature-card"
       href="{{ opportunity.url | relative_url }}">

      {% if opportunity.type %}
      <span class="feature-number">
        {{ opportunity.type }}
      </span>
      {% endif %}

      <h3>{{ opportunity.title }}</h3>

      {% if opportunity.description %}
      <p>
        {{ opportunity.description }}
      </p>
      {% endif %}

      {% if opportunity.status %}
      <p>
        <strong>Estado:</strong>
        {{ opportunity.status }}
      </p>
      {% endif %}

      <span class="card-link">
        Ver oportunidad →
      </span>

    </a>

    {% endfor %}

  </div>

</section>
