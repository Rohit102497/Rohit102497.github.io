---
layout: page
permalink: /activities/
title: Activities
nav: true
nav_order: 4
---

<style>
/* ── Nav pills ────────────────────────────────────────────────────────── */
.sv-nav {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  margin-bottom: 3rem;
}
.sv-nav-pill {
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
.sv-nav-pill i { font-size: 1.5rem; }
.sv-nav-pill:hover {
  opacity: 0.75;
  transform: translateY(-2px);
}

/* ── Section ──────────────────────────────────────────────────────────── */
.sv-section { margin-bottom: 3.5rem; }
.sv-section-header {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  margin-bottom: 1.5rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--global-theme-color);
}
.sv-section-header i { color: var(--global-theme-color); font-size: 1.2rem; }
.sv-section-header h2 {
  margin: 0 !important;
  font-size: 1.4rem !important;
  font-weight: 700 !important;
  color: var(--global-theme-color) !important;
  letter-spacing: normal !important;
  text-transform: none !important;
  border: none !important;
  padding: 0 !important;
}
.sv-section-header h2::after { display: none !important; }

/* ── Subsection label ─────────────────────────────────────────────────── */
.sv-sub {
  font-size: 0.74rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  margin: 1.4rem 0 0.7rem;
}

/* ── Timeline ─────────────────────────────────────────────────────────── */
.sv-timeline {
  list-style: none;
  padding: 0;
  margin: 0;
  position: relative;
}
.sv-timeline::before {
  content: '';
  position: absolute;
  left: 10px;
  top: 6px;
  bottom: 6px;
  width: 2px;
  background: var(--global-divider-color);
}
.sv-timeline-item {
  display: flex;
  gap: 1.25rem;
  padding-left: 2rem;
  margin-bottom: 1.1rem;
  position: relative;
}
.sv-timeline-item::before {
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
.sv-timeline-year {
  min-width: 50px;
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--global-text-color-light);
  padding-top: 2px;
  flex-shrink: 0;
}
.sv-timeline-body { flex: 1; font-size: 0.88rem; line-height: 1.6; }

