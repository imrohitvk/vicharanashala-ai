---
layout: default
title: Contact
permalink: /contact/
---

<div class="contact-hero">
  <p class="story-label"><i class="ph ph-chats-circle"></i> Get in touch</p>
  <h1 class="contact-h">Let's talk.</h1>
  <p class="contact-intro">Questions about our programmes, a collaboration, or a visit to the lab? Reach us any of these ways — we read everything.</p>
</div>

<div class="contact-grid">
  <div class="contact-cards">

    <a class="contact-card" href="mailto:dled@iitrpr.ac.in">
      <div class="contact-card-icon"><i class="ph ph-envelope-simple" style="color:#e48f38"></i></div>
      <div class="contact-card-body">
        <span class="contact-card-label">Email</span>
        <span class="contact-card-value">dled@iitrpr.ac.in</span>
      </div>
      <i class="ph ph-arrow-up-right contact-card-go"></i>
    </a>

    <a class="contact-card" href="https://www.linkedin.com/company/vicharanashala" target="_blank" rel="noopener">
      <div class="contact-card-icon"><i class="ph ph-linkedin-logo" style="color:#0A66C2"></i></div>
      <div class="contact-card-body">
        <span class="contact-card-label">LinkedIn</span>
        <span class="contact-card-value">linkedin.com/company/vicharanashala</span>
      </div>
      <i class="ph ph-arrow-up-right contact-card-go"></i>
    </a>

    <div class="contact-card contact-card-static">
      <div class="contact-card-icon"><i class="ph ph-map-pin" style="color:#42a6ac"></i></div>
      <div class="contact-card-body">
        <span class="contact-card-label">Visit us</span>
        <span class="contact-card-value">VLED — Vicharanashala Lab for Education Design<br>
        Lab No. C-101, Super Academic Block<br>
        Indian Institute of Technology, Ropar<br>
        Rupnagar, Punjab 140001</span>
      </div>
    </div>

  </div>

  <div class="contact-map">
    <iframe
      src="https://maps.google.com/maps?q=Indian+Institute+of+Technology+Ropar+Rupnagar+Punjab&output=embed"
      width="100%"
      height="100%"
      style="border:0; min-height: 300px;"
      allowfullscreen=""
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
      title="IIT Ropar location on Google Maps">
    </iframe>
  </div>
</div>

<style>
.contact-hero {
  padding: 0 0 1.5rem;
  border-bottom: 1px solid #e2e2de;
  margin-bottom: 2rem;
}
.contact-h {
  font-size: 2rem;
  font-weight: 600;
  letter-spacing: -0.02em;
  color: #1a1a1a;
  margin: 0.4rem 0 0.6rem;
}
.contact-intro {
  font-size: 1rem;
  line-height: 1.75;
  color: #444;
  max-width: 560px;
  margin: 0;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
  align-items: stretch;
}

.contact-cards {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.contact-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.15rem 1.3rem;
  border: 1px solid #e2e2de;
  border-radius: 10px;
  background: #fff;
  text-decoration: none;
  transition: border-color 0.15s, box-shadow 0.15s;
}
a.contact-card:hover {
  border-color: #767676;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.06);
  text-decoration: none;
}
.contact-card-icon {
  width: 42px; height: 42px; border-radius: 50%;
  background: #efefec;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.2rem; flex-shrink: 0;
}
.contact-card-body { display: flex; flex-direction: column; gap: 0.15rem; flex: 1; }
.contact-card-label {
  font-size: 0.7rem; font-weight: 600; letter-spacing: 0.08em;
  text-transform: uppercase; color: #767676;
}
.contact-card-value { font-size: 0.95rem; color: #1a1a1a; line-height: 1.55; }
.contact-card-go { color: #b0b0aa; font-size: 1rem; flex-shrink: 0; }
a.contact-card:hover .contact-card-go { color: #1a1a1a; }
.contact-card-static { cursor: default; }

.contact-map {
  border-radius: 10px;
  overflow: hidden;
  border: 1px solid #e2e2de;
  min-height: 340px;
}
.contact-map iframe { display: block; width: 100%; height: 100%; }

@media (max-width: 640px) {
  .contact-grid { grid-template-columns: 1fr; }
  .contact-map { min-height: 280px; }
  .contact-h { font-size: 1.6rem; }
}
</style>
