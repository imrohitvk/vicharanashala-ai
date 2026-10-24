---
layout: default
title: Vi-Prayoga
permalink: /logs/vi-prayoga/
---

<div class="initiative-page-hero">
  <a href="{{ site.baseurl }}/vichara_logs/" class="initiative-back"><i class="ph ph-arrow-left"></i> Vichara Logs</a>
  <p class="story-label"><i class="ph ph-flask"></i> Vichara Logs</p>
  <h1 class="initiative-page-h">Vi-Prayoga</h1>
  <p class="initiative-page-tag">Teaching and learning explored through experiments, ideas, and evolving practice.</p>
</div>

Vi-Prayoga is where theory meets classroom reality. *Prayoga* means experiment — and that is exactly what this space is: a record of ideas tested, approaches tried, and practices refined in real educational settings.

These writings bring together insights on pedagogy, reflections for educators, and guidance for learners across contexts. They are not polished prescriptions. They are honest accounts of what we tried, what we noticed, and what questions emerged that we did not expect.

The underlying belief: in education, questions are as valuable as answers. Vi-Prayoga is committed to documenting both.

---

{%- comment -%}
  Articles are listed automatically from the _prayoga/ folder, newest first.
  To add one, add a single markdown file there — see docs/README-VI-PRAYOGA.md. Nothing here needs editing.
{%- endcomment -%}
{%- assign articles = site.prayoga | sort: "date" | reverse -%}
{%- if articles.size > 0 %}
<div class="initiative-grid">
{%- for a in articles %}
  <a href="{{ a.url | relative_url }}" class="initiative-card">
    <div class="initiative-card-icon"><i class="ph ph-flask"></i></div>
    <div class="initiative-card-body">
      <div class="initiative-card-title">{{ a.title }}</div>
      <p class="initiative-card-desc">{{ a.subtitle }}</p>
      <span class="initiative-card-link">Read →</span>
    </div>
  </a>
{%- endfor %}
</div>
{%- else %}

*Articles coming soon.*
{%- endif %}
