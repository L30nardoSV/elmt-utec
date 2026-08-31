---
layout: default
title: Opportunities
lang: en
permalink: /en/opportunities/
---

<section class="page-intro">

  <p class="section-kicker">Opportunities</p>

  <h1>
    Opportunities for students
  </h1>

  <p class="page-lead">
    Explore thesis topics, research projects, internships,
    and other opportunities related to the Department of
    Electronic Engineering and Mechatronics.
  </p>

</section>


<section class="section">

  <div class="feature-grid">

    {% assign opportunities_en = site.opportunities
      | where: "lang", "en"
      | sort: "order" %}

    {% for opportunity in opportunities_en %}

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
        <strong>Status:</strong>
        {{ opportunity.status }}
      </p>
      {% endif %}

      <span class="card-link">
        View opportunity →
      </span>

    </a>

    {% endfor %}

  </div>

</section>
