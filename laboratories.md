---
layout: default
title: Laboratorios
lang: es
permalink: /laboratories/
---

<section class="page-intro">

  <p class="section-kicker">Laboratorios</p>

  <h1>
    Laboratorios del departamento
  </h1>

  <p class="page-lead">
    Nuestros laboratorios apoyan la docencia, la investigación
    y el desarrollo experimental en Ingeniería Electrónica
    y Mecatrónica.
  </p>

</section>


<section class="section">

  <div class="feature-grid">

    {% assign laboratories_es = site.laboratories
      | where: "lang", "es"
      | sort: "order" %}

    {% for laboratory in laboratories_es %}

    <a class="feature-card"
       href="{{ laboratory.url | relative_url }}">

{% if laboratory.image %}

<div class="laboratory-card-image">
  <img src="{{ laboratory.image | relative_url }}"
       alt="{{ laboratory.title }}">
</div>

{% endif %}

      <span class="feature-number">
        {{ laboratory.order | prepend: "0" | slice: -2, 2 }}
      </span>

      <h3>{{ laboratory.title }}</h3>

      {% if laboratory.description %}
      <p>
        {{ laboratory.description }}
      </p>
      {% endif %}

      <span class="card-link">
        Ver laboratorio →
      </span>

    </a>

    {% endfor %}

  </div>

</section>
