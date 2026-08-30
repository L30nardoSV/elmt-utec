---
layout: default
title: Investigación
lang: es
permalink: /research/
---

<section class="page-intro">

  <p class="section-kicker">Investigación</p>

  <h1>
    Áreas de investigación
  </h1>

  <p class="page-lead">
    Nuestra investigación integra Ingeniería Electrónica y Mecatrónica
    para abordar problemas en sistemas computacionales, automatización,
    robótica, procesamiento de información y tecnologías emergentes.
  </p>

</section>


<section class="section">

  <div class="research-grid">

    {% assign research_areas = site.research
      | where: "lang", "es"
      | sort: "order" %}

    {% for area in research_areas %}

    <article class="research-card">

      <span class="research-number">
        {{ area.order | prepend: "0" | slice: -2, 2 }}
      </span>

      <h3>{{ area.title }}</h3>

      <p>
        {{ area.description }}
      </p>

      <div class="research-meta">

        <a href="{{ area.url | relative_url }}#faculty">
          Profesores asociados
        </a>

        <a href="{{ area.url | relative_url }}#projects">
          Proyectos
        </a>

        <a href="{{ area.url | relative_url }}#publications">
          Publicaciones
        </a>

      </div>

      <a class="research-link"
         href="{{ area.url | relative_url }}">
        Ver área de investigación →
      </a>

    </article>

    {% endfor %}

  </div>

</section>
