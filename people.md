---
layout: default
title: Personas
lang: es
permalink: /people/
---

<section class="page-intro">

  <p class="section-kicker">Personas</p>

  <h1>
    Profesores y equipo del departamento
  </h1>

  <p class="page-lead">
    Nuestro departamento reúne profesores de Ingeniería Electrónica
    y Mecatrónica que trabajan en docencia, investigación y desarrollo
    tecnológico.
  </p>

</section>


{% assign people_es = site.people
  | where: "lang", "es"
  | sort: "order" %}

{% assign leadership = people_es
  | where: "discipline", "leadership" %}

{% assign electronics = people_es
  | where: "discipline", "electronics" %}

{% assign mechatronics = people_es
  | where: "discipline", "mechatronics" %}


<section class="section">

  <div class="section-heading">
    <p class="section-kicker">Dirección</p>
    <h2>Dirección del departamento</h2>
  </div>

  <div class="people-grid">

    {% for person in leadership %}

    <article class="person-card"
             id="{{ person.name | slugify }}">

{% if person.image %}

  <img class="person-photo"
       src="{{ person.image | relative_url }}"
       alt="{{ person.name }}">

{% else %}

  <div class="person-photo-placeholder">
    Foto
  </div>

{% endif %}

      <div class="person-info">

        <h3>{{ person.name }}</h3>

        {% if person.role %}
        <p class="person-role">
          {{ person.role }}
        </p>
        {% endif %}

        <div class="person-links">
          <a href="{{ person.url | relative_url }}">
            Ver perfil
          </a>

          {% if person.scholar %}
            <a href="{{ person.scholar }}">Google Scholar</a>
          {% endif %}

          {% if person.orcid %}
            <a href="{{ person.orcid }}">ORCID</a>
          {% endif %}
        </div>

      </div>

    </article>

    {% endfor %}

  </div>

</section>


<section class="section">

  <div class="section-heading">
    <p class="section-kicker">EL</p>
    <h2>Ingeniería Electrónica</h2>
  </div>

  <div class="people-grid">

    {% for person in electronics %}

    <article class="person-card"
             id="{{ person.name | slugify }}">

      <div class="person-photo-placeholder">
        Foto
      </div>

      <div class="person-info">

        <h3>{{ person.name }}</h3>

        {% if person.role %}
        <p class="person-role">
          {{ person.role }}
        </p>
        {% endif %}

        {% if person.research_interests %}
        <p class="person-area">
          {{ person.research_interests | join: " · " }}
        </p>
        {% endif %}

        <div class="person-links">

          <a href="{{ person.url | relative_url }}">
            Ver perfil
          </a>

          {% if person.website %}
            <a href="{{ person.website }}">Web</a>
          {% endif %}

          {% if person.scholar %}
            <a href="{{ person.scholar }}">Google Scholar</a>
          {% endif %}

          {% if person.orcid %}
            <a href="{{ person.orcid }}">ORCID</a>
          {% endif %}

        </div>

      </div>

    </article>

    {% endfor %}

  </div>

</section>


<section class="section">

  <div class="section-heading">
    <p class="section-kicker">MT</p>
    <h2>Mecatrónica</h2>
  </div>

  <div class="people-grid">

    {% for person in mechatronics %}

    <article class="person-card"
             id="{{ person.name | slugify }}">

      <div class="person-photo-placeholder">
        Foto
      </div>

      <div class="person-info">

        <h3>{{ person.name }}</h3>

        {% if person.role %}
        <p class="person-role">
          {{ person.role }}
        </p>
        {% endif %}

        {% if person.research_interests %}
        <p class="person-area">
          {{ person.research_interests | join: " · " }}
        </p>
        {% endif %}

        <div class="person-links">

          <a href="{{ person.url | relative_url }}">
            Ver perfil
          </a>

          {% if person.website %}
            <a href="{{ person.website }}">Web</a>
          {% endif %}

          {% if person.scholar %}
            <a href="{{ person.scholar }}">Google Scholar</a>
          {% endif %}

          {% if person.orcid %}
            <a href="{{ person.orcid }}">ORCID</a>
          {% endif %}

        </div>

      </div>

    </article>

    {% endfor %}

  </div>

</section>
