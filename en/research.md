---
layout: default
title: Research
lang: en
permalink: /en/research/
---

<section class="page-intro">

  <p class="section-kicker">Research</p>

  <h1>
    Research areas
  </h1>

  <p class="page-lead">
    Our research brings together Electronic Engineering and Mechatronics
    to address challenges in computing systems, automation, robotics,
    information processing, and emerging technologies.
  </p>

</section>


<section class="section">

  <div class="research-grid">

    {% assign research_areas = site.research
      | where: "lang", "en"
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
          Associated faculty
        </a>

        <a href="{{ area.url | relative_url }}#projects">
          Projects
        </a>

        <a href="{{ area.url | relative_url }}#publications">
          Publications
        </a>

      </div>

      <a class="research-link"
         href="{{ area.url | relative_url }}">
        View research area →
      </a>

    </article>

    {% endfor %}

  </div>

</section>
