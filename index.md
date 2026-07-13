---
layout: splash
title: "Humans on AIr"
permalink: /
author_profile: false
---

<section class="home-hero">
  <div class="home-hero__image"></div>

  <div class="home-hero__content">
    <h1>Humans<br>on <span>AIr</span></h1>

    <p>
      Reflexiones críticas sobre el impacto de la inteligencia artificial
      en la cultura, la comunicación y la sociedad.
    </p>

    <div class="home-hero__buttons">
      <a href="{{ '/charlas/' | relative_url }}" class="home-button home-button--primary">
        Ver charlas →
      </a>

      <a href="{{ '/sobre/' | relative_url }}" class="home-button home-button--secondary">
        Sobre el proyecto →
      </a>
    </div>
  </div>
</section>

{% assign hay_actividades = false %}

{% if hay_actividades %}
  <section class="home-events">
    <h2>Próximas actividades</h2>

    <article class="home-event-card">
      <div class="home-event-date">
        <span>JUL</span>
        <strong>09</strong>
        <small>JUEVES</small>
      </div>

      <div class="home-event-info">
        <p class="home-event-type">TALLER</p>

        <h3>
          Taller de IA: Uso práctico de la IA Generativa para adultos
        </h3>

        <p>
          Benamí Barros García y Nicolás Robinson-García ·
          U^CHASS (Universidad de Granada)
        </p>

        <p class="home-event-meta">
          9 de julio de 2026 · 11:00 h · Punto Vuela de Quéntar
        </p>
      </div>

      <a href="{{ '/talleres/' | relative_url }}" class="home-event-link">
        Más información →
      </a>
    </article>
  </section>
{% endif %}

<section class="home-services">
  <header class="home-services__header">
    <p class="home-services__eyebrow">Lo que hacemos</p>

    <h2>Espacios para pensar, crear y colaborar</h2>

    <p class="home-services__intro">
      Actividades y encuentros para explorar la intersección entre
      tecnología, humanidades y sociedad.
    </p>
  </header>

  <div class="home-services__grid">

    <article class="home-service-card">
      <div class="home-service-card__icon" aria-hidden="true">
        🎙
      </div>

      <div class="home-service-card__content">
        <h3>Charlas</h3>

        <p>
          Conversaciones con especialistas sobre IA, lenguaje, cultura
          y sociedad.
        </p>
      </div>

      <a href="{{ '/charlas/' | relative_url }}" class="home-service-card__link">
        <span>Explorar charlas</span>
        <span aria-hidden="true">→</span>
      </a>
    </article>

    <article class="home-service-card">
      <div class="home-service-card__icon" aria-hidden="true">
        ✎
      </div>

      <div class="home-service-card__content">
        <h3>Talleres</h3>

        <p>
          Espacios prácticos para experimentar y reflexionar sobre
          tecnología y humanidades.
        </p>
      </div>

      <a href="{{ '/talleres/' | relative_url }}" class="home-service-card__link">
        <span>Ver talleres</span>
        <span aria-hidden="true">→</span>
      </a>
    </article>

    <article class="home-service-card">
      <div class="home-service-card__icon" aria-hidden="true">
        👥
      </div>

      <div class="home-service-card__content">
        <h3>Equipo</h3>

        <p>
          Conoce al equipo interdisciplinar que impulsa el proyecto
          Humans on AIr.
        </p>
      </div>

      <a href="{{ '/equipo/' | relative_url }}" class="home-service-card__link">
        <span>Conocer equipo</span>
        <span aria-hidden="true">→</span>
      </a>
    </article>

  </div>
</section>

{% unless hay_actividades %}
  <section class="home-events home-events--empty">
    <h2>Próximas actividades</h2>

    <div class="home-events-empty">
      <p>Actualmente no hay próximas actividades programadas.</p>

      <a href="{{ '/talleres/' | relative_url }}" class="home-event-link">
        Ver talleres realizados →
      </a>
    </div>
  </section>
{% endunless %}