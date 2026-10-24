---
layout: default
title: VLED in Action
permalink: /vled-in-action/
---

<div class="initiative-page-hero">
  <p class="home-label"><i class="ph ph-images"></i> &nbsp;GLIMPSES</p>
  <h1 class="initiative-page-h">VLED in Action</h1>
  <p class="initiative-page-tag">From people who walked into the lab to rooms we walked into — researchers, educators, and practitioners who've crossed paths with this work.</p>
</div>

<div class="moments-filter">
  <button class="moments-filter-btn active" data-filter="all">All</button>
  <button class="moments-filter-btn" data-filter="visit">Visits</button>
  <button class="moments-filter-btn" data-filter="lab-event">Lab Events</button>
  <button class="moments-filter-btn" data-filter="conference">Conferences &amp; Conclaves</button>
</div>

<div class="moments-grid">
  {% for moment in site.data.moments %}
  <div class="moment-card" data-type="{{ moment.type }}">
    <div class="moment-img-wrap">
      {% if moment.gallery %}
        <div class="moment-carousel" id="carousel-{{ forloop.index }}">
          {% for img in moment.gallery %}
          <img src="{{ site.baseurl }}/assets/images/moments/{{ img }}" alt="{{ moment.caption }}" class="moment-img moment-slide{% if forloop.first %} active{% endif %}" loading="lazy">
          {% endfor %}
          <div class="carousel-dots">
            {% for img in moment.gallery %}
            <button class="carousel-dot{% if forloop.first %} active{% endif %}" data-index="{{ forloop.index0 }}" aria-label="Photo {{ forloop.index }}"></button>
            {% endfor %}
          </div>
        </div>
      {% else %}
        <img src="{{ site.baseurl }}/assets/images/moments/{{ moment.image }}" alt="{{ moment.caption }}" class="moment-img" loading="lazy">
      {% endif %}
    </div>
    <div class="moment-body">
      <span class="moment-tag moment-tag--{{ moment.type }}">{% if moment.type == 'visit' %}Visit{% elsif moment.type == 'lab-event' %}Lab Event{% elsif moment.type == 'conference' %}Conference &amp; Conclave{% else %}{{ moment.type }}{% endif %}</span>
      <p class="moment-caption">{{ moment.caption }}</p>
      <p class="moment-detail">{{ moment.detail }}</p>
      <p class="moment-date">{{ moment.date }}</p>
    </div>
  </div>
  {% endfor %}
</div>

<script>
  // Filter buttons
  const btns = document.querySelectorAll('.moments-filter-btn');
  const cards = document.querySelectorAll('.moment-card');
  btns.forEach(btn => {
    btn.addEventListener('click', () => {
      btns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        card.style.display = (filter === 'all' || card.dataset.type === filter) ? '' : 'none';
      });
    });
  });

  // Carousels
  document.querySelectorAll('.moment-carousel').forEach(carousel => {
    const slides = carousel.querySelectorAll('.moment-slide');
    const dots = carousel.querySelectorAll('.carousel-dot');
    let current = 0;
    let timer;

    function goTo(index) {
      slides[current].classList.remove('active');
      dots[current].classList.remove('active');
      current = (index + slides.length) % slides.length;
      slides[current].classList.add('active');
      dots[current].classList.add('active');
    }

    function startAuto() {
      timer = setInterval(() => goTo(current + 1), 3000);
    }

    dots.forEach((dot, i) => {
      dot.addEventListener('click', () => {
        clearInterval(timer);
        goTo(i);
        startAuto();
      });
    });

    startAuto();
  });
</script>
