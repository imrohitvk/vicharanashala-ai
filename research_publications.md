---
layout: page
title: Research Publications
permalink: /research/
quote: "Research is formalized curiosity. It is poking and prying with a purpose."
quote_author: "Zora Neale Hurston"
---

A curated record of research from Vicharanashala — spanning the work of the Principal Investigator, core team members, research scholars, and collaborators. Our research sits at the intersection of learning design, educational technology, and higher education policy.

<div class="rs-stats">
  <div class="rs-stat"><span class="rs-stat-num">1,194</span><span class="rs-stat-lbl">PI citations</span></div>
  <div class="rs-stat"><span class="rs-stat-num">17</span><span class="rs-stat-lbl">h-index</span></div>
  <div class="rs-stat"><span class="rs-stat-num">{{ site.data.papers | size }}</span><span class="rs-stat-lbl">Working papers</span></div>
  <div class="rs-stat"><span class="rs-stat-num">{{ site.data.datasets | size }}</span><span class="rs-stat-lbl">Open datasets</span></div>
</div>

<nav class="rs-jump">
  <a href="#pi-publications"><i class="ph ph-medal"></i> PI Publications</a>
  <a href="#working-papers-posters--reports"><i class="ph ph-files"></i> Papers &amp; Posters</a>
  <a href="#datasets"><i class="ph ph-database"></i> Datasets</a>
  <a href="#instruments-developed"><i class="ph ph-ruler"></i> Instruments</a>
  <a href="#courses-designed"><i class="ph ph-books"></i> Courses</a>
  <a href="#research-areas"><i class="ph ph-compass"></i> Research Areas</a>
</nav>

<p class="home-label rs-label"><i class="ph ph-medal"></i> Selected works</p>

## PI Publications

<div class="pub-header">
  <div class="pub-stats">
    <span class="pub-stat"><strong>1,194</strong> citations</span>
    <span class="pub-stat-sep">·</span>
    <span class="pub-stat">h-index <strong>17</strong></span>
    <span class="pub-stat-sep">·</span>
    <span class="pub-stat">i10-index <strong>38</strong></span>
    <span class="pub-stat-asof">(as of September 2026)</span>
  </div>
  <a href="https://scholar.google.com/citations?user=hy7n9kEAAAAJ&hl=en&sortby=citations" class="pub-gs-link" target="_blank" rel="noopener">Full profile on Google Scholar →</a>
</div>

