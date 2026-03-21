---
layout: page
permalink: /honors/
title: Honors
nav: true
nav_order: 6
---

<style>
/* ── Nav pills ────────────────────────────────────────────────────────── */
.hn-nav {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  margin-bottom: 3rem;
}
.hn-nav-pill {
  flex: 1;
  min-width: 110px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.3rem;
  padding: 0.75rem 0.5rem;
  color: var(--global-theme-color);
  text-decoration: none !important;
  font-weight: 600;
  font-size: 0.9rem;
  transition: opacity 0.18s, transform 0.18s;
}
.hn-nav-pill i { font-size: 1.5rem; }
.hn-nav-pill:hover {
  opacity: 0.75;
  transform: translateY(-2px);
}

/* ── Section ──────────────────────────────────────────────────────────── */
.hn-section { margin-bottom: 3.5rem; }
.hn-section-header {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  margin-bottom: 1.5rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--global-theme-color);
}
.hn-section-header i { color: var(--global-theme-color); font-size: 1.2rem; }
.hn-section-header h2 {
  margin: 0 !important;
  font-size: 1.4rem !important;
  font-weight: 700 !important;
  color: var(--global-theme-color) !important;
  letter-spacing: normal !important;
  text-transform: none !important;
  border: none !important;
  padding: 0 !important;
}
.hn-section-header h2::after { display: none !important; }

/* ── Timeline ─────────────────────────────────────────────────────────── */
.hn-timeline {
  list-style: none;
  padding: 0;
  margin: 0;
  position: relative;
}
.hn-timeline::before {
  content: '';
  position: absolute;
  left: 10px;
  top: 6px;
  bottom: 6px;
  width: 2px;
  background: var(--global-divider-color);
}
.hn-timeline-item {
  display: flex;
  gap: 1.25rem;
  padding-left: 2rem;
  margin-bottom: 1.1rem;
  position: relative;
}
.hn-timeline-item::before {
  content: '';
  position: absolute;
  left: 2px;
  top: 5px;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: var(--global-theme-color);
  border: 3px solid var(--global-bg-color);
  box-shadow: 0 0 0 2px var(--global-theme-color);
}
.hn-timeline-year {
  min-width: 72px;
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--global-text-color-light);
  padding-top: 2px;
  flex-shrink: 0;
}
.hn-timeline-body { flex: 1; font-size: 0.88rem; line-height: 1.6; }

@media (max-width: 576px) {
  .hn-timeline-year { display: none; }
  .hn-nav-pill { min-width: 80px; font-size: 0.8rem; }
}
</style>

<!-- ── Navigation pills ───────────────────────────────────────────────── -->
<div class="hn-nav">
  <a href="#awards" class="hn-nav-pill">
    <i class="fa-solid fa-trophy"></i>
    <span>Awards</span>
  </a>
  <a href="#achievements" class="hn-nav-pill">
    <i class="fa-solid fa-medal"></i>
    <span>Achievements</span>
  </a>
</div>


<!-- ═══════════════════════ AWARDS ═══════════════════════════════════════ -->
<section id="awards" class="hn-section">
  <div class="hn-section-header">
    <i class="fa-solid fa-trophy"></i>
    <h2>Awards &amp; Scholarships</h2>
  </div>
  <ul class="hn-timeline">
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2025</span>
      <div class="hn-timeline-body">
        <strong>Golden Wings Award</strong> &mdash; <a href="https://www.goldenbookawards.com/shining-superstar/" target="_blank">Golden Book Awards</a> for the book <em>Cloud Computing for Everyone</em>
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2025</span>
      <div class="hn-timeline-body">
        <strong>Travel Grant</strong> &mdash; $1,000 to present doctoral dissertation at IEEE IJCNN Conference
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2023</span>
      <div class="hn-timeline-body">
        <strong>Visiting Researcher Grant</strong> &mdash; 3-month research stay at National University of Singapore (NUS), awarded by UiT
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2017&ndash;19</span>
      <div class="hn-timeline-body">
        <strong>Merit Cum Means (MCM) Scholarship</strong> &mdash; IIT (ISM) Dhanbad
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2017&ndash;18</span>
      <div class="hn-timeline-body">
        <strong>Director Scholarship</strong> &mdash; Excellence in academics, IIT (ISM) Dhanbad
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2018</span>
      <div class="hn-timeline-body">
        <strong>Science Academies&rsquo; Summer Research Fellowship</strong> &mdash; Indian Academy of Sciences
      </div>
    </li>
  </ul>
</section>


<!-- ═══════════════════════ ACHIEVEMENTS ═════════════════════════════════ -->
<section id="achievements" class="hn-section">
  <div class="hn-section-header">
    <i class="fa-solid fa-medal"></i>
    <h2>Achievements</h2>
  </div>
  <ul class="hn-timeline">
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2024</span>
      <div class="hn-timeline-body">
        <strong>Runner-up</strong> &mdash; DLN Mini-MBA, organized by Digital Life Norway
        (<a href="https://drive.google.com/file/d/1Gk7inD3IUaL9EWBrSwBAPsGwtZ2CtJKJ/view?usp=sharing" target="_blank">certificate</a>)
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2015&ndash;20</span>
      <div class="hn-timeline-body">
        <strong>Gold Medalist</strong> &mdash; Applied Mathematics Department, IIT (ISM) Dhanbad
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2015</span>
      <div class="hn-timeline-body">
        <strong>AIR 5017</strong> &mdash; IIT JEE Advanced among 1M+ candidates
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2015</span>
      <div class="hn-timeline-body">
        <strong>General Merit Rank 51</strong> &mdash; WBJEE among 3,00,000+ candidates
      </div>
    </li>
    <li class="hn-timeline-item">
      <span class="hn-timeline-year">2014</span>
      <div class="hn-timeline-body">
        <strong>International Rank 23 (Level 1) &amp; Rank 19 (Level 2)</strong> &mdash; International Olympiad of Mathematics
      </div>
    </li>
  </ul>
</section>
