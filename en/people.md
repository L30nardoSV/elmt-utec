---
layout: default
title: People
lang: en
permalink: /en/people/
---

<section class="page-intro">

  <p class="section-kicker">People</p>

  <h1>
    Faculty and department team
  </h1>

  <p class="page-lead">
    Our department brings together faculty from Electronic Engineering
    and Mechatronics working across education, research, and technological
    development.
  </p>

</section>


{% assign people_en = site.people
  | where: "lang", "en"
  | sort: "order" %}

{% assign leadership = people_en
  | where: "discipline", "leadership" %}

{% assign electronics = people_en
  | where: "discipline", "electronics" %}

{% assign mechatronics = people_en
  | where: "discipline", "mechatronics" %}


<section class="section">

  <div class="section-heading">
    <p class="section-kicker">Leadership</p>
    <h2>Department leadership</h2>
  </div>

  <div class="people-grid">

    {% for person in leadership %}

    <article class="person-card"
             id="{{ person.name | slugify }}">

      <div class="person-photo-placeholder">
        Photo
      </div>

      <div class="person-info">

        <h3>{{ person.name }}</h3>

        {% if person.role %}
        <p class="person-role">
          {{ person.role }}
        </p>
        {% endif %}

        <div class="person-links">

          <a href="{{ person.url | relative_url }}">
            View profile
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
    <h2>Electronic Engineering</h2>
  </div>

  <div class="people-grid">

    {% for person in electronics %}

    <article class="person-card"
             id="{{ person.name | slugify }}">

      <div class="person-photo-placeholder">
        Photo
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
            View profile
          </a>

          {% if person.website %}
            <a href="{{ person.website }}">Website</a>
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
    <h2>Mechatronics</h2>
  </div>

  <div class="people-grid">

    {% for person in mechatronics %}

    <article class="person-card"
             id="{{ person.name | slugify }}">

      <div class="person-photo-placeholder">
        Photo
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
            View profile
          </a>

          {% if person.website %}
            <a href="{{ person.website }}">Website</a>
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