<div class="rs-pi-list">

  <div class="rs-pi">
    <div class="rs-pi-cite"><span class="rs-pi-num">235</span><span class="rs-pi-unit">citations</span></div>
    <div class="rs-pi-body">
      <a href="https://arxiv.org/abs/2011.07190" class="rs-pi-title" target="_blank" rel="noopener">Centrality Measures in Complex Networks: A Survey <i class="ph ph-arrow-up-right"></i></a>
      <p class="rs-pi-meta">A. Saxena, S. R. S. Iyengar &nbsp;·&nbsp; arXiv, 2020</p>
    </div>
  </div>

  <div class="rs-pi">
    <div class="rs-pi-cite"><span class="rs-pi-num">61</span><span class="rs-pi-unit">citations</span></div>
    <div class="rs-pi-body">
      <span class="rs-pi-title">Node-Weighted Centrality: A New Way of Centrality Hybridization</span>
      <p class="rs-pi-meta">A. Singh, R. R. Singh, S. R. S. Iyengar &nbsp;·&nbsp; Computational Social Networks, 2020</p>
    </div>
  </div>

  <div class="rs-pi">
    <div class="rs-pi-cite"><span class="rs-pi-num">46</span><span class="rs-pi-unit">citations</span></div>
    <div class="rs-pi-body">
      <span class="rs-pi-title">Understanding Human Navigation Using Network Analysis</span>
      <p class="rs-pi-meta">S. R. S. Iyengar, C. E. Veni Madhavan, K. A. Zweig, A. Natarajan &nbsp;·&nbsp; Topics in Cognitive Science, 2012</p>
    </div>
  </div>

  <div class="rs-pi">
    <div class="rs-pi-cite"><span class="rs-pi-num">44</span><span class="rs-pi-unit">citations</span></div>
    <div class="rs-pi-body">
      <span class="rs-pi-title">A Faster Algorithm to Update Betweenness Centrality After Node Alteration</span>
      <p class="rs-pi-meta">R. R. Singh, K. Goel, S. R. S. Iyengar, S. Gupta &nbsp;·&nbsp; Internet Mathematics, 2015</p>
    </div>
  </div>

  <div class="rs-pi">
    <div class="rs-pi-cite"><span class="rs-pi-num">43</span><span class="rs-pi-unit">citations</span></div>
    <div class="rs-pi-body">
      <span class="rs-pi-title">Understanding Spreading Patterns on Social Networks Based on Network Topology</span>
      <p class="rs-pi-meta">A. Saxena, S. R. S. Iyengar, Y. Gupta &nbsp;·&nbsp; IEEE/ACM ASONAM, 2015</p>
    </div>
  </div>

  <div class="rs-pi">
    <div class="rs-pi-cite"><span class="rs-pi-num">25</span><span class="rs-pi-unit">citations</span></div>
    <div class="rs-pi-body">
      <span class="rs-pi-title">Dynamics of Edit War Sequences in Wikipedia</span>
      <p class="rs-pi-meta">A. Chhabra, R. Kaur, S. R. S. Iyengar &nbsp;·&nbsp; OpenSym, 2020</p>
    </div>
  </div>

</div>

<p class="home-label rs-label"><i class="ph ph-files"></i> In progress</p>

## Working Papers, Posters & Reports

<div class="rs-wp-grid">
{% for p in site.data.papers %}
  <a class="rs-wp" href="https://arxiv.org/abs/{{ p.arxiv }}" target="_blank" rel="noopener">
    <i class="ph ph-file-text rs-wp-icon"></i>
    <span class="rs-wp-body">
      <span class="rs-wp-title">{{ p.title }}</span>
      <span class="rs-wp-meta">arXiv:{{ p.arxiv }}</span>
    </span>
    <span class="pub-status pub-status--arxiv">arXiv <i class="ph ph-arrow-up-right"></i></span>
  </a>
{% endfor %}
</div>

<p class="home-label rs-label"><i class="ph ph-database"></i> Open data</p>

## Datasets

Openly available datasets released by the lab, each published on several platforms.