/* ── Conference / Journal badges ─────────────────────────────────────── */
.sv-badge {
  display: inline-block;
  font-size: 0.65rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 0.08rem 0.45rem;
  border-radius: 8px;
  margin-right: 0.1rem;
  vertical-align: middle;
}
.sv-badge-C { background: rgba(61,126,191,0.13); color: #3d7ebf; }
.sv-badge-J { background: rgba(94,158,110,0.13); color: #5e9e6e; }

/* ── Cards grid (supervision, teaching) ──────────────────────────────── */
.sv-card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1.1rem;
}
.sv-card {
  padding: 1.1rem 1.25rem;
  border: 1px solid var(--global-divider-color);
  border-top: 3px solid var(--global-theme-color);
  border-radius: 0 0 8px 8px;
  background: var(--global-card-bg-color, var(--global-bg-color));
  transition: box-shadow 0.18s, transform 0.18s;
}
.sv-card:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.08);
  transform: translateY(-2px);
}
.sv-card-period {
  font-size: 0.72rem;
  font-weight: 700;
  color: var(--global-theme-color);
  text-transform: uppercase;
  letter-spacing: 0.06em;
  margin-bottom: 0.35rem;
}
.sv-card-title { font-size: 0.95rem; font-weight: 700; margin-bottom: 0.2rem; }
.sv-card-sub { font-size: 0.82rem; color: var(--global-text-color-light); line-height: 1.5; margin-bottom: 0.6rem; }
.sv-card-link {
  display: inline-block;
  font-size: 0.72rem;
  padding: 0.15rem 0.6rem;
  border: 1px solid var(--global-theme-color);
  border-radius: 20px;
  color: var(--global-theme-color);
  text-decoration: none !important;
  transition: background 0.15s, color 0.15s;
}
.sv-card-link:hover { background: var(--global-theme-color); color: #fff !important; }

/* ── Membership list ──────────────────────────────────────────────────── */
.sv-list { list-style: none; padding: 0; margin: 0; }
.sv-list li {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  padding: 0.65rem 0;
  border-bottom: 1px solid var(--global-divider-color);
  font-size: 0.88rem;
  line-height: 1.5;
}
.sv-list li:last-child { border-bottom: none; }
.sv-list-icon {
  color: var(--global-theme-color);
  font-size: 0.85rem;
  padding-top: 0.15rem;
  flex-shrink: 0;
  width: 16px;
  text-align: center;
}
.sv-list-year {
  min-width: 72px;
  font-size: 0.74rem;
  font-weight: 600;
  color: var(--global-text-color-light);
  flex-shrink: 0;
  padding-top: 0.05rem;
}

@media (max-width: 576px) {
  .sv-timeline-year { display: none; }
  .sv-nav-pill { min-width: 80px; font-size: 0.8rem; }
  .sv-list-year { display: none; }
}
</style>

<!-- ── Navigation pills ───────────────────────────────────────────────── -->
<div class="sv-nav">
  <a href="#academic" class="sv-nav-pill">
    <i class="fa-solid fa-clipboard-check"></i>
    <span>Academic</span>
  </a>
  <a href="#supervision" class="sv-nav-pill">
    <i class="fa-solid fa-user-graduate"></i>
    <span>Supervision</span>
  </a>
  <a href="#teaching" class="sv-nav-pill">
    <i class="fa-solid fa-chalkboard-user"></i>
    <span>Teaching</span>
  </a>
  <a href="#community" class="sv-nav-pill">
    <i class="fa-solid fa-users"></i>
    <span>Community</span>
  </a>
</div>


<!-- ═══════════════════════ ACADEMIC SERVICE ═════════════════════════════ -->
<section id="academic" class="sv-section">
  <div class="sv-section-header">
    <i class="fa-solid fa-clipboard-check"></i>
    <h2>Academic Service</h2>
  </div>

  <p class="sv-sub">Reviewing</p>
  <ul class="sv-timeline">
    <li class="sv-timeline-item">
      <span class="sv-timeline-year">2026</span>
      <div class="sv-timeline-body">
        <span class="sv-badge sv-badge-J">J</span> TMLR
      </div>
    </li>
    <li class="sv-timeline-item">
      <span class="sv-timeline-year">2025</span>
      <div class="sv-timeline-body">
        <span class="sv-badge sv-badge-C">C</span> ICLR
      </div>
    </li>
    <li class="sv-timeline-item">
      <span class="sv-timeline-year">2024</span>
      <div class="sv-timeline-body">
        <span class="sv-badge sv-badge-C">C</span> ICASSP &times;2 &ensp;
        <span class="sv-badge sv-badge-C">C</span> <a href="https://www.bioailab.org/sprcv-workshop/home" target="_blank">ICPR-SPRCV</a> &ensp;
        <span class="sv-badge sv-badge-J">J</span> IEEE TGRS &ensp;
        <span class="sv-badge sv-badge-J">J</span> TMLR
      </div>
    </li>
    <li class="sv-timeline-item">
      <span class="sv-timeline-year">2023</span>
      <div class="sv-timeline-body">
        <span class="sv-badge sv-badge-C">C</span> <a href="https://drive.google.com/file/d/1faP94c4oVwRi5Ui1D4a7RxL_IgQ8EAZO/view?usp=sharing" target="_blank">ICDEC</a> &times;2 &ensp;
        <span class="sv-badge sv-badge-J">J</span> Nordic Machine Intelligence (NMI)
      </div>
    </li>
  </ul>

  <p class="sv-sub">Program Committee</p>
  <ul class="sv-timeline">
    <li class="sv-timeline-item">
      <span class="sv-timeline-year">2024</span>
      <div class="sv-timeline-body">International Conference on Pattern Recognition (ICPR) &mdash; SPRCV Workshop</div>
    </li>
    <li class="sv-timeline-item">
      <span class="sv-timeline-year">2023</span>
      <div class="sv-timeline-body">International Conference on Neural Information Processing (ICONIP)</div>
    </li>
  </ul>

</section>


<!-- ═══════════════════════ SUPERVISION ══════════════════════════════════ -->
<section id="supervision" class="sv-section">
  <div class="sv-section-header">
    <i class="fa-solid fa-user-graduate"></i>
    <h2>Supervision</h2>
  </div>
  <div class="sv-card-grid">
    <div class="sv-card">
      <div class="sv-card-period">2025 &ndash; 2026</div>
      <div class="sv-card-title">Arijit Das</div>
      <div class="sv-card-sub">Master&rsquo;s Student<br>IIT (ISM) Dhanbad</div>
    </div>
    <div class="sv-card">
      <div class="sv-card-period">2022 &ndash; 2023</div>
      <div class="sv-card-title">Aaron Celeste</div>
      <div class="sv-card-sub">Master&rsquo;s Student<br>UiT The Arctic University of Norway</div>
      <a href="https://munin.uit.no/handle/10037/29335" target="_blank" class="sv-card-link">Thesis &rarr;</a>
    </div>
  </div>
</section>


<!-- ═══════════════════════ TEACHING ═════════════════════════════════════ -->
<section id="teaching" class="sv-section">
  <div class="sv-section-header">
    <i class="fa-solid fa-chalkboard-user"></i>
    <h2>Teaching</h2>
  </div>
  <div class="sv-card-grid">
    <div class="sv-card">
      <div class="sv-card-period">Fall 2021, 2022, 2023, 2024</div>
      <div class="sv-card-title">Cloud and Big Data Technology</div>
      <div class="sv-card-sub">INF-2220-1 &mdash; Teaching Assistant<br>UiT The Arctic University of Norway</div>
    </div>
    <div class="sv-card">
      <div class="sv-card-period">Spring 2023, 2024</div>
      <div class="sv-card-title">AI &mdash; Methods and Applications</div>
      <div class="sv-card-sub">INF-2600-1 &mdash; Teaching Assistant<br>UiT The Arctic University of Norway</div>
    </div>
  </div>
</section>


<!-- ═══════════════════════ COMMUNITY & MEMBERSHIPS ══════════════════════ -->
<section id="community" class="sv-section">
  <div class="sv-section-header">
    <i class="fa-solid fa-users"></i>
    <h2>Community &amp; Memberships</h2>
  </div>
  <ul class="sv-list">
    <li>
      <i class="fa-solid fa-circle-check sv-list-icon"></i>
      <span class="sv-list-year">2023&ndash;25</span>
      <span><strong>Board Member</strong> &mdash; Digital Life Norway, <a href="https://www.digitallifenorway.org/about/organisation/junior_resource_group.html" target="_blank">Junior Research Group</a></span>
    </li>
    <li>
      <i class="fa-solid fa-circle-check sv-list-icon"></i>
      <span class="sv-list-year">2021&ndash;</span>
      <span><strong>Member</strong> &mdash; Norwegian Artificial Intelligence Research Consortium (NORA)</span>
    </li>
    <li>
      <i class="fa-solid fa-circle-check sv-list-icon"></i>
      <span class="sv-list-year">2023</span>
      <span><strong>Member</strong> &mdash; Institute of Electrical and Electronics Engineers (IEEE)</span>
    </li>
    <li>
      <i class="fa-solid fa-volleyball sv-list-icon"></i>
      <span class="sv-list-year">2021&ndash;</span>
      <span><strong>Division 2 Volleyball Player</strong> &mdash; Tromsøstudentenes Idrettslag, Tromsø</span>
    </li>
    <li>
      <i class="fa-solid fa-chalkboard sv-list-icon"></i>
      <span class="sv-list-year">2019&ndash;20</span>
      <span><strong>Mentor</strong> &mdash; Data Science Club (DSC), IIT (ISM) Dhanbad</span>
    </li>
  </ul>
</section>
