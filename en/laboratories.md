---
layout: default
title: Laboratories
lang: en
permalink: /en/laboratories/
---

<section class="page-intro">

  <p class="section-kicker">Laboratories</p>

  <h1>
    Department laboratories
  </h1>

  <p class="page-lead">
    Our laboratories support education, research, and experimental
    development across Electronic Engineering and Mechatronics.
  </p>

</section>


<section class="section">

  <div class="feature-grid">

    {% assign laboratories_en = site.laboratories
      | where: "lang", "en"
      | sort: "order" %}

    {% for laboratory in laboratories_en %}

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
        View laboratory →
      </span>

    </a>

    {% endfor %}

  </div>

</section>