<div class="rs-ds-list">
{% for d in site.data.datasets %}
  <div class="rs-ds">
    <div class="rs-ds-icon-wrap"><i class="ph ph-database rs-ds-icon"></i></div>
    <div class="rs-ds-body">
      <div class="rs-ds-title">{{ d.name }}</div>
      <p class="rs-ds-desc">{{ d.description }}</p>
      <p class="rs-ds-meta">{{ d.meta }}</p>
      <div class="ds-links">
        {% if d.kaggle %}<a href="{{ d.kaggle }}" class="ds-link" target="_blank" rel="noopener">Kaggle →</a>{% endif %}
        {% if d.huggingface %}<a href="{{ d.huggingface }}" class="ds-link" target="_blank" rel="noopener">Hugging Face →</a>{% endif %}
        {% if d.aikosh %}<a href="{{ d.aikosh }}" class="ds-link" target="_blank" rel="noopener">AIKosh →</a>{% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>

<p class="home-label rs-label"><i class="ph ph-ruler"></i> Measurement</p>

## Instruments Developed

<div class="rs-card-grid">
  <div class="rs-card">
    <div class="rs-card-icon-wrap"><i class="ph ph-gauge rs-card-icon"></i></div>
    <div class="rs-card-title">AI Literacy Benchmarking Instrument</div>
    <div class="rs-card-desc">Measures baseline and growth in AI literacy across learner cohorts</div>
  </div>
  <div class="rs-card">
    <div class="rs-card-icon-wrap"><i class="ph ph-list-checks rs-card-icon"></i></div>
    <div class="rs-card-title">Weighted Quality Score (WQS) Rubric</div>
    <div class="rs-card-desc">Evaluates instructional content quality for GuruSetu</div>
  </div>
  <div class="rs-card">
    <div class="rs-card-icon-wrap"><i class="ph ph-chats-circle rs-card-icon"></i></div>
    <div class="rs-card-title">AI Interview Rubric</div>
    <div class="rs-card-desc">Structured evaluation rubric for Samagama/Yaksha internship assessments</div>
  </div>
</div>

<p class="home-label rs-label"><i class="ph ph-books"></i> Teaching</p>

## Courses Designed

<div class="rs-course-row">
  <span class="rs-course"><i class="ph ph-chalkboard"></i> Chalkboards to Chatbots</span>
  <span class="rs-course"><i class="ph ph-lightbulb"></i> Brainstorming with AI</span>
  <span class="rs-course"><i class="ph ph-strategy"></i> Strategic AI Leadership</span>
  <span class="rs-course"><i class="ph ph-code"></i> Fundamentals of MERN Stack</span>
  <span class="rs-course"><i class="ph ph-plant"></i> Fundamentals of AI Using Agriculture Datasets</span>
</div>

<p class="home-label rs-label"><i class="ph ph-compass"></i> Focus</p>

## Research Areas

Our work spans:

<div class="challenges-grid rs-areas">
  <div class="challenge-card">
    <div class="challenge-left"><span class="challenge-num">01</span><i class="ph ph-monitor-play challenge-icon"></i></div>
    <div class="challenge-right"><div class="challenge-title">Online learning design and active learning systems</div></div>
  </div>
  <div class="challenge-card">
    <div class="challenge-left"><span class="challenge-num">02</span><i class="ph ph-chalkboard-teacher challenge-icon"></i></div>
    <div class="challenge-right"><div class="challenge-title">Faculty professional development at scale</div></div>
  </div>
  <div class="challenge-card">
    <div class="challenge-left"><span class="challenge-num">03</span><i class="ph ph-robot challenge-icon"></i></div>
    <div class="challenge-right"><div class="challenge-title">AI literacy in higher education</div></div>
  </div>
  <div class="challenge-card">
    <div class="challenge-left"><span class="challenge-num">04</span><i class="ph ph-exam challenge-icon"></i></div>
    <div class="challenge-right"><div class="challenge-title">Assessment, evaluation, and academic integrity</div></div>
  </div>
  <div class="challenge-card">
    <div class="challenge-left"><span class="challenge-num">05</span><i class="ph ph-briefcase challenge-icon"></i></div>
    <div class="challenge-right"><div class="challenge-title">Internship systems and structured student exposure</div></div>
  </div>
</div>

<style>
/* ---- stats strip + jump nav ---- */
.rs-stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0;
  margin: 2rem 0 1.2rem;
  background: #42a6ac;
  border-radius: 6px;
  overflow: hidden;
}
.rs-stat {
  padding: 1.3rem 1.2rem;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  border-right: 1px solid rgba(255,255,255,0.18);
}
.rs-stat:last-child { border-right: none; }
.rs-stat-num { font-size: 1.7rem; font-weight: 700; letter-spacing: -0.03em; color: #fff; line-height: 1.1; }
.rs-stat-lbl { font-size: 0.68rem; font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase; color: rgba(255,255,255,0.85); }

.rs-jump { display: flex; flex-wrap: wrap; gap: 0.5rem; margin: 0 0 2.5rem; }
.rs-jump a {
  display: inline-flex; align-items: center; gap: 0.35rem;
  font-size: 0.78rem; font-weight: 500; color: #444;
  background: #efefec; border-radius: 999px; padding: 0.35rem 0.85rem;
  text-decoration: none; transition: background 0.15s, color 0.15s;
}
.rs-jump a:hover { background: #1a1a1a; color: #f9f9f7; text-decoration: none; }

/* ---- section labels + headings ---- */
.rs-label { margin: 3.5rem 0 0.3rem; }
.rs-label + h2 { margin-top: 0; }
.page-content h2 { scroll-margin-top: 1.5rem; }

/* ---- PI publications ---- */
.pub-header {
  display: flex; align-items: center; justify-content: space-between;
  flex-wrap: wrap; gap: 0.8rem; margin-bottom: 1.2rem;
}
.pub-stats { display: flex; align-items: center; gap: 0.5rem; font-size: 0.88rem; color: #444; }
.pub-stat-sep { color: #c0c0bb; }
.pub-stat-asof { color: #767676; font-size: 0.8rem; }
.pub-gs-link { font-size: 0.82rem; font-weight: 500; color: #e48f38; text-decoration: none; letter-spacing: 0.01em; }
.pub-gs-link:hover { opacity: 0.8; text-decoration: none; }

.rs-pi-list { display: flex; flex-direction: column; gap: 0.7rem; }
.rs-pi {
  display: flex; align-items: center; gap: 1.4rem;
  border: 1px solid #e2e2de; border-left: 3px solid #e48f38; border-radius: 6px;
  padding: 1rem 1.4rem; background: #fff;
  transition: box-shadow 0.2s, transform 0.2s;
}
.rs-pi:hover { box-shadow: 0 4px 20px rgba(0,0,0,0.06); transform: translateY(-1px); }
.rs-pi-cite { display: flex; flex-direction: column; align-items: center; min-width: 4.2rem; }
.rs-pi-num { font-size: 1.45rem; font-weight: 700; color: #e48f38; letter-spacing: -0.03em; line-height: 1; }
.rs-pi-unit { font-size: 0.62rem; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase; color: #767676; margin-top: 0.25rem; }
.rs-pi-body { flex: 1; }
.rs-pi-title { font-size: 0.95rem; font-weight: 600; color: #1a1a1a; line-height: 1.45; text-decoration: none; }
a.rs-pi-title:hover { color: #e48f38; text-decoration: none; }
.rs-pi-title .ph { font-size: 0.8rem; color: #e48f38; }
.rs-pi-meta { font-size: 0.8rem; color: #767676; margin: 0.3rem 0 0; line-height: 1.5; }

/* ---- working papers ---- */
.rs-wp-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 0.7rem; }
.rs-wp {
  display: flex; align-items: flex-start; gap: 0.75rem;
  border: 1px solid #e2e2de; border-radius: 6px; padding: 0.9rem 1rem; background: #fff;
  transition: border-color 0.15s, box-shadow 0.15s;
}
.rs-wp:hover { border-color: #767676; box-shadow: 0 2px 12px rgba(0,0,0,0.05); }
.rs-wp-icon { font-size: 1.2rem; color: #42a6ac; margin-top: 0.1rem; flex-shrink: 0; }
.rs-wp-title { flex: 1; font-size: 0.86rem; font-weight: 600; color: #1a1a1a; line-height: 1.45; }
a.rs-wp { text-decoration: none; color: inherit; }
a.rs-wp:hover { text-decoration: none; border-color: #e48f38; }
a.rs-wp:hover .rs-wp-title { color: #e48f38; }
.rs-wp-body { flex: 1; display: flex; flex-direction: column; gap: 0.3rem; }
.rs-wp-meta { font-size: 0.74rem; color: #767676; letter-spacing: 0.01em; }
.pub-status--arxiv { background: #fbeaea; color: #b31b1b; display: inline-flex; align-items: center; gap: 0.2rem; }
.pub-status {
  flex-shrink: 0; font-size: 0.62rem; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase;
  padding: 0.18rem 0.45rem; border-radius: 2px; white-space: nowrap; margin-top: 0.1rem;
}
.pub-status--draft    { background: #efefec; color: #767676; }
.pub-status--review   { background: #fef3e8; color: #b85a10; }
.pub-status--accepted { background: #e8f6f7; color: #2a8a90; }

/* ---- datasets ---- */
.rs-ds-list { display: flex; flex-direction: column; gap: 0.9rem; margin-top: 1.2rem; }
.rs-ds {
  display: flex; gap: 1.3rem; align-items: flex-start;
  border: 1px solid #e2e2de; border-radius: 6px; padding: 1.3rem 1.5rem; background: #fff;
  transition: box-shadow 0.2s, border-color 0.2s;
}
.rs-ds:hover { border-color: #42a6ac; box-shadow: 0 4px 20px rgba(66,166,172,0.12); }
.rs-ds-icon-wrap {
  width: 48px; height: 48px; border-radius: 50%; background: #e8f6f7; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
}
.rs-ds-icon { font-size: 1.45rem; color: #2a8a90; }
.rs-ds-body { flex: 1; }
.rs-ds-title { font-size: 1rem; font-weight: 600; color: #1a1a1a; letter-spacing: -0.01em; line-height: 1.4; }
.rs-ds-desc { font-size: 0.86rem; color: #555; line-height: 1.6; margin: 0.4rem 0 0.35rem; }
.rs-ds-meta { font-size: 0.74rem; font-weight: 600; letter-spacing: 0.06em; text-transform: uppercase; color: #767676; margin: 0; }
.ds-links { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 0.9rem; }
.ds-link {
  font-size: 0.78rem; font-weight: 500; color: #e48f38; border: 1px solid #e48f38; border-radius: 2px;
  padding: 0.25rem 0.7rem; text-decoration: none; letter-spacing: 0.01em; transition: background 0.15s, color 0.15s;
}
.ds-link:hover { background: #e48f38; color: #f9f9f7; text-decoration: none; }

/* ---- instruments ---- */
.rs-card-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 1rem; margin-top: 1.2rem; }
.rs-card {
  border: 1px solid #e2e2de; border-radius: 6px; padding: 1.3rem; background: #fff;
  display: flex; flex-direction: column; gap: 0.45rem;
  transition: border-color 0.15s, box-shadow 0.15s;
}
.rs-card:hover { border-color: #767676; box-shadow: 0 2px 12px rgba(0,0,0,0.06); }
.rs-card-icon-wrap {
  width: 48px; height: 48px; border-radius: 50%; background: #fef3e8;
  display: flex; align-items: center; justify-content: center; margin-bottom: 0.6rem;
}
.rs-card-icon { font-size: 1.45rem; color: #e48f38; }
.rs-card-title { font-size: 0.95rem; font-weight: 600; color: #1a1a1a; line-height: 1.4; }
.rs-card-desc { font-size: 0.84rem; color: #767676; line-height: 1.55; }

/* ---- courses ---- */
.rs-course-row { display: flex; flex-wrap: wrap; gap: 0.6rem; margin-top: 1.2rem; }
.rs-course {
  display: inline-flex; align-items: center; gap: 0.5rem;
  font-size: 0.86rem; font-weight: 500; color: #1a1a1a;
  border: 1px solid #e2e2de; border-radius: 999px; padding: 0.5rem 1rem; background: #fff;
}
.rs-course .ph { font-size: 1.1rem; color: #42a6ac; }

/* ---- research areas (reuses .challenge-card) ---- */
.rs-areas { margin-top: 1rem; }
.rs-areas .challenge-card { padding: 1.1rem 1.6rem; align-items: center; background: #fff; }
.rs-areas .challenge-title { margin: 0; font-size: 0.95rem; }

@media (max-width: 640px) {
  .rs-stats { grid-template-columns: repeat(2, 1fr); }
  .rs-stat:nth-child(2) { border-right: none; }
  .rs-stat:nth-child(-n+2) { border-bottom: 1px solid rgba(255,255,255,0.18); }
  .rs-wp-grid { grid-template-columns: 1fr; }
  .rs-pi { padding: 0.9rem 1rem; gap: 1rem; }
  .rs-ds { flex-direction: column; gap: 0.8rem; }
}
</style>
